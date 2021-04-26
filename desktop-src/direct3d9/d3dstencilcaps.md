---
description: Flag di funzionalità dello stencil del driver.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6716748d77fe4c3620413f43ae4a4ae48076c09f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997378"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Flag di funzionalità dello stencil del driver.



| \#Definire                 | Valore       | Descrizione                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| D3DSTENCILCAPS \_ KEEP     | 0x00000001L | Non aggiornare la voce nel buffer degli stencil. Si tratta del valore predefinito.                             |
| D3DSTENCILCAPS \_ ZERO     | 0x00000002L | Impostare la voce stencil-buffer su 0.                                                                    |
| D3DSTENCILCAPS \_ REPLACE  | 0x00000004L | Sostituire la voce stencil-buffer con il valore di riferimento.                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | Incrementare la voce dello stencil buffer, fissando il valore massimo.                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | Decrementare la voce dello stencil buffer, fissando a zero.                                                 |
| D3DSTENCILCAPS \_ INVERT   | 0x00000020L | Invertire i bit nella voce stencil-buffer.                                                          |
| D3DSTENCILCAPS \_ INCR     | 0x00000040L | Incrementare la voce stencil-buffer, a capo su zero se il nuovo valore supera il valore massimo.      |
| DECREMENTO D3DSTENCILCAPS \_     | 0x00000080L | Decrementare la voce stencil-buffer, a capo fino al valore massimo se il nuovo valore è minore di zero. |
| D3DSTENCILCAPS \_ TWOSIDED | 0x00000100L | Il dispositivo supporta stencil a due lati.                                                                |



 

Le voci stencil-buffer sono valori interi compresi tra 0 e 2ⁿ - 1, dove n è la profondità in bit del buffer degli stencil.

Queste costanti vengono usate dal membro StencilCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



