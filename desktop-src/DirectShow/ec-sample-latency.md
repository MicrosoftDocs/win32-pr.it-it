---
description: Specifica la distanza di pianificazione di un componente per l'elaborazione degli esempi.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324152"
---
# <a name="ec_sample_latency"></a>\_ \_ latenza campione EC

Specifica la distanza di pianificazione di un componente per l'elaborazione degli esempi.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const reference \_ Time** \* ) la distanza dietro il componente, in unità di 100 nanosecondi. Se questo valore è positivo, il componente è dietro la pianificazione. Se questo valore è negativo, il componente precede la pianificazione.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Un presentatore personalizzato per il filtro EVR ( [**Enhanced video renderer**](enhanced-video-renderer-filter.md) ) può inviare questo messaggio a EVR per inviare una notifica a EVR se il Presenter è dietro la pianificazione o in anticipo.

Il modo più semplice per calcolare *lParam1* è: *QPC Now*   *QPC target*, dove *QPC ora* è l'ora di clock e *QPC target* è l'ora di presentazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Come scrivere un presentatore EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

