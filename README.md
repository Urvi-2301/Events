public class EventPublisher
{
   
    public event EventHandler<MyEventArgs> MyEventOccurred;


    protected virtual void OnMyEventOccurred(string message)
    {
       
        MyEventOccurred?.Invoke(this, new MyEventArgs(message));
    }

    
    public void PerformAction()
    {
       
        OnMyEventOccurred("Event message here!");
    }
}
