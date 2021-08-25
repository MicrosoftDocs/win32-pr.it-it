---
description: La proprietà PKEY \_ AudioEngine OEMFormat specifica il formato predefinito del dispositivo usato per il rendering o l'acquisizione \_ di un flusso. I valori vengono popolati dall'OEM in un file inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed43ee7a607bc7b97e6ce521c3c1f76356380d27b3471d16dde27cd021838e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053641"
---
# <a name="pkey_audioengine_oemformat"></a>PKEY \_ AudioEngine \_ OEMFormat

La proprietà PKEY \_ AudioEngine OEMFormat specifica il formato predefinito del dispositivo usato per il rendering o l'acquisizione \_ di un flusso. I valori vengono popolati dall'OEM in un file inf.

Il **membro vt** della **struttura PROPVARIANT** è impostato su BLOB VT. \_

Il **membro** BLOB della **struttura PROPVARIANT** è una struttura di tipo **BLOB** che contiene due membri. Member **blob.cbSize** è un **valore DWORD** che specifica il numero di byte nella descrizione del formato. Il **membro blob.pBlobData** punta a una **struttura WAVEFORMATEX** che contiene la descrizione del formato. Per altre informazioni su BLOB, vedere la documentazione Windows SDK. Per altre informazioni su **WAVEFORMATEX,** vedere la documentazione Windows DDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà dell'endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




