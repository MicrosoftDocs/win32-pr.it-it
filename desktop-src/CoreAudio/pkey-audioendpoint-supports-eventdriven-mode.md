---
description: PKEY \_ AudioEndpoint \_ supporta la \_ proprietà della \_ modalità EventDriven indica se l'endpoint supporta la modalità guidata dagli eventi.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966288"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>PKEY \_ AudioEndpoint \_ supporta \_ la \_ modalità EventDriven

**Pkey AudioEndpoint supporta la proprietà della \_ \_ \_ \_ modalità EventDriven** indica se l'endpoint supporta la modalità guidata dagli eventi.

Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ UI4.

Il membro **uintVal** della struttura **PROPVARIANT** è un **valore DWORD** che indica se l'endpoint supporta la modalità guidata dagli eventi.

## <a name="remarks"></a>Commenti

Il valore di questa proprietà viene popolato da un OEM audio in un file con estensione inf per indicare che l'hardware HDAudio supporta la modalità guidata dagli eventi in base al requisito WHQL.

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

 

 




