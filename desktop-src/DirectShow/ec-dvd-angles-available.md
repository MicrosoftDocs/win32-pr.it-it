---
description: Indica se è in corso la riproduzione di un blocco di angolo ed è possibile modificare l'angolo.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e95c692aed8ac6c709ff0db1d6056fc59219fa73f5aa2e4cfb9b31b2c1a03d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015989"
---
# <a name="ec_dvd_angles_available"></a>EC \_ DVD \_ ANGLES \_ AVAILABLE

Indica se è in corso la riproduzione di un blocco di angolo ed è possibile modificare l'angolo.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore booleano **(BOOL)** che indica se viene riprodotto un blocco angolare. Zero (0) indica che la riproduzione non è in un blocco di angolo e che gli angoli non sono disponibili, uno (1) indica che è in corso la riproduzione di un blocco angolare ed è possibile apportare modifiche all'angolo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le modifiche dell'angolo non sono limitate ai blocchi angolare e la variazione dell'angolo può essere vista solo in un blocco angolare.

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

 

 




