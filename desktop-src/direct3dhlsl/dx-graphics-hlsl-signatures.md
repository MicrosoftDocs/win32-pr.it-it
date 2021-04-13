---
title: Firme
description: Una firma shader è un elenco dei parametri che sono input o output di una funzione shader.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992856"
---
# <a name="signatures"></a><span data-ttu-id="6e931-103">Firme</span><span class="sxs-lookup"><span data-stu-id="6e931-103">Signatures</span></span>

<span data-ttu-id="6e931-104">Una firma shader è un elenco dei parametri che sono input o output di una funzione shader.</span><span class="sxs-lookup"><span data-stu-id="6e931-104">A shader signature is a list of the parameters that are either input to or output from a shader function.</span></span> <span data-ttu-id="6e931-105">In Direct3D 10, le fasi adiacenti condividono efficacemente una matrice di registri, in cui lo shader di output (o la fase della pipeline) scrive i dati in percorsi specifici nella matrice di registro e lo shader di input deve leggere dalle stesse posizioni.</span><span class="sxs-lookup"><span data-stu-id="6e931-105">In Direct3D 10, adjacent stages effectively share a register array, where the output shader (or pipeline stage) writes data to specific locations in the register array and the input shader must read from the same locations.</span></span> <span data-ttu-id="6e931-106">L'API usa le firme shader per associare gli output dello shader con gli input senza l'overhead della risoluzione semantica.</span><span class="sxs-lookup"><span data-stu-id="6e931-106">The API uses shader signatures to bind shader outputs with inputs without the overhead of semantic resolution.</span></span>

<span data-ttu-id="6e931-107">In Direct3D 10, le firme di input vengono generate da una dichiarazione di input shader e la firma di output viene generata da una dichiarazione shader-output.</span><span class="sxs-lookup"><span data-stu-id="6e931-107">In Direct3D 10, input signatures are generated from a shader-input declaration and the output signature is generated from a shader-output declaration.</span></span> <span data-ttu-id="6e931-108">Una firma di input è detta compatibilità con una firma di output quando la firma di output è un subset rigoroso (tipo di argomento e corrispondenza dell'ordine) della firma di input.</span><span class="sxs-lookup"><span data-stu-id="6e931-108">An input signature is said to be compatible with an output signature when the output signature is a strict subset (argument type and order match) of the input signature.</span></span> <span data-ttu-id="6e931-109">Il modo più semplice per ottenere questo risultato consiste nel collegare gli input e gli output dello shader corrispondenti allo stesso tipo di struttura.</span><span class="sxs-lookup"><span data-stu-id="6e931-109">The most straightforward way to achieve this is to link corresponding shader inputs and outputs by the same structure type.</span></span>

<span data-ttu-id="6e931-110">Di seguito è riportato un esempio di firme compatibili.</span><span class="sxs-lookup"><span data-stu-id="6e931-110">Here is an example of compatible signatures.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



<span data-ttu-id="6e931-111">Di seguito è riportato un esempio di firme incompatibili. l'ordine dei parametri nella firma di input non corrisponde a quello nella firma di output.</span><span class="sxs-lookup"><span data-stu-id="6e931-111">Here is an example of incompatible signatures; the order of parameters in the input signature does not match the order in the output signature.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



<span data-ttu-id="6e931-112">PSInWorks è un subset compatibile di VSOut (le prime due voci corrispondono sia al tipo sia all'ordine con le prime due voci in VSOut).</span><span class="sxs-lookup"><span data-stu-id="6e931-112">PSInWorks is a compatible subset of VSOut (the first two entries match both type and order with the first two entries in VSOut).</span></span> <span data-ttu-id="6e931-113">Tuttavia, PSInFails è incompatibile perché l'ordinamento non corrisponde a VSOut.</span><span class="sxs-lookup"><span data-stu-id="6e931-113">However, PSInFails is incompatible because the ordering does not match with VSOut.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e931-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e931-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e931-115">Funzioni</span><span class="sxs-lookup"><span data-stu-id="6e931-115">Functions</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




