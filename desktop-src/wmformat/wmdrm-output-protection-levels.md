---
title: Struttura WMDRM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: La \_ struttura dei \_ livelli di protezione dell'output \_ di WMDRM contiene i livelli di protezione dell'output (OPLs) richiesti da una licenza per eseguire varie azioni.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- Formato di Windows Media per la struttura WMDRM_OUTPUT_PROTECTION_LEVELS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326598"
---
# <a name="wmdrm_output_protection_levels-structure"></a>\_Struttura del \_ livello di protezione dell'output WMDRM \_

La struttura dei livelli di protezione dell'output di WMDRM contiene i livelli di protezione dell'output (OPLs) richiesti da una licenza per eseguire varie azioni. **\_ \_ \_**

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
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

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

OPL minimo necessario per copiare il contenuto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata dal metodo [**IWMDRMLicense:: GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





