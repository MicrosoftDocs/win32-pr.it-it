---
title: Regole di packing per le variabili costanti
description: Le regole di packing determinano la modalità di disposta dei dati quando vengono archiviati.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49b10f6383344821c7659ac40b367a77e0421d33be68a374c59920a62d37697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120085"
---
# <a name="packing-rules-for-constant-variables"></a>Regole di packing per le variabili costanti

Le regole di packing determinano la modalità di disposta dei dati quando vengono archiviati. HLSL implementa le regole di pacchetto per i dati di output di Visual Studio, i dati di input e output di GS e i dati di input e output PS. I dati non sono compressi per gli input di Visual Studio perché la fase IA non può decomprimere i dati.

Le regole di pacchetto HLSL sono simili all'esecuzione di un **\# pragma pack 4** con Visual Studio, che racchiude i dati in limiti a 4 byte. Inoltre, HLSL esegue il pack dei dati in modo che non attraversi un limite di 16 byte. Le variabili vengono suddivise in un determinato vettore a quattro componenti fino a quando la variabile non si eserciterà su un limite a 4 vettori. le variabili seguenti verranno restituite al vettore a quattro componenti successivo.

Ogni struttura forza l'avvio della variabile successiva sul vettore a quattro componenti successivo. In alcuni casi viene generata la spaziatura interna per le matrici di strutture. Le dimensioni risultanti di qualsiasi struttura saranno sempre divisibile in modo uniforme in base **a sizeof**(*vettore a quattro componenti*).

Le matrici non vengono imballate in HLSL per impostazione predefinita. Per evitare di forzare l'overhead ALU dello shader per i calcoli di offset, ogni elemento di una matrice viene archiviato in un vettore a quattro componenti. Si noti che è possibile ottenere la creazione di un pacchetto per le matrici (e incorrere nei calcoli di indirizzamento) usando il cast.

Di seguito sono riportati esempi di strutture e delle dimensioni compresse corrispondenti (dato che un **valore float1** occupa 4 byte):


```
//  2 x 16byte elements
cbuffer IE
{
    float4 Val1;
    float2 Val2;  // starts a new vector
    float2 Val3;
};

//  3 x 16byte elements
cbuffer IE
{
    float2 Val1;
    float4 Val2;  // starts a new vector
    float2 Val3;  // starts a new vector
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val2;
    float2 Val3;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float2 Val2;
    float1 Val3;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float1 Val1;
    float2 Val2;    // starts a new vector
};


//  1 x 16byte elements
cbuffer IE
{
    float3 Val1;
    float1 Val2;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float3 Val2;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float3 Val2;        // starts a new vector
};


// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;

    struct     {
        float4 SVal1;    // starts a new vector
        float1 SVal2;    // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;  
    struct     {
        float1 SVal1;     // starts a new vector
        float4 SVal2;     // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    struct     {
        float4 SVal1;
        float1 SVal2;    // starts a new vector
    } Val1;

    float1 Val2; 
};
```



## <a name="more-aggressive-packing"></a>Creazione di un pacchetto più aggressivo

È possibile creare un pacchetto di una matrice in modo più aggressivo. Ad esempio, data una matrice di variabili float:


```
float4 array[16];
```



È possibile scegliere di creare un pacchetto simile al seguente, senza spazi nella matrice:


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



La compattazione più stretta è un compromesso rispetto alla necessità di istruzioni shader aggiuntive per il calcolo degli indirizzi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




