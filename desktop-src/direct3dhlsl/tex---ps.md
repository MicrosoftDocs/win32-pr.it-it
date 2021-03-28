---
title: Tex-PS
description: Carica il registro di destinazione con i dati di colore (RGBA) campionati da una trama. La trama deve essere associata a una fase di trama particolare (n) utilizzando la texture. Il campionamento della trama è controllato da SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963238"
---
# <a name="tex---ps"></a>Tex-PS

Carica il registro di destinazione con i dati di colore (RGBA) campionati da una trama. La trama deve essere associata a una fase di trama particolare (n) [**utilizzando la texture.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Il campionamento della trama è controllato da [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).

## <a name="syntax"></a>Sintassi



| ora di Tex |
|---------|



 

dove

-   DST è il registro di destinazione.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Tex                   | x    | x    | x    |      |      |      |       |      |       |



 

Il numero del registro di destinazione specifica il numero della fase della trama.

Il campionamento di trama usa coordinate di trama per cercare o campionare un valore di colore in corrispondenza delle coordinate specificate (u, v, w, q) tenendo conto degli attributi dello stato della fase della trama.

I dati delle coordinate di trama vengono interpolati dai dati delle coordinate di trama dei vertici ed è associato a una fase di trama specifica. L'associazione predefinita è un mapping uno-a-uno tra il numero di fase della trama e l'ordine di dichiarazione delle coordinate di trama. Ciò significa che per impostazione predefinita, il primo set di coordinate di trama definito nel formato Vertex è associato alla fase 0 della trama.

Le coordinate di trama possono essere associate a qualsiasi fase usando due tecniche. Quando si usa un vertex shader della funzione fissa o la pipeline della funzione fissa, il flag di stato della fase \_ di trama TEXCOORDINDEX può essere usato in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) per associare le coordinate a una fase. In caso contrario, le coordinate di trama vengono restituite dai registri vertex shader oTn quando si usa un vertex shader programmabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 