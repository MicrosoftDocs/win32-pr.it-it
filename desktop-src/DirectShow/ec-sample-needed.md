---
description: Richiede un nuovo esempio di input dal filtro renderer video avanzato (EVR).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da73d02604e128fdf94edb8f84d1526cfcdb586e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324149"
---
# <a name="ec_sample_needed"></a>\_esempio EC \_ necessario

Richiede un nuovo esempio di input dal filtro [**renderer video avanzato**](enhanced-video-renderer-filter.md) (EVR).

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificatore del flusso di input che necessita di un nuovo input.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il mixer per il filtro EVR Invia questo messaggio quando è necessario un nuovo esempio di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> </dl>

 

 




