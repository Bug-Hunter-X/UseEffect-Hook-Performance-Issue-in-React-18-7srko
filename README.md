# React useEffect Hook Performance Issue

This repository demonstrates a common performance issue related to the `useEffect` hook in React 18.  The provided code example shows an effect that runs after every render, even when there's no need. This leads to unnecessary re-renders and potential performance bottlenecks. The solution demonstrates how to correctly specify dependencies to optimize the effect's execution.

## Problem

The initial implementation of the `useEffect` hook lacks proper dependency management. This causes the effect to run after every render, significantly impacting performance. The cleanup function also executes repeatedly, which may be inefficient or even harmful in certain scenarios.

## Solution

The solution involves adding the relevant state variable (`count` in this case) to the dependency array of the `useEffect` hook.  This ensures that the effect only runs when the value of `count` changes.