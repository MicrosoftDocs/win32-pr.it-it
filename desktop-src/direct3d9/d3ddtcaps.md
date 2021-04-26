---
description: Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 094ca568554722f4da2606233f4ad2c1e59e892f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999448"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.



| \#Definire              | Valore       | Descrizione                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3DDTCAPS \_ UBYTE4     | 0x00000001L | Byte senza segno 4D.                                                                                                             |
| D3DDTCAPS \_ UBYTE4N    | 0x00000002L | Byte senza segno normalizzato 4D. Ognuno dei quattro byte viene normalizzato dividendo a 255,0.                                      |
| D3DDTCAPS \_ SHORT2N    | 0x00000004L | Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).                                     |
| D3DDTCAPS \_ SHORT4N    | 0x00000008L | Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).  |
| D3DDTCAPS \_ USHORT2N   | 0x00000010L | Normalizzato, 2D unsigned short, espanso in (primo byte/65535.0, secondo byte/65535.0, 0, 1).                                   |
| D3DDTCAPS \_ USHORT4N   | 0x00000020L | Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0). |
| D3DDTCAPS \_ UDEC3      | 0x00000040L | Formato 3D senza segno 10 10 10 espanso in (valore, valore, valore, 1).                                                             |
| D3DDTCAPS \_ DEC3N      | 0x00000080L | Formato 10 10 10 con segno 3D normalizzato ed espanso a (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100L | Numeri a virgola mobile a 16 bit 2D.                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200L | Numeri a virgola mobile a 16 bit 4D.                                                                                             |



 

Queste costanti vengono usate dal membro DeclTypes di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



