---
title: Firme
description: Una firma shader è un elenco dei parametri che sono input o output da una funzione shader.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5631dbe473b2e3eea0abb525e58621faf9c5137dd5dc3d743bde53b0ae258f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789581"
---
# <a name="signatures"></a>Firme

Una firma shader è un elenco dei parametri che sono input o output da una funzione shader. In Direct3D 10 le fasi adiacenti condividono in modo efficace una matrice di registri, in cui lo shader di output (o fase della pipeline) scrive i dati in posizioni specifiche nella matrice di registro e lo shader di input deve leggere dalle stesse posizioni. L'API usa le firme shader per associare gli output dello shader agli input senza l'overhead della risoluzione semantica.

In Direct3D 10 le firme di input vengono generate da una dichiarazione di input shader e la firma di output viene generata da una dichiarazione di output shader. Una firma di input viene detto compatibile con una firma di output quando la firma di output è un subset rigoroso (tipo di argomento e corrispondenza dell'ordine) della firma di input. Il modo più semplice per ottenere questo risultato è collegare gli input e gli output dello shader corrispondenti dallo stesso tipo di struttura.

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



Di seguito è riportato un esempio di firme incompatibili. L'ordine dei parametri nella firma di input non corrisponde all'ordine nella firma di output.


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



PSInWorks è un subset compatibile di VSOut (le prime due voci corrispondono sia al tipo che all'ordine con le prime due voci in VSOut). PSInFails è tuttavia incompatibile perché l'ordinamento non corrisponde a VSOut.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




