---
description: Segnala che è stata avviata una modifica della frequenza nella riproduzione di DVD.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode.h)
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
ms.openlocfilehash: 8de40dc8fd7f70dda522f4d1faf34f8c05059c6928f80a141d7ac9ae1889ecec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823681"
---
# <a name="ec_dvd_playback_rate_change"></a>MODIFICA DELLA \_ VELOCITÀ DI RIPRODUZIONE DEI DVD \_ \_ \_ EC

Segnala che è stata avviata una modifica della frequenza nella riproduzione di DVD.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

LONG che indica la nuova velocità di riproduzione. Il valore è la velocità di riproduzione effettiva moltiplicata per 10.000, quindi la velocità di riproduzione è uguale a 10000,0 */lParam1.* I valori minori di zero indicano la modalità di riproduzione inversa e i valori maggiori di zero indicano la modalità di riproduzione in avanti.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene generato nel dominio del titolo.

La *velocità di* riproduzione è l'inverso della velocità di *riproduzione.* Ad esempio, se la velocità di riproduzione è 2x, la velocità è 0,5.

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

 

 




