---
description: Flag di funzionalità degli stencil del driver.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343056"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Flag di funzionalità stencil del driver.



| \#Definire                 | Valore       | Descrizione                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| D3DSTENCILCAPS \_ KEEP     | 0x00000001L | Non aggiornare la voce nel buffer degli stencil. Si tratta del valore predefinito.                             |
| D3DSTENCILCAPS \_ ZERO     | 0x00000002L | Impostare la voce stencil-buffer su 0.                                                                    |
| D3DSTENCILCAPS \_ REPLACE  | 0x00000004L | Sostituire la voce stencil-buffer con il valore di riferimento.                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | Incrementare la voce stencil-buffer, fissando al valore massimo.                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | Decrementare la voce stencil-buffer, fissando a zero.                                                 |
| D3DSTENCILCAPS \_ INVERT   | 0x00000020L | Invertire i bit nella voce stencil-buffer.                                                          |
| D3DSTENCILCAPS \_ INCR     | 0x00000040L | Incrementare la voce dello stencil buffer, a capo su zero se il nuovo valore supera il valore massimo.      |
| D3DSTENCILCAPS \_ DECR     | 0x00000080L | Decrementare la voce dello stencil buffer, a capo del valore massimo se il nuovo valore è minore di zero. |
| D3DSTENCILCAPS \_ A DUE LATI | 0x00000100L | Il dispositivo supporta lo stencil a due lati.                                                                |



 

Le voci dello stencil buffer sono valori interi compresi tra 0 e 2ⁿ - 1, dove n è la profondità in bit del buffer di stencil.

Queste costanti vengono usate dal membro StencilCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



