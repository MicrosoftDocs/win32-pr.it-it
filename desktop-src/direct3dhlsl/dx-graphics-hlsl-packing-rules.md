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
# <a name="packing-rules-for-constant-variables"></a><span data-ttu-id="3e5dd-103">Regole di compressione per variabili costanti</span><span class="sxs-lookup"><span data-stu-id="3e5dd-103">Packing Rules for Constant Variables</span></span>

<span data-ttu-id="3e5dd-104">Le regole di compressione stabiliscono il modo in cui i dati possono essere disposti quando vengono archiviati.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-104">Packing rules dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="3e5dd-105">HLSL implementa le regole di compressione per i dati di output di Visual Studio, i dati di input e output GS e i dati di input e output di PS.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-105">HLSL implements packing rules for VS output data, GS input and output data, and PS input and output data.</span></span> <span data-ttu-id="3e5dd-106">I dati non vengono compressi per gli input VS perché la fase IA non può decomprimere i dati.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-106">(Data is not packed for VS inputs because the IA stage cannot unpack data.)</span></span>

<span data-ttu-id="3e5dd-107">Le regole di compressione di HLSL sono simili all'esecuzione di un **\# pragma pack 4** con Visual Studio, che consente di impacchettare i dati in limiti di 4 byte.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-107">HLSL packing rules are similar to performing a **\#pragma pack 4** with Visual Studio, which packs data into 4-byte boundaries.</span></span> <span data-ttu-id="3e5dd-108">Inoltre, HLSL comprime i dati in modo che non superino un limite di 16 byte.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-108">Additionally, HLSL packs data so that it does not cross a 16-byte boundary.</span></span> <span data-ttu-id="3e5dd-109">Le variabili vengono compresse in un vettore a quattro componenti specificato fino a quando la variabile non sarà a cavalcioni di un limite di 4 vettori; le variabili successive verranno rimbalzate sul vettore a quattro componenti successivo.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-109">Variables are packed into a given four-component vector until the variable will straddle a 4-vector boundary; the next variables will be bounced to the next four-component vector.</span></span>

<span data-ttu-id="3e5dd-110">Ogni struttura impone che la variabile successiva venga avviata sul vettore successivo a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-110">Each structure forces the next variable to start on the next four-component vector.</span></span> <span data-ttu-id="3e5dd-111">Questa operazione genera talvolta la spaziatura interna per le matrici di strutture.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-111">This sometimes generates padding for arrays of structures.</span></span> <span data-ttu-id="3e5dd-112">Le dimensioni risultanti di qualsiasi struttura sono sempre divisibili in modo uniforme per **sizeof**(*vettore a quattro componenti*).</span><span class="sxs-lookup"><span data-stu-id="3e5dd-112">The resulting size of any structure will always be evenly divisible by **sizeof**(*four-component vector*).</span></span>

<span data-ttu-id="3e5dd-113">Per impostazione predefinita, le matrici non vengono compresse in HLSL.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-113">Arrays are not packed in HLSL by default.</span></span> <span data-ttu-id="3e5dd-114">Per evitare di forzare lo shader a eseguire un sovraccarico ALU per i calcoli di offset, ogni elemento in una matrice viene archiviato in un vettore a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-114">To avoid forcing the shader to take on ALU overhead for offset computations, every element in an array is stored in a four-component vector.</span></span> <span data-ttu-id="3e5dd-115">Si noti che è possibile ottenere la compressione per le matrici (e incorrere nei calcoli di indirizzamento) usando il cast.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-115">Note that you can achieve packing for arrays (and incur the addressing calculations) by using casting.</span></span>

<span data-ttu-id="3e5dd-116">Di seguito sono riportati alcuni esempi di strutture e le relative dimensioni compresse corrispondenti (dato: un **float1** occupa 4 byte):</span><span class="sxs-lookup"><span data-stu-id="3e5dd-116">Following are examples of structures and their corresponding packed sizes (given: a **float1** occupies 4 bytes):</span></span>


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



## <a name="more-aggressive-packing"></a><span data-ttu-id="3e5dd-117">Compressione più aggressiva</span><span class="sxs-lookup"><span data-stu-id="3e5dd-117">More Aggressive Packing</span></span>

<span data-ttu-id="3e5dd-118">È possibile comprimere una matrice in modo più aggressivo.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-118">You could pack an array more aggressively.</span></span> <span data-ttu-id="3e5dd-119">Ad esempio, data una matrice di variabili float:</span><span class="sxs-lookup"><span data-stu-id="3e5dd-119">For instance, given an array of float variables:</span></span>


```
float4 array[16];
```



<span data-ttu-id="3e5dd-120">È possibile scegliere di comprimere il pacchetto in modo analogo al seguente, senza spazi nella matrice:</span><span class="sxs-lookup"><span data-stu-id="3e5dd-120">You could choose to pack it like this, without any spaces in the array:</span></span>


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



<span data-ttu-id="3e5dd-121">La compressione più stretta è un compromesso rispetto alla necessità di istruzioni aggiuntive dello shader per il calcolo degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="3e5dd-121">The tighter packing is a trade off versus the need for additional shader instructions for address computation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e5dd-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3e5dd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e5dd-123">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="3e5dd-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




