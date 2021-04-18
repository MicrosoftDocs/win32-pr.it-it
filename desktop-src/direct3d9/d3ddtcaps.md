---
description: Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49131fed9961782a6ade3d3ec5f541bb0fe63a50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304794"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.



|                       |             |                                                                                                                               |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| \#definire              | Valore       | Descrizione                                                                                                                   |
| \_UBYTE4 D3DDTCAPS     | 0x00000001L | byte senza segno 4D.                                                                                                             |
| \_Dati UBYTE4N D3DDTCAPS    | 0x00000002L | Normalizzato, byte senza segno 4D. Ognuno dei quattro byte viene normalizzato dividendo in 255,0.                                      |
| \_SHORT2N D3DDTCAPS    | 0x00000004L | Normalizzato, short con segno 2D, espanso fino a (primo byte/32767.0, secondo byte/32767.0, 0, 1).                                     |
| \_SHORT4N D3DDTCAPS    | 0x00000008L | Normalizzato, 4D con firma breve, espanso fino a (primo byte/32767.0, secondo byte/32767.0, terzo byte/32767.0, quarto byte/32767.0).  |
| \_USHORT2N D3DDTCAPS   | 0x00000010L | Normalizzato, breve senza segno 2D, espanso in (primo byte/65535.0, secondo byte/65535.0, 0, 1).                                   |
| \_USHORT4N D3DDTCAPS   | 0x00000020L | Normalizzato di 4D senza segno, espanso fino a (primo byte/65535.0, secondo byte/65535.0, terzo byte/65535.0, quarto byte/65535.0). |
| \_UDEC3 D3DDTCAPS      | 0x00000040L | formato 3D senza segno 10 10 10 espanso a (valore, valore, valore, 1).                                                             |
| \_DEC3N D3DDTCAPS      | 0x00000080L | formato con firma 3D 10 10 10 normalizzato ed espanso a (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100L | numeri a virgola mobile a 16 bit 2D.                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200L | numeri a virgola mobile a 16 bit 4D.                                                                                             |



 

Queste costanti vengono usate dal membro DeclTypes di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



