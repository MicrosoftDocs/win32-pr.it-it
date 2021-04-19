---
description: Segnala che è stata avviata una modifica della frequenza nella riproduzione DVD.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326644"
---
# <a name="ec_dvd_playback_rate_change"></a>\_modifica della \_ frequenza di riproduzione DVD \_ EC \_

Segnala che è stata avviata una modifica della frequenza nella riproduzione DVD.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore LONG che indica la nuova velocità di riproduzione. Il valore è la velocità effettiva di riproduzione moltiplicata per 10.000, quindi la velocità di riproduzione è uguale a 10000,0/ *lParam1*. I valori minori di zero indicano la modalità di riproduzione inversa e i valori maggiori di zero indicano la modalità di riproduzione in modalità diretta.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene generato nel dominio del titolo.

La *frequenza* di riproduzione è l'inverso della *velocità* di riproduzione. Se ad esempio la velocità di riproduzione è 2x, la frequenza è 0,5.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode. h (include dshow. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




