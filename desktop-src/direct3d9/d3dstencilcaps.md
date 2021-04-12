---
description: Flag funzionalità stencil driver.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e76c42acfcf8b6515e84679ea2fb540178608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401384"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Flag funzionalità stencil driver.



|                          |             |                                                                                                       |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| \#definire                 | Valore       | Descrizione                                                                                           |
| D3DSTENCILCAPS \_ Keep     | 0x00000001L | Non aggiornare la voce nel buffer dello stencil. Si tratta del valore predefinito.                             |
| D3DSTENCILCAPS \_ zero     | 0x00000002L | Impostare la voce stencil-buffer su 0.                                                                    |
| D3DSTENCILCAPS \_ Sostituisci  | 0x00000004L | Sostituire la voce dello stencil buffer con il valore di riferimento.                                                |
| \_INCRSAT D3DSTENCILCAPS  | 0x00000008L | Incrementa la voce dello stencil buffer, bloccando il valore massimo.                                    |
| \_DECRSAT D3DSTENCILCAPS  | 0x00000010L | Decrementa la voce del buffer di stencil, che viene fissata a zero.                                                 |
| D3DSTENCILCAPS \_ invertito   | 0x00000020L | Inverti i bit nella voce dello stencil buffer.                                                          |
| \_Incr D3DSTENCILCAPS     | 0x00000040L | Incrementa la voce dello stencil buffer, eseguendo il wrapping su zero se il nuovo valore supera il valore massimo.      |
| \_Decr D3DSTENCILCAPS     | 0x00000080L | Decrementa la voce dello stencil buffer, eseguendo il wrapping fino al valore massimo se il nuovo valore è minore di zero. |
| \_TWOSIDED D3DSTENCILCAPS | 0x00000100L | Il dispositivo supporta lo stencil a due lati.                                                                |



 

Gli stencil: le voci del buffer sono valori integer compresi tra 0 e 2 Grigioni-1, dove n è la profondità di bit del buffer dello stencil.

Queste costanti vengono usate dal membro StencilCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



