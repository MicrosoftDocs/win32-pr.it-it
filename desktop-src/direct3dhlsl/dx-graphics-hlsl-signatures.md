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
# <a name="signatures"></a>Firme

Una firma shader è un elenco dei parametri che sono input o output di una funzione shader. In Direct3D 10, le fasi adiacenti condividono efficacemente una matrice di registri, in cui lo shader di output (o la fase della pipeline) scrive i dati in percorsi specifici nella matrice di registro e lo shader di input deve leggere dalle stesse posizioni. L'API usa le firme shader per associare gli output dello shader con gli input senza l'overhead della risoluzione semantica.

In Direct3D 10, le firme di input vengono generate da una dichiarazione di input shader e la firma di output viene generata da una dichiarazione shader-output. Una firma di input è detta compatibilità con una firma di output quando la firma di output è un subset rigoroso (tipo di argomento e corrispondenza dell'ordine) della firma di input. Il modo più semplice per ottenere questo risultato consiste nel collegare gli input e gli output dello shader corrispondenti allo stesso tipo di struttura.

Di seguito è riportato un esempio di firme compatibili.


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



Di seguito è riportato un esempio di firme incompatibili. l'ordine dei parametri nella firma di input non corrisponde a quello nella firma di output.


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



PSInWorks è un subset compatibile di VSOut (le prime due voci corrispondono sia al tipo sia all'ordine con le prime due voci in VSOut). Tuttavia, PSInFails è incompatibile perché l'ordinamento non corrisponde a VSOut.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




