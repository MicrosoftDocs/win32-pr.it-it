---
description: La proprietà PKEY \_ AudioEndpoint \_ JackSubType contiene un GUID di categoria di output per un dispositivo endpoint audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95ca24d48a35299144f36d052ceea2e2d0d12c56fbc03b58a993fd95772c9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053731"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

La **proprietà PKEY \_ AudioEndpoint \_ JackSubType** contiene un GUID della categoria di output per un dispositivo endpoint audio. Il file di intestazione Ksmedia.h definisce i GUID. ogni GUID specifica il tipo di connessione. A questi GUID sono associate anche categorie di pin. Ad esempio, il file di intestazione Ksmedia.h definisce il GUID **KSNODETYPE \_ DISPLAYPORT \_ INTERFACE** per una porta di visualizzazione che si connette al pin KS definito dal GUID **PINNAME \_ DISPLAYPORT \_ OUT**.

Per altre informazioni, vedere la descrizione delle proprietà della categoria pin nella documentazione Windows DDK.

Il **membro vt** della **struttura PROPVARIANT** è impostato su **VT \_ LPWSTR**.

Il **membro pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione Null che contiene un GUID di categoria.

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

[Proprietà audio di base](core-audio-properties.md)
</dt> </dl>

 

 




