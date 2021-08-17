---
title: tex - ps
description: Carica il registro di destinazione con i dati di colore (RGBA) campionati da una trama. La trama deve essere associata a una particolare fase della trama (n) usando SetTexture. Il campionamento delle trame è controllato da SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0646a057fdc2fb96e5f72e7451b9b273191ced22f5092a14fab11a9042c5de25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788110"
---
# <a name="tex---ps"></a>tex - ps

Carica il registro di destinazione con i dati di colore (RGBA) campionati da una trama. La trama deve essere associata a una particolare fase della trama (n) usando [**SetTexture.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Il campionamento delle trame è controllato [**da SetSamplerState.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)

## <a name="syntax"></a>Sintassi



| tex dst |
|---------|



 

dove

-   dst è il registro di destinazione.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Tex                   | x    | x    | x    |      |      |      |       |      |       |



 

Il numero del registro di destinazione specifica il numero della fase della trama.

Il campionamento trame usa le coordinate della trama per cercare, o campionare, un valore di colore in corrispondenza delle coordinate specificate (u,v,w,q) tenendo conto degli attributi dello stato della fase della trama.

I dati delle coordinate della trama vengono interpolati dai dati delle coordinate della trama dei vertici ed è associato a una fase di trama specifica. L'associazione predefinita è un mapping uno-a-uno tra il numero della fase della trama e l'ordine di dichiarazione delle coordinate della trama. Ciò significa che il primo set di coordinate di trama definite nel formato vertice è associato per impostazione predefinita alla fase di trama 0.

Le coordinate della trama possono essere associate a qualsiasi fase usando due tecniche. Quando si usa un vertex shader a funzione fissa o la pipeline di funzioni fisse, il flag di stato della fase della trama TSS TEXCOORDINDEX può essere usato \_ in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) per associare le coordinate a una fase. In caso contrario, le coordinate della trama vengono restituite dai registri oTn del vertex shader quando si usa un vertex shader programmabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 