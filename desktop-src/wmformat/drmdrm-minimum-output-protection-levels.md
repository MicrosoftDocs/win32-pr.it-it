---
title: Struttura DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: La \_ struttura dei livelli di protezione dell'output minimo DRM \_ \_ \_ include i livelli minimi di protezione dell'output (OPLs) per la riproduzione di diversi tipi di contenuto. Un dispositivo deve supportare il OPL minimo per un tipo di dati per ricevere il tipo di dati dal lettore.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- Formato di Windows Media per la struttura DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324454"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>\_Struttura del \_ \_ livello di protezione dell'output minimo DRM \_

La struttura dei **\_ livelli di \_ \_ protezione \_ dell'output minimo DRM** include i livelli minimi di protezione dell'output (OPLs) per la riproduzione di diversi tipi di contenuto. Un dispositivo deve supportare il OPL minimo per un tipo di dati per ricevere il tipo di dati dal lettore.

## <a name="syntax"></a>Sintassi


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**wCompressedDigitalVideo**
</dt> <dd>

Numero minimo di OPL necessari per la ricezione di video digitali compressi.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

Numero minimo di OPL necessari per la ricezione di video digitali non compressi.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

Numero minimo di OPL necessari per la ricezione di video analogici.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

OPL minime necessarie per ricevere audio digitale compresso.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

OPL minime necessarie per ricevere audio digitale non compresso.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata come membro della struttura [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





