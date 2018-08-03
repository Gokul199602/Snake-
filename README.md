# Snake-
Its a snake and ladder game

code for moving the player


using UnityEngine;
using System.Collections;

public class Points : MonoBehaviour {
	public Transform[] points;
	public float moveSpeed = 1f;
	public int pointIndex = 0;
	public RandomGenerator j = null;
	public RandomGenerator k = null;
	public RandomGenerator pin = null;
	public RandomGenerator pin1 = null;
	public RandomGenerator pin2 = null;
	public RandomGenerator pin3 = null;
	public RandomGenerator random = null;
	public void Start()
	{
		transform.position = points [pointIndex].transform.position;
		Debug.Log (points.Length);

	}
  
//Player reach the finish point

	public void Move(int i)
	{
				 {
			if(transform.position==points[99].transform.position)
			{
				if(j.j==1){
				Application.LoadLevel(4);
				}
				else if(k.k==1)
				{
					Application.LoadLevel(5);
				}

			}
			//ladder to climb high
			if(transform.position==points[3].transform.position)
			{
				Debug.Log("Hello");
				transform.position = Vector2.MoveTowards (transform.position, points [13].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
				pin.pin=13;
				}
				if(j.j==1){
				pin1.pin1=13;
				}

			}
			if(transform.position==points[8].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [30].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
				pin.pin=30;
				}
				if(j.j==1){
				pin1.pin1=30;
				}
				Debug.Log("Hello");
			}
			if(transform.position==points[19].transform.position)
			{
				Debug.Log("Hello");
				transform.position = Vector2.MoveTowards (transform.position, points [37].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
				pin.pin=37;
				}
				if(j.j==1){
				pin1.pin1=37;
				}
			}
			if(transform.position==points[27].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [83].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
				pin.pin=83;
				}
				if(j.j==1){
				pin1.pin1=83;
				}
				Debug.Log("Hello");
			}
			if(transform.position==points[39].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [58].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
				pin.pin=58;
				}
				if(j.j==1){
				pin1.pin1=59;
				}
				Debug.Log("Hello");
			}
			if(transform.position==points[62].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [80].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
				pin.pin=81;
				}
				if(j.j==1){
				pin1.pin1=81;
				}
				Debug.Log("Hello");
			}
			if(transform.position==points[70].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [90].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
				pin.pin=91;
				}
				if(j.j==1){
				pin1.pin1=91;
				}
				Debug.Log("Hello");
			}
      
			//To increment the player on every roll of dice
				if (pointIndex <= points.Length) {
				pointIndex=i;
				transform.position = Vector2.MoveTowards (transform.position, points [i].transform.position, moveSpeed * Time.deltaTime);
								if (transform.position == points [pointIndex].transform.position) {
										pointIndex += 1;
								}
						}
            
			//snake eats player code
			if(transform.position==points[16].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [7].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
					pin.pin=6;
				}
				if(j.j==1){
					pin1.pin1=6;
				}
				
			}
			if(transform.position==points[53].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [33].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
					pin.pin=33;
				}
				if(j.j==1){
					pin1.pin1=33;
				}
				
			}
			if(transform.position==points[61].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [13].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
					pin.pin=17;
				}
				if(j.j==1){
					pin1.pin1=17;
				}
				
			}
			if(transform.position==points[63].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [13].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
					pin.pin=59;
				}
				if(j.j==1){
					pin1.pin1=59;
				}
				
			}
			if(transform.position==points[86].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [13].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
					pin.pin=23;
				}
				if(j.j==1){
					pin1.pin1=23;
				}
				
			}
			if(transform.position==points[92].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [72].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
					pin.pin=72;
				}
				if(j.j==1){
					pin1.pin1=72;
				}
				
			}
			if(transform.position==points[94].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [13].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
					pin.pin=74;
				}
				if(j.j==1){
					pin1.pin1=74;
				}
				
			}
			if(transform.position==points[98].transform.position)
			{
				transform.position = Vector2.MoveTowards (transform.position, points [13].transform.position, moveSpeed * Time.deltaTime);
				if(k.k==1){
					pin.pin=77;
				}
				if(j.j==1){
					pin1.pin1=77;
				}
				
			}
				}
		}
}
