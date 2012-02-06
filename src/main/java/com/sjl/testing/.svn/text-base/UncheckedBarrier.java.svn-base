package com.sjl.testing;


import java.util.concurrent.*;

/**
 * Intended for use in TestCases only ...
 * @author steve 
 */
public class UncheckedBarrier {

	private CyclicBarrier barrier;
	
	public UncheckedBarrier(int aParties) {
		barrier = new CyclicBarrier(aParties);
	}

	public int await() {
		try {
			return barrier.await();
		} catch (Exception anExc) {
			throw new RuntimeException(anExc);
		}
	}

	public int await(long anTimeout, TimeUnit anUnit) {
		try {
			return barrier.await(anTimeout, anUnit);
		} catch (Exception anExc) {
			throw new RuntimeException(anExc);
		}		
	}

	public int getNumberWaiting() {
		return barrier.getNumberWaiting();
	}

	public int getParties() {
		return barrier.getParties();
	}

	public boolean isBroken() {
		return barrier.isBroken();
	}

	public void reset() {
		barrier.reset();
	}
		
	
}
