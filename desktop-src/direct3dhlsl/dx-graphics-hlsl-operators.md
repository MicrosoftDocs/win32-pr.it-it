---
title: Operatori
description: Le espressioni sono sequenze di variabili e valori letterali punteggiati da operatori.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7a44fe02983038658247fedaec7122f09306548
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119606"
---
# <a name="operators"></a>Operatori

Le espressioni sono sequenze di [variabili](dx-graphics-hlsl-variable-syntax.md) e valori letterali punteggiati dagli [operatori](dx-graphics-hlsl-statement-blocks.md). Gli operatori determinano il modo in cui le variabili e i valori letterali vengono combinati, confrontati, selezionati e così via. Gli operatori includono:



| Nome operatore                                                                                | Operatori                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Operatori additivi e moltiplicativi](#additive-and-multiplicative-operators) | +, -, \*, /, %                                                     |
| [Operatore Array](#array-operator)                                               | \[i\]                                                              |
| [Operatori di assegnazione](#assignment-operators)                                   | =, +=, -=, \*=, /=, %=                                             |
| [Cast binari](#binary-casts)                                                   | Regole C per float e int, regole C o intrinseci HLSL per bool     |
| [Operatori bit per bit](#bitwise-operators)                                         | ~, <<, >>, &, \| , ^, <<=, >>=, &=, \| =, ^= |
| [Operatori matematici booleani](#boolean-math-operators)                               | & &, , \| \| ?:                                                      |
| [Operatore Cast](#cast-operator)                                                 | (tipo)                                                             |
| [Operatore virgola](#comma-operator)                                               | ,                                                                  |
| [Operatori di confronto](#comparison-operators)                                   | <, >, ==, !=, <=, >=                                   |
| [Operatori di prefisso o suffisso](#prefix-or-postfix-operators)                     | ++, --                                                             |
| [Operatore Structure](#structure-operator)                                       | .                                                                  |
| [Operatori unari](#unary-operators)                                             | !, -, +                                                            |



 

Molti operatori sono per componente, pertanto l'operazione viene eseguita in modo indipendente per ogni componente di ogni variabile. Ad esempio, una singola variabile componente ha un'operazione eseguita. D'altra parte, una variabile a quattro componenti ha quattro operazioni eseguite, una per ogni componente.

Tutti gli operatori che e fanno qualcosa per il valore, ad esempio + e \* , funzionano per componente.

Gli operatori di confronto richiedono il funzionamento di un singolo componente, a meno che non si usi [**la**](dx-graphics-hlsl-all.md) funzione all o [**qualsiasi**](dx-graphics-hlsl-any.md) funzione intrinseca con una variabile a più componenti. L'operazione seguente non riesce perché l'istruzione if richiede un singolo bool ma riceve un bool4:


```
if (A4 < B4)
```



Le operazioni seguenti hanno esito positivo:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



Gli operatori di cast binari [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md)e così via funzionano per componente, ad eccezione di [**asdouble**](asdouble.md) le cui regole speciali sono documentate.

Gli operatori di selezione, ad esempio punto, virgola e parentesi di matrice, non funzionano per componente.

Gli operatori cast modificano il numero di componenti. Le operazioni cast seguenti mostrano l'equivalenza:


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a>Operatori additivi e moltiplicativi

Gli operatori additivi e moltiplicativi sono: +, -, \* , /, %


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



L'operatore modulo restituisce il resto di una divisione. Ciò produce risultati diversi quando si usano numeri interi e numeri a virgola mobile. I resti interi frazionari verranno troncati.


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



L'operatore modulo tronca un resto frazionario quando si usano numeri interi.


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



L'operatore % viene definito solo nei casi in cui entrambi i lati sono positivi o entrambi i lati sono negativi. A differenza di C, funziona anche su tipi di dati a virgola mobile, nonché su numeri interi.

## <a name="array-operator"></a>Operatore Array

L'operatore di selezione dei membri della matrice " \[ i " seleziona uno o più componenti in una \] matrice. È un set di parentesi quadre che contengono un indice in base zero.


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



L'operatore array può essere usato anche per accedere a un vettore.


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



Aggiungendo un indice aggiuntivo, l'operatore array può anche accedere a una matrice.


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



Il primo indice è l'indice di riga in base zero. Il secondo indice è l'indice di colonna in base zero.

## <a name="assignment-operators"></a>Operatori di assegnazione

Gli operatori di assegnazione sono: =, +=, -=, \* =, /=

Alle variabili possono essere assegnati valori letterali:


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



È anche possibile assegnare alle variabili il risultato di un'operazione matematica:


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



Una variabile può essere usata su entrambi i lati del segno di uguale:


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



La divisione per le variabili a virgola mobile è come previsto perché i resti decimali non sono un problema.


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



Prestare attenzione se si usano numeri interi che possono essere divisi, soprattutto quando il troncamento influisce sul risultato. Questo esempio è identico all'esempio precedente, ad eccezione del tipo di dati . Il troncamento causa un risultato molto diverso.


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a>Cast binari

L'operazione di cast tra int e float converte il valore numerico nelle rappresentazioni appropriate in base alle regole C per il troncamento di un tipo int. Il cast di un valore da float a int e di nuovo a un tipo float comporta una conversione in perdita in base alla precisione della destinazione.

I cast binari possono essere eseguiti anche usando [**funzioni intrinseche (DirectX HLSL),**](dx-graphics-hlsl-intrinsic-functions.md)che reinterpretano la rappresentazione in bit di un numero nel tipo di dati di destinazione.


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a>Operatori bit per bit

HLSL supporta gli operatori bit per bit seguenti, che seguono la stessa precedenza di C rispetto ad altri operatori. Nella tabella seguente vengono descritti gli operatori .

> [!Note]  
> Gli operatori bit per bit [richiedono Shader Model \_ 4 0](dx-graphics-hlsl-sm4.md) con Direct3D 10 e hardware superiore.

 



| Operatore          |  Funzione                 |
|-----------|-------------------|
| ~         | Not logico       |
| <<  | Maiusc di sinistra        |
| >>  | Maiusc di destra       |
| &         | And logico       |
| \|        | Esegue un'operazione di Or logico.        |
| ^         | Xor logico       |
| <<= | Maiusc di sinistra uguale  |
| >>= | Maiusc destro uguale |
| &=        | E uguale         |
| \|=       | O uguale a          |
| ^=        | Xor Uguale         |



 

Gli operatori bit per bit vengono definiti per operare solo sui tipi di dati int e uint. Il tentativo di usare operatori bit per bit su tipi di dati float o struct restituirà un errore.

## <a name="boolean-math-operators"></a>Operatori matematici booleani

Gli operatori matematici booleani sono:  &&, \| \| , ?:


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



A differenza della valutazione di corto circuito di &&, e ?: in C, le espressioni HLSL non esereranno mai un corto circuito per una valutazione perché \| \| sono operazioni vettoriali. Tutti i lati dell'espressione vengono sempre valutati.

Gli operatori booleani funzionano in base al componente. Ciò significa che se si confrontano due vettori, il risultato è un vettore contenente il risultato booleano del confronto per ogni componente.

Per le espressioni che usano operatori booleani, le dimensioni e il tipo di componente di ogni variabile vengono promossi in modo che siano uguali prima che venga eseguita l'operazione. Il tipo alzato di livello determina la risoluzione in corrispondenza della quale viene eseguita l'operazione, nonché il tipo di risultato dell'espressione. Ad esempio, un'espressione int3 + float viene promossa a float3 + float3 per la valutazione e il risultato sarà di tipo float3.

## <a name="cast-operator"></a>Operatore cast

Un'espressione preceduta da un nome di tipo tra parentesi è un cast di tipo esplicito. Un cast di tipo converte l'espressione originale nel tipo di dati del cast. In generale, è possibile eseguire il cast dei tipi di dati semplici ai tipi di dati più complessi (con un cast di promozione), ma è possibile eseguire il cast solo di alcuni tipi di dati complessi in tipi di dati semplici (con un cast di abbassamento di livello).

È valido solo il cast del tipo sul lato destro. Ad esempio, espressioni come non `(int)myFloat = myInt;` sono valide. In alternativa, utilizzare `myFloat = (float)myInt;`.

Il compilatore esegue anche il cast di tipo implicito. Ad esempio, le due espressioni seguenti sono equivalenti:


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a>Operatore virgola

L'operatore virgola (,) separa una o più espressioni che devono essere valutate in ordine. Il valore dell'ultima espressione nella sequenza viene usato come valore della sequenza.

Ecco un caso a cui vale la pena richiamare l'attenzione. Se il tipo di costruttore viene accidentalmente lasciato fuori dal lato destro del segno di uguale, il lato destro contiene ora quattro espressioni, separate da tre virgole.


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



L'operatore virgola valuta un'espressione da sinistra a destra. In questo modo si riduce il lato destro per:


```
float4 x = 1; 
```



HLSL usa la promozione scalare in questo caso, quindi il risultato è come se fosse scritto come segue:


```
float4 x = float4(1,1,1,1);
```



In questo caso, lasciare il tipo float4 dal lato destro è probabilmente un errore che il compilatore non è in grado di rilevare perché si tratta di un'istruzione valida.

## <a name="comparison-operators"></a>Operatori di confronto

Gli operatori di confronto sono: <, >, ==, !=, <=, >=.

Confrontare i valori maggiori o minori di qualsiasi valore scalare:


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



In caso contrario, confrontare i valori uguali (o non uguali) a qualsiasi valore scalare:


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



Oppure combinare e confrontare valori maggiori o uguali a (o minori o uguali a) qualsiasi valore scalare:


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



Ognuno di questi confronti può essere eseguito con qualsiasi tipo di dati scalare.

Per usare gli operatori di confronto con i tipi di vettore e matrice, usare la [**funzione intrinseca all**](dx-graphics-hlsl-all.md) [**o**](dx-graphics-hlsl-any.md) any.

Questa operazione ha esito negativo perché l'istruzione if richiede un solo bool ma riceve un valore bool4:


```
if (A4 < B4)
```



Queste operazioni hanno esito positivo:


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a>Operatori prefisso o suffisso

Gli operatori prefisso e suffisso sono: ++, --. Gli operatori di prefisso modificano il contenuto della variabile prima che l'espressione venga valutata. Gli operatori suffissi modificano il contenuto della variabile dopo la valutazione dell'espressione.

In questo caso, un ciclo usa il contenuto di i per tenere traccia del conteggio dei cicli.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



Poiché viene usato l'operatore di incremento suffisso (++), arrayOfFloats i viene moltiplicato per \[ \] 2 prima che i venga incrementato. Questa operazione potrebbe essere leggermente ridisposta in modo da usare l'operatore di incremento prefisso. Questo è più difficile da leggere, anche se entrambi gli esempi sono equivalenti.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



Poiché viene usato l'operatore prefisso (++), arrayOfFloats \[ i+1 - 1 viene moltiplicato per 2 dopo l'incremento \] di i.

L'operatore di decremento prefisso e decremento suffisso (--) viene applicato nella stessa sequenza dell'operatore di incremento. La differenza è che il decremento sottrae 1 anziché aggiungere 1.

## <a name="structure-operator"></a>Operatore Structure

L'operatore di selezione dei membri della struttura (.) è un punto. Data questa struttura:


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



Può essere letto nel modo seguente:


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



Ogni membro può essere letto o scritto con l'operatore structure:


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a>Operatori unari

Gli operatori unari sono: !, -, +

Gli operatori unari operano su un singolo operando.


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a>Ordine di precedenza degli operatori

Quando un'espressione contiene più di un operatore, la precedenza degli operatori determina l'ordine di valutazione. La precedenza degli operatori per HLSL segue la stessa precedenza di C.

## <a name="remarks"></a>Commenti

Le parentesi graffe ( {,} ) avviano e terminano un blocco di istruzioni. Quando un blocco di istruzioni usa una singola istruzione, le parentesi graffe sono facoltative.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni (DirectX HLSL)](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




