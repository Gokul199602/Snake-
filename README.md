# Snake-
Its a snake and ladder game



//code for moving the player

public class Points : MonoBehaviour 
{
//Variables declared
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


// Code to Generate Random Numbers.
public class RandomGenerator : MonoBehaviour {
	public TextMesh text1 = null;
	public bool click = true;
	public bool canMove = false;
	public Camera camera = null;
	public int t = 0;
	public Ray ray;
	public RaycastHit hit;
	public Points move = null;
	public int pin = 0;
	public int pin1 = 0;
	public Points move1 = null;
	public int i =0;
	public int j =0;
	public TextMesh text = null;
	public int k = 0;
	public int number;
	
	//Generate the random no.s
	public void RandomGenerate()
	{
		number = Random.Range (1,6);
		text.text = number.ToString ();
		pin = pin+number;
		Debug.Log ("pin:"+pin);
	}
	public void RandomGenerate1()
	{
		number = Random.Range (1,6);
		text.text = number.ToString ();
		pin1 = pin1+number;
		Debug.Log ("pin:"+pin1);
	}
	//click to update the position of player.
	void Update(){

		if (j==1) {
				  move.Move (pin1);
			text1.text ="Player:1";
				}
		if (k == 1) 
		{
			move1.Move(pin);
			text1.text ="Player:2";
		}
		if (Input.GetMouseButtonDown (0)) 
		{

			ray = camera.ScreenPointToRay(Input.mousePosition);
			if(Physics.Raycast(ray, out hit))
			{
				
				if(hit.collider.name== this.name)
				{
					if(click == true){
					RandomGenerate1();
				    j=1;
						k=0;
						click = false;
					}
					else if(click==false)
					{
						RandomGenerate();
						k=1;
						j=0;
						click = true;
					}

				}
			}
		}
		}



	}

