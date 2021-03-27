---
title: Regole di compressione per variabili costanti
description: Le regole di compressione stabiliscono il modo in cui i dati possono essere disposti quando vengono archiviati.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d85566083dc9ead93a1a9e73fb06051b62178114
ms.sourcegitcommit: 004d7881dc9ff92ea394cd2331774e13b1e7f13c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/12/2020
ms.locfileid: "103724367"
---
# <a name="packing-rules-for-constant-variables"></a>Regole di compressione per variabili costanti

Le regole di compressione stabiliscono il modo in cui i dati possono essere disposti quando vengono archiviati. HLSL implementa le regole di compressione per i dati di output di Visual Studio, i dati di input e output GS e i dati di input e output di PS. I dati non vengono compressi per gli input VS perché la fase IA non può decomprimere i dati.

Le regole di compressione di HLSL sono simili all'esecuzione di un **\# pragma pack 4** con Visual Studio, che consente di impacchettare i dati in limiti di 4 byte. Inoltre, HLSL comprime i dati in modo che non superino un limite di 16 byte. Le variabili vengono compresse in un vettore a quattro componenti specificato fino a quando la variabile non sarà a cavalcioni di un limite di 4 vettori; le variabili successive verranno rimbalzate sul vettore a quattro componenti successivo.

Ogni struttura impone che la variabile successiva venga avviata sul vettore successivo a quattro componenti. Questa operazione genera talvolta la spaziatura interna per le matrici di strutture. Le dimensioni risultanti di qualsiasi struttura sono sempre divisibili in modo uniforme per **sizeof**(*vettore a quattro componenti*).

Per impostazione predefinita, le matrici non vengono compresse in HLSL. Per evitare di forzare lo shader a eseguire un sovraccarico ALU per i calcoli di offset, ogni elemento in una matrice viene archiviato in un vettore a quattro componenti. Si noti che è possibile ottenere la compressione per le matrici (e incorrere nei calcoli di indirizzamento) usando il cast.

Di seguito sono riportati alcuni esempi di strutture e le relative dimensioni compresse corrispondenti (dato: un **float1** occupa 4 byte):


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



## <a name="more-aggressive-packing"></a>Compressione più aggressiva

È possibile comprimere una matrice in modo più aggressivo. Ad esempio, data una matrice di variabili float:


```
float4 array[16];
```



È possibile scegliere di comprimere il pacchetto in modo analogo al seguente, senza spazi nella matrice:


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



La compressione più stretta è un compromesso rispetto alla necessità di istruzioni aggiuntive dello shader per il calcolo degli indirizzi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




