---
description: Specifica informazioni sui frame di riferimento a lungo termine (LTR) e viene restituito nell'esempio di output.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: MFSampleExtension_LongTermReferenceFrameInfo attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642c246adf0e5e1c10249085201fba3dc430b6547516b79fe4929e9de4b998a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848121"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>Attributo MFSampleExtension \_ LongTermReferenceFrameInfo

Specifica informazioni sui frame di riferimento a lungo termine (LTR) e viene restituito nell'esempio di output.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

**Codificatori H.264/AVC:**

I codificatori devono restituire questo attributo nell'esempio di output quando l'applicazione controlla i fotogrammi LTR, specificato da [CODECAPI \_ AVEncVideoLTRBufferControl.](codecapi-avencvideoltrbuffercontrol.md)

MFSampleExtension \_ LongTermReferenceFrameInfo restituisce un massimo di due campi.

Il primo campo, bit \[ 0..15, è \] *LongTermFrameIdx* associato al frame di output se è contrassegnato come frame LTR. Il primo valore è 0xffff, se questo frame di output è un frame di riferimento a breve termine o un frame non di riferimento.

Il secondo campo, bit \[ 16..31, è una bitmap costituita da \] molti bit *MaxNumLTRFrames* che indicano quali fotogrammi ATR sono stati usati per la codifica di questo frame di output, a partire dal bit 16. I restanti bit devono essere impostati su 0. Il secondo valore è 0 se questo frame di output non è codificato usando fotogrammi LTR. *MaxNumLTRFrames* è il numero massimo di fotogrammi LTR impostati tramite [CODECAPI \_ AVEncVideoLTRBufferControl.](codecapi-avencvideoltrbuffercontrol.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




