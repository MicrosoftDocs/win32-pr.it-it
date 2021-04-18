---
description: La \_ proprietà di associazione pkey AudioEndpoint \_ associa una categoria di pin di streaming kernel (KS) a un dispositivo endpoint audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305262"
---
# <a name="pkey_audioendpoint_association"></a>\_Associazione pkey AudioEndpoint \_

La proprietà di **\_ \_ associazione pkey AudioEndpoint** associa una categoria di pin di streaming kernel (KS) a un dispositivo endpoint audio. Il file con estensione inf che installa una scheda audio assegna una categoria pin a ogni pin KS nell'adapter. Un pin KS in un dispositivo adapter rappresenta il punto in cui un flusso audio entra o esce dal dispositivo. Una categoria pin è un GUID che specifica il tipo di funzione eseguita da un pin KS. Ad esempio, il file di intestazione Ksmedia. h definisce il microfono KSNODETYPE GUID della categoria pin \_ per indicare un pin KS che si connette a un microfono e KSNODETYPE le \_ cuffie per indicare un pin KS che si connette alle cuffie. Per ulteriori informazioni, vedere la descrizione delle proprietà della categoria pin nella documentazione di Windows DDK.

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.

Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide a terminazione null che contiene un GUID di categoria del pin KS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà endpoint audio**](audio-endpoint-properties.md)
</dt> <dt>

[Proprietà audio principali](core-audio-properties.md)
</dt> </dl>

 

 




