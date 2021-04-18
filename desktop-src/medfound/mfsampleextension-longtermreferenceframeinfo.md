---
description: Specifica le informazioni del frame di riferimento a lungo termine (LTR) e viene restituito nell'esempio di output.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: Attributo MFSampleExtension_LongTermReferenceFrameInfo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af85ffa5876cdf58a21a6933c46f460c23e7456
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320813"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>\_Attributo LongTermReferenceFrameInfo di MFSampleExtension

Specifica le informazioni del frame di riferimento a lungo termine (LTR) e viene restituito nell'esempio di output.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

**Codificatori H. 264/AVC:**

I codificatori devono restituire questo attributo nell'esempio di output quando l'applicazione controlla i frame LTR, che è specificato da [codecapi \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

MFSampleExtension \_ LongTermReferenceFrameInfo restituisce fino a due campi.

Il primo campo, BITS \[ 0.. 15 \] , è *LongTermFrameIdx* associato al frame di output se è contrassegnato come frame ltr. Il primo valore è 0xFFFF, se questo frame di output è un frame di riferimento a breve termine o un frame non di riferimento.

Il secondo campo, BITS \[ 16.31 \] , è una bitmap costituita da *MaxNumLTRFrames* molti bit che indicano i frame LTR usati per codificare questo frame di output, a partire dal bit 16. Il resto dei bit deve essere impostato su 0. Il secondo valore è 0 se il frame di output non è codificato con frame LTR. *MaxNumLTRFrames* è il numero massimo di fotogrammi LTR impostati tramite [codecapis \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




