---
description: La \_ Proprietà pkey AudioEndpoint \_ JackSubType contiene un GUID della categoria di output per un dispositivo endpoint audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127438"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

La proprietà **pkey \_ AudioEndpoint \_ JACKSUBTYPE** contiene un GUID della categoria di output per un dispositivo endpoint audio. Il file di intestazione Ksmedia. h definisce i GUID; ogni GUID specifica il tipo di connessione. A questi GUID sono inoltre associate categorie pin. Ad esempio, il file di intestazione Ksmedia. h definisce **l' \_ \_ interfaccia DisplayPort KSNODETYPE** GUID per una porta di visualizzazione che si connette con il pin KS definito dal GUID **PINNAME \_ DisplayPort \_**.

Per ulteriori informazioni, vedere la descrizione delle proprietà della categoria pin nella documentazione di Windows DDK.

Il membro **VT** della struttura **PROPVARIANT** è impostato su **VT \_ LPWSTR**.

Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide a terminazione null che contiene un GUID di categoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




