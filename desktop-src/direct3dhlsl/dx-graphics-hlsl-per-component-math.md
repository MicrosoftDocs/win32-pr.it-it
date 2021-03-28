---
title: Operazioni matematiche Per-Component
description: Con HLSL è possibile programmare gli shader a livello di algoritmo.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ff30cd19b7821c9a059251e105f6acfa9cf961e
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/17/2021
ms.locfileid: "104982819"
---
# <a name="per-component-math-operations"></a>Operazioni matematiche Per-Component

Con HLSL è possibile programmare gli shader a livello di algoritmo. Per comprendere il linguaggio, è necessario sapere come dichiarare variabili e funzioni, usare funzioni intrinseche, definire tipi di dati personalizzati e usare la semantica per connettere gli argomenti dello shader ad altri shader e alla pipeline.

Dopo aver apprendere come creare shader in HLSL, è necessario ottenere informazioni sulle chiamate API, in modo da poter compilare uno shader per hardware specifico, inizializzare costanti shader e inizializzare altro stato della pipeline, se necessario.

-   [Tipo di vettore](#the-vector-type)
-   [Tipo matrice](#the-matrix-type)
    -   [Ordinamento matrice](#matrix-ordering)
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



Il valore integer che segue immediatamente il tipo di dati è il numero di componenti sul vettore.

Gli inizializzatori possono anche essere inclusi nelle dichiarazioni.


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



In alternativa, è possibile usare il tipo di vettore per creare le stesse dichiarazioni:


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Il tipo Vector usa le parentesi angolari per specificare il tipo e il numero di componenti.

I vettori contengono fino a quattro componenti, a ognuno dei quali è possibile accedere utilizzando uno dei due set di denominazione seguenti:

-   Il set di posizioni: x, y, z, w
-   Set di colori: r, g, b, a

Entrambe le istruzioni restituiscono il valore nel terzo componente.


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



La specifica di uno o più componenti vettoriali durante la lettura dei componenti è denominata swizzling. Ad esempio:


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



Il mascheramento controlla il numero di componenti scritti.


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



Le assegnazioni non possono essere scritte nello stesso componente più di una volta. Quindi, il lato sinistro di questa istruzione non è valido:


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



Inoltre, gli spazi dei nomi di componente non possono essere misti. La scrittura di un componente non è valida:


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



L'accesso a un vettore come scalare può accedere al primo componente del vettore. Le due istruzioni seguenti sono equivalenti.


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>Tipo matrice

Una matrice è una struttura di dati che contiene righe e colonne di dati. I dati possono essere qualsiasi tipo di dati scalari, tuttavia, ogni elemento di una matrice è dello stesso tipo di dati. Il numero di righe e colonne viene specificato con la stringa riga per colonna aggiunta al tipo di dati.


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



In alternativa, il tipo di matrice può essere usato per creare le stesse dichiarazioni:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



Il tipo di matrice utilizza le parentesi acute per specificare il tipo, il numero di righe e il numero di colonne. In questo esempio viene creata una matrice a virgola mobile, con due righe e due colonne. È possibile utilizzare qualsiasi tipo di dati scalari.

Questa dichiarazione definisce una matrice di valori float (numeri a virgola mobile a 32 bit) con due righe e tre colonne:


```
matrix <float, 2, 3> fFloatMatrix;
```



Una matrice contiene valori organizzati in righe e colonne, a cui è possibile accedere utilizzando l'operatore di struttura "." seguito da uno dei due set di denominazione seguenti:

-   Posizione in base zero della colonna di riga:
    -   \_M00, \_ M01, \_ M02, \_ M03
    -   \_M10, \_ M11, \_ M12, \_ M13
    -   \_M20, \_ M21, \_ M22, \_ M23
    -   \_M30, \_ M31, \_ M32, \_ M33
-   Posizione della colonna di riga in base 1:
    -   \_11, \_ 12, \_ 13, \_ 14
    -   \_21, \_ 22, \_ 23, \_ 24
    -   \_31, \_ 32, \_ 33, \_ 34
    -   \_41, \_ 42, \_ 43, \_ 44

Ogni set di denominazione inizia con un carattere di sottolineatura seguito dal numero di riga e dal numero di colonna. La convenzione in base zero include anche la lettera "m" prima del numero di riga e colonna. Di seguito è riportato un esempio che usa i due set di denominazione per accedere a una matrice:


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



Analogamente ai vettori, i set di denominazione possono usare uno o più componenti da uno dei due set di denominazione.


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



È possibile accedere a una matrice anche usando la notazione di accesso alla matrice, ovvero un set di indici in base zero. Ogni indice è racchiuso tra parentesi quadre. È possibile accedere a una matrice 4x4 con gli indici seguenti:

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



Si noti che l'operatore di struttura "." non viene usato per accedere a una matrice. La notazione di accesso alla matrice non può utilizzare swizzling per leggere più di un componente.


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



Tuttavia, l'accesso alla matrice può leggere un vettore a più componenti.


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



Come per i vettori, la lettura di più di un componente della matrice è denominata swizzling. È possibile assegnare più di un componente, supponendo che venga utilizzato un solo spazio dei nomi. Tutte le assegnazioni valide sono:


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



Il mascheramento controlla il numero di componenti scritti.


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



Le assegnazioni non possono essere scritte nello stesso componente più di una volta. Quindi, il lato sinistro di questa istruzione non è valido:


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



Inoltre, gli spazi dei nomi di componente non possono essere misti. La scrittura di un componente non è valida:


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a>Ordinamento matrice

Per impostazione predefinita, l'ordine di compressione della matrice per i parametri uniformi è impostato su column-major. Ciò significa che ogni colonna della matrice viene archiviata in un unico registro costante. D'altra parte, una matrice di righe-principali imballa ogni riga della matrice in un unico registro costante. La compressione della matrice può essere modificata con la direttiva **\# pragmapack \_ Matrix** oppure con la parola chiave Major della **riga \_** o con la parola chiave **\_ Major della colonna** .

I dati di una matrice vengono caricati in registri costanti dello shader prima dell'esecuzione di uno shader. Sono disponibili due opzioni per il modo in cui vengono letti i dati della matrice, in ordine di riga o in ordine principale. Per ordine di colonna si intende che ogni colonna della matrice verrà archiviata in un unico registro costante e l'ordine delle righe significa che ogni riga della matrice verrà archiviata in un unico registro costante. Si tratta di una considerazione importante per il numero di registri costanti utilizzati per una matrice.

Una matrice riga-principale è configurata come la seguente:



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 12  | 13  | 14  |
| 21  | 22  | 23  | 24  |
| 31  | 32  | 33  | 34  |
| 41  | 42  | 43  | 44  |



 

Una matrice column-major è configurata come la seguente:



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 21  | 31  | 41  |
| 12  | 22  | 32  | 42  |
| 13  | 23  | 33  | 43  |
| 14  | 24  | 34  | 44  |



 

Ordine delle matrici row-major e column-major determinare l'ordine in cui i componenti della matrice vengono letti dagli input dello shader. Una volta scritti i dati in registri costanti, l'ordine della matrice non influisce sul modo in cui i dati vengono utilizzati o a cui si accede dal codice dello shader. Inoltre, le matrici dichiarate in un corpo dello shader non vengono compresse in registri costanti. L'ordine di compressione delle righe e delle colonne principali non ha alcun effetto sull'ordine di compressione dei costruttori (che segue sempre l'ordinamento della riga principale).

L'ordine dei dati in una matrice può essere dichiarato in fase di compilazione oppure il compilatore Ordina i dati in fase di esecuzione per un uso più efficiente.

## <a name="examples"></a>Esempio

HLSL usa due tipi speciali, un tipo di vettore e un tipo matrice per semplificare la programmazione di grafica 2D e 3D. Ognuno di questi tipi contiene più di un componente. un vettore contiene fino a quattro componenti e una matrice contiene fino a 16 componenti. Quando i vettori e le matrici vengono usati nelle equazioni HLSL standard, la matematica eseguita è progettata per funzionare per ogni componente. Ad esempio, HLSL implementa questa operazione Multiply:


```
float4 v = a*b;
```



come moltiplicatore a quattro componenti. Il risultato è quattro scalari:


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



Si tratta di quattro moltiplicazioni in cui ogni risultato viene archiviato in un componente separato di v. Si tratta di una moltiplicazione a quattro componenti. HLSL usa la matematica dei componenti che rende molto efficiente la scrittura degli shader.

Si tratta di un'operazione molto diversa da una moltiplicazione, che viene in genere implementata come prodotto a virgola, che genera un singolo scalare:


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



Una matrice USA anche operazioni per componente in HLSL:


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



Il risultato è un moltiplicatore per componente delle due matrici (in contrapposizione a una matrice standard 3x3). Un moltiplicatore di matrice per componente produce il primo termine:


```
mat3.m00 = mat1.m00 * mat2._m00;
```



Si tratta di una differenza rispetto a una matrice 3x3 che produrrebbe il primo termine:


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



Le versioni di overload della funzione intrinseca Multiply gestiscono i casi in cui un operando è un vettore e l'altro operando è una matrice. Ad esempio: Vector Vector \* , vector \* Matrix, Matrix \* Vector e Matrix Matrix \* . Ad esempio:


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



produce lo stesso risultato di:


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



Questo esempio esegue il cast del vettore POS a un vettore di colonna usando il cast (float1x4). La modifica di un vettore mediante il cast o lo scambio dell'ordine degli argomenti forniti a Multiply equivale alla trasposizione della matrice.

La conversione del cast automatico fa in modo che le funzioni intrinseche Multiply e dot restituiscano gli stessi risultati usati in questo esempio:


```
{
  float4 val;
  return mul(val,val);
}
```



Questo risultato della moltiplicazione è un \* vettore 4 4x1 = 1x1. Equivale a un prodotto a virgola:


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

 

 




