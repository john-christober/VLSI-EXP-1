# EXP.NO-1
DATESIMULATIONANDIMPLEMENTATIONOFLOGICGATESAND
4BITADDER&SUBTRACTOR
AIM:TosimulateandsynthesisLogicGates,AddersandSubtractorusingVIVADO
APPARATUSREQUIRED:VIVADO2023.2
PROCEDURE:
STEP:1StarttheVivado,SelectandNametheNewproject.
STEP:2Selectthedevicefamily,device,packageandspeed.
STEP:3SelectnewsourceintheNewProjectandselectVerilogModuleasthe
Sourcetype.
STEP:4TypetheFileNameandClickNextandthenfinishbutton.Typethecodeand
saveit.
STEP:5SelecttheBehaviouralSimulationintheSourceWindowandclickthecheck
syntax.
STEP:6Clickthesimulationtosimulatetheprogram andgivetheinputsandverify
theoutputsasperthetruthtable.


# LOGIC-GATES:
      
 ![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/02a01b7a-4ddf-4441-a0a5-a2c2aa86df38)


PROGRAM:
modulelogic_gates(a,b,andgate,orgate,xorgate,nandgate,norgate,xnorgate,notgate);
inputa,b;
outputandgate,orgate,xorgate,nandgate,norgate,xnorgate,notgate;
and(andgate,a,b);
or(orgate,a,b);
xor(xorgate,a,b);
nand(nandgate,a,b);
nor(norgate,a,b);
xnor(xnorgate,a,b);
not(notgate,a);
endmodule
OUTPUT:
       ![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/7d9c2e0b-b01a-4afe-bea9-2e6858223a16)


# HALFADDER:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/a4774506-0996-4dda-ac3b-219a63891a54)


PROGRAM:
moduleha(a,b,sum,carry);
inputa,b;
outputsum,carry;
assignsum=a^b;
assigncarry=a&b;
endmodule

output:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/a768de88-cfe3-4d18-b7ec-2a9944cb2521)

# HALFSUBTRACTOR:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/a00fac58-563d-481b-bdd5-306ae6bb1ede)

PROGRAM:
modulehs(a,b,diff,borrow);
inputa,b;
outputdiff,borrow;
assigndiff=a^b;
assignborrow=~a&b;
endmodule

output:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/cd53d44a-1aa3-41a4-a96a-28e7308d7904)

# FULLADDER:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/4e0052a4-aa46-4729-9ae8-de4fd754555b)


PROGRAM:
modulefa(a,b,c,sum,carry);
inputa,b,c;
outputsum,carry;
assignsum=a^b^c;
assigncarry=(a&b)|(a&c)|(b&c);
endmodule
OUTPUT:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/6260275d-65bd-4980-a326-dbbbbe06d527)

# FULLSUBTRACTOR:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/45da3aef-8d5c-4c79-86a6-1a9f680fd14c)


PROGRAM:
modulefs(a,b,c,diff,borrow);
inputa,b,c;
outputdiff,borrow;
assigndiff=a^b^c;
assignborrow=(~a&c)|(~a&b)|(b&c);
endmodule

OUTPUT:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/30cf6ec9-0b61-467d-9fbb-1d25df8d1379)

# 8-BIT-RIPPLE-CARRY-ADDER:
![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/74b8abed-8dd8-40fd-8de4-1e8007b642f1)

PROGRAM:
moduleripplemod(a,b,cin,sum,cout);
input[07:0]a;
input[07:0]b;
inputcin;
output[7:0]sum;
outputcout;
wire[6:0]c;
fulladda1(a[0],b[0],cin,sum[0],c[0]);
fulladda2(a[1],b[1],c[0],sum[1],c[1]);
fulladda3(a[2],b[2],c[1],sum[2],c[2]);
fulladda4(a[3],b[3],c[2],sum[3],c[3]);
fulladda6(a[5],b[5],c[4],sum[5],c[5]);
fulladda7(a[6],b[6],c[5],sum[6],c[6]);
fulladda8(a[7],b[7],c[6],sum[7],cout);
endmodule
modulefulladd(a,b,cin,sum,cout);
inputa;
inputb;
inputcin;
outputsum;
outputcout;
assignsum=(a^b^cin);
assigncout=((a&b)|(b&cin)|(a&cin));
endmodule

OUTPUT:
 ![image](https://github.com/john-christober/vlsi-exp1/assets/145186233/fb7cda03-f1e9-40ea-8ea0-a72a4635e075)

# RESULT:
  Thus,thelogicgatesand4BitofAdderandSubtractorareImplementedandsimulatedsuccessfully.
