---
description: Definisce lo stato di Output Protection Manager (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: MF_MEDIA_ENGINE_OPM_STATUS enumerazione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 98efb0054402f8bf019e91d639f16322a1378a23dfeee76cd31daea9d12bf6fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013041"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>Enumerazione MF \_ MEDIA \_ ENGINE \_ OPM \_ STATUS

Definisce lo stato di [Output Protection Manager](output-protection-manager.md) (OPM).

## <a name="syntax"></a>Sintassi


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MOTORE MULTIMEDIALE MF \_ \_ \_ OPM \_ NON \_ RICHIESTO**
</dt> <dd>

Stato predefinito. Usato per restituire lo stato corretto quando il contenuto non è protetto.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ ESTABLISHED**
</dt> <dd>

OPM è stato stabilito correttamente.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MACCHINA VIRTUALE \_ OPM DEL MOTORE MULTIMEDIALE MF \_ \_ NON \_ \_ RIUSCITA**
</dt> <dd>

OPM non riuscito perché in esecuzione in una macchina virtuale (VM).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ FAILED \_ BDA**
</dt> <dd>

OPM non è riuscito perché non è presente alcun driver di grafica e il sistema sta usando BDA (Basic Display Adapter).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ FAILED \_ UNSIGNED \_ DRIVER**
</dt> <dd>

OPM non riuscito perché il driver di grafica non è con firma PE, con fall back a WARP.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ FAILED**
</dt> <dd>

OPM non è riuscito per altri motivi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation enumerazioni](media-foundation-enumerations.md)
</dt> </dl>

 

 




