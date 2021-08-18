---
description: Indica che lo strumento di spostamento DVD ha iniziato o terminato la riproduzione dei dati del DVD.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4edbdb337c4b57a7ed09bd63a8ed4fb0d1946b289b369badab64b561000d3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928571"
---
# <a name="ec_dvd_karaoke_mode"></a>EC \_ DVD \_ DVD \_ MODALITÀ

Indica che lo strumento di spostamento [DVD ha](data-flow-in-the-dvd-navigator.md) iniziato o terminato la riproduzione dei dati del DVD.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

. Se **TRUE,** viene riprodotta una traccia di tipo "a". In caso contrario, non viene riprodotta alcuna traccia Disa.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il lettore DVD segnala questo evento ogni volta che cambia dominio.

Questo evento viene generato in tutti i domini DVD.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode.h (includere Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




