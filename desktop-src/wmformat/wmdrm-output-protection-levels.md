---
title: WMDRM_OUTPUT_PROTECTION_LEVELS struttura (Wmdrmsdk.h)
description: La struttura WMDRM OUTPUT PROTECTION LEVELS contiene i livelli di protezione dell'output richiesti da una licenza \_ \_ per eseguire varie \_ azioni.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS struttura windows Media Format
- Struttura windows Media Format
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
ms.openlocfilehash: 4a19d7098266857f8a17e395ad749b216e45ce101278812f67c032943933955a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843962"
---
# <a name="wmdrm_output_protection_levels-structure"></a>Struttura WMDRM \_ OUTPUT \_ PROTECTION \_ LEVELS

La **struttura WMDRM \_ OUTPUT PROTECTION \_ \_ LEVELS** contiene i livelli di protezione dell'output richiesti da una licenza per eseguire varie azioni.

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

OPL minimo necessario per ricevere video digitale compresso.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

OPL minimo necessario per ricevere video digitali non compressi.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

OPL minimo necessario per ricevere video analogico.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

OPL minimo necessario per ricevere audio digitale compresso.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

OPL minimo necessario per ricevere audio digitale non compresso.

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

OPL minimo necessario per copiare il contenuto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata dal [**metodo IWMDRMLicense::GetOutputProtectionLevels.**](iwmdrmlicense-getoutputprotectionlevels.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





