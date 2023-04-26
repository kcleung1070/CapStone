# CapStone
DAML CapStone 

# Bidding App
Daml templates designed for a platform for Bidding items, which will then be rejected/accepted by the seller.

### I. Overview 
This project was created by using the `empty-skeleton` template. The buyer, a signatory, can create a Bid contract. Then the seller can exercise the Accept choice as a controller to accept the Bid, or reject the Bid with a reason. If the seller exercises Reject choice on the Bid, the buyer can exercise Offer choice on it to raise the bidding price. Upon seller exercising the Accept choice, a Settlement contract is created.


### II. Workflow
1. A buyer creates a Bid contract. The staff is an obeserver. The seller, as a controller, is authorized to exercise either Reject or Accept choices.
2. Upon the controller exercising Reject, a new contract is created.
3. Offer choice can be exercised on the newly generated contract from above.
4. Accept choice is exercised to finalize the Bid and generate a new Settlement contract.


### III. Building
To compile the project
```
$ daml build
```

### IV. Testing
To test all scripts:
Either run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start
```

### V. Running
To load the project into the sandbox and start navigator:
```
$ daml start
```
