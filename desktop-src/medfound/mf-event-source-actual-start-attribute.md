---
description: Contiene l'ora di inizio in cui un'origine multimediale viene riavviata dalla posizione corrente.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Attributo MF_EVENT_SOURCE_ACTUAL_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401677"
---
# <a name="mf_event_source_actual_start-attribute"></a>\_ \_ \_ Attributo iniziale effettivo origine evento MF \_

Contiene l'ora di inizio in cui un'origine multimediale viene riavviata dalla posizione corrente.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come valore **LONGLONG** .

## <a name="remarks"></a>Commenti

Questo attributo viene utilizzato con l'evento [MESourceStarted](mesourcestarted.md) . L'attributo è pertinente quando i dati dell'evento sono vuoti (**VT \_ vuoto**), che indica che l'origine multimediale è stata avviata dalla posizione di riproduzione corrente. In tal caso, l' **attributo \_ \_ \_ \_ Start effettivo dell'origine eventi MF** specifica l'ora di inizio effettiva. Se i dati dell'evento sono **VT \_ vuoti** e questo attributo non è impostato, si presuppone che l'ora di inizio sia zero.

Quando i dati dell'evento [MESourceStarted](mesourcestarted.md) contengono l'ora di inizio (**VT \_ i8**), questo attributo non deve essere impostato.

Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




