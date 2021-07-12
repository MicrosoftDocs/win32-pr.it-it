---
title: Per-Component operazioni matematiche
description: Con HLSL è possibile programmare shader a livello di algoritmo.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5cd065e415aafffa59dd6c31d2b9aa4f4505021d
ms.sourcegitcommit: 7c7a05f65d2cf1ba2dadf05f63ae91a048083946
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113589588"
---
# <a name="per-component-math-operations"></a>Per-Component operazioni matematiche

Con HLSL è possibile programmare shader a livello di algoritmo. Per comprendere il linguaggio, è necessario sapere come dichiarare variabili e funzioni, usare funzioni intrinseche, definire tipi di dati personalizzati e usare la semantica per connettere argomenti shader ad altri shader e alla pipeline.

Dopo aver appreso come creare shader in HLSL, è necessario conoscere le chiamate API in modo da poter compilare uno shader per hardware specifico, inizializzare le costanti dello shader e inizializzare altri stati della pipeline, se necessario.

-   [Tipo di vettore](#the-vector-type)
-   [Tipo di matrice](#the-matrix-type)
    -   [Ordinamento delle matrici](#matrix-ordering)
-   [esempi](#examples)
-   [Argomenti correlati](#related-topics)

## <a name="the-vector-type"></a>Tipo di vettore

Un vettore è una struttura di dati che contiene tra uno e quattro componenti.


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



L'intero immediatamente successivo al tipo di dati è il numero di componenti nel vettore.

Gli inizializzatori possono anche essere inclusi nelle dichiarazioni.


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



In alternativa, il tipo di vettore può essere usato per creare le stesse dichiarazioni:


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Il tipo di vettore usa parentesi angolari per specificare il tipo e il numero di componenti.

I vettori contengono fino a quattro componenti, ognuno dei quali è accessibile usando uno dei due set di denominazione:

-   Posizione impostata: x,y,z,w
-   Set di colori: r,g,b,a

Entrambe queste istruzioni restituiscono il valore nel terzo componente.


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



I set di denominazione possono usare uno o più componenti, ma non possono essere misti.


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



La specifica di uno o più componenti vettoriali durante la lettura dei componenti è detta swizzling. Ad esempio:


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



La maschera controlla il numero di componenti scritti.


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



Le assegnazioni non possono essere scritte nello stesso componente più di una volta. Il lato sinistro di questa istruzione non è quindi valido:


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



Inoltre, gli spazi dei nomi dei componenti non possono essere misti. Si tratta di un componente non valido:


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



L'accesso a un vettore come scalare accederà al primo componente del vettore. Le due istruzioni seguenti sono equivalenti.


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>Tipo di matrice

Una matrice è una struttura di dati che contiene righe e colonne di dati. I dati possono essere di qualsiasi tipo scalare, tuttavia, ogni elemento di una matrice è dello stesso tipo di dati. Il numero di righe e colonne viene specificato con la stringa riga per colonna aggiunta al tipo di dati .


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



Il numero massimo di righe o colonne è 4. il numero minimo è 1.

Una matrice può essere inizializzata quando viene dichiarata:


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



In caso contrario, il tipo di matrice può essere usato per creare le stesse dichiarazioni:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



Il tipo matrice usa le parentesi angolari per specificare il tipo, il numero di righe e il numero di colonne. Questo esempio crea una matrice a virgola mobile, con due righe e due colonne. È possibile usare qualsiasi tipo di dati scalare.

Questa dichiarazione definisce una matrice di valori float (numeri a virgola mobile a 32 bit) con due righe e tre colonne:


```
matrix <float, 2, 3> fFloatMatrix;
```



Una matrice contiene valori organizzati in righe e colonne, a cui è possibile accedere usando l'operatore di struttura "." seguito da uno dei due set di denominazione seguenti:

-   Posizione della colonna di riga in base zero:
    -   \_m00, \_ m01, \_ m02, \_ m03
    -   \_m10, \_ m11, \_ m12, \_ m13
    -   \_m20, \_ m21, \_ m22, \_ m23
    -   \_m30, \_ m31, \_ m32, \_ m33
-   Posizione della colonna di riga in base uno:
    -   \_11, \_ 12, \_ 13, \_ 14
    -   \_21, \_ 22, \_ 23, \_ 24
    -   \_31, \_ 32, \_ 33, \_ 34
    -   \_41, \_ 42, \_ 43, \_ 44

Ogni set di denominazione inizia con un carattere di sottolineatura seguito dal numero di riga e dal numero di colonna. La convenzione in base zero include anche la lettera "m" prima del numero di riga e colonna. Ecco un esempio che usa i due set di denominazione per accedere a una matrice:


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



Analogamente ai vettori, i set di denominazione possono usare uno o più componenti di entrambi i set di denominazione.


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



È anche possibile accedere a una matrice usando la notazione di accesso alla matrice, ovvero un set di indici in base zero. Ogni indice è racchiuso tra parentesi quadre. È possibile accedere a una matrice 4x4 con gli indici seguenti:

-   \[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]
-   \[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]
-   \[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] , \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]
-   \[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]

Di seguito è riportato un esempio di accesso a una matrice:


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



Si noti che l'operatore di struttura "." non viene usato per accedere a una matrice. La notazione di accesso alle matrici non può usare lo swizzling per leggere più di un componente.


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



Tuttavia, l'accesso alle matrici può leggere un vettore a più componenti.


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



Come per i vettori, la lettura di più componenti della matrice è detta swizzling. È possibile assegnare più componenti, presupponendo che sia usato un solo spazio dei nomi. Queste sono tutte assegnazioni valide:


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



La maschera controlla il numero di componenti scritti.


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



Le assegnazioni non possono essere scritte nello stesso componente più di una volta. Il lato sinistro di questa istruzione non è quindi valido:


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



Inoltre, gli spazi dei nomi dei componenti non possono essere misti. Si tratta di un componente non valido:


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a>Ordinamento delle matrici

Per impostazione predefinita, l'ordine di tabulazione della matrice per i parametri uniformi è impostato su column-major. Ciò significa che ogni colonna della matrice viene archiviata in un unico registro costante. D'altra parte, una matrice row-major racchiude ogni riga della matrice in un unico registro costante. La creazione di una matrice può essere modificata con la **\# direttiva pragmapack \_ matrix** o con la parola chiave **row \_ major** o **column \_ major.**

I dati in una matrice vengono caricati nei registri costanti dello shader prima dell'esecuzione di uno shader. Esistono due opzioni per la modalità di lettura dei dati della matrice: nell'ordine delle righe principali o nell'ordine delle colonne principali. L'ordine delle colonne principali indica che ogni colonna della matrice verrà archiviata in un singolo registro costante e l'ordine delle righe principali indica che ogni riga della matrice verrà archiviata in un unico registro costante. Si tratta di una considerazione importante per il numero di registri costanti usati per una matrice.

Una matrice principale di riga è strutturata come la seguente:

:::row:::
    :::column:::
        11<br/>
        21<br/>
        31<br/>
        41<br/>
    :::column-end:::
    :::column:::
        12<br/>
        22<br/>
        32<br/>
        42<br/>
    :::column-end:::
    :::column:::
        13<br/>
        23<br/>
        33<br/>
        43<br/>
    :::column-end:::
    :::column:::
        14<br/>
        24<br/>
        34<br/>
        44<br/>
    :::column-end:::
:::row-end:::




 

Una matrice di colonne principali è strutturata come segue:


:::row:::
    :::column:::
        11<br/>
        12<br/>
        13<br/>
        14<br/>
    :::column-end:::
    :::column:::
        21<br/>
        22<br/>
        23<br/>
        24<br/>
    :::column-end:::
    :::column:::
        31<br/>
        32<br/>
        33<br/>
        34<br/>
    :::column-end:::
    :::column:::
        41<br/>
        42<br/>
        43<br/>
        44<br/>
    :::column-end:::
:::row-end:::




 

L'ordinamento delle matrici row-major e column-major determina l'ordine in cui i componenti della matrice vengono letti dagli input shader. Dopo che i dati sono stati scritti in registri costanti, l'ordine delle matrici non ha alcun effetto sul modo in cui i dati vengono usati o accessibili dall'interno del codice shader. Inoltre, le matrici dichiarate in un corpo dello shader non vengono imballate in registri costanti. L'ordine di tabulazione delle righe principali e delle colonne non influisce sull'ordine di creazione dei costruttori (che segue sempre l'ordinamento principale delle righe).

L'ordine dei dati in una matrice può essere dichiarato in fase di compilazione oppure il compilatore ordina i dati in fase di esecuzione per un uso più efficiente.

## <a name="examples"></a>Esempio

HLSL usa due tipi speciali, un tipo vettore e un tipo matrice per semplificare la programmazione della grafica 2D e 3D. Ognuno di questi tipi contiene più di un componente. un vettore contiene fino a quattro componenti e una matrice contiene fino a 16 componenti. Quando vettori e matrici vengono usati nelle equazioni HLSL standard, la matematica eseguita è progettata per funzionare per componente. Ad esempio, HLSL implementa questa moltiplicazione:


```
float4 v = a*b;
```



come moltiplicazione a quattro componenti. Il risultato è quattro scalari:


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



Si tratta di quattro moltiplicazioni in cui ogni risultato viene archiviato in un componente separato di v. Si tratta di una moltiplicazione a quattro componenti. HLSL usa componenti matematici che rendono molto efficiente la scrittura di shader.

Questo è molto diverso da una moltiplicazione che viene in genere implementata come un prodotto punto che genera un singolo scalare:


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



Una matrice usa anche operazioni per componente in HLSL:


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



Il risultato è una moltiplicazione per componente delle due matrici (anziché una moltiplicazione standard di matrice 3x3). La moltiplicazione di una matrice per componente restituisce il primo termine:


```
mat3.m00 = mat1.m00 * mat2._m00;
```



Questa operazione è diversa da una moltiplicazione di matrice 3x3 che restituisce questo primo termine:


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



Le versioni di overload della funzione intrinseca multiply gestiscono i casi in cui un operando è un vettore e l'altro operando è una matrice. Ad esempio: \* vettore vettoriale, \* matrice vettoriale, \* vettore matrice e matrice \* matrice. Ad esempio:


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



produce lo stesso risultato di :


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



Questo esempio esegue il cast del vettore pos a un vettore di colonna usando il cast (float1x4). La modifica di un vettore tramite cast o lo scambio dell'ordine degli argomenti forniti per la moltiplicazione equivale a trasposizione della matrice.

La conversione cast automatica fa sì che le funzioni intrinseche multiply e dot restituiranno gli stessi risultati usati qui:


```
{
  float4 val;
  return mul(val,val);
}
```



Questo risultato della moltiplicazione è un vettore 1x4 \* 4x1 = 1x1. Equivale a un prodotto punto:


```
{
  float4 val;
  return dot(val,val);
}
```



che restituisce un singolo valore scalare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




