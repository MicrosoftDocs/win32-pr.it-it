---
description: Specifica la distanza rispetto alla pianificazione di un componente per l'elaborazione degli esempi.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612c553916dc19685224bb512f6627363dba439883553d82c59f153324f5eda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686151"
---
# <a name="ec_sample_latency"></a>LATENZA \_ DI \_ ESEMPIO EC

Specifica la distanza rispetto alla pianificazione di un componente per l'elaborazione degli esempi.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const REFERENCE \_ TIME**) Distanza del \* componente, in unità da 100 nanosecondi. Se questo valore è positivo, il componente è in ritardo rispetto alla pianificazione. Se questo valore è negativo, il componente è in anticipo rispetto alla pianificazione.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Un presentatore personalizzato per il filtro EVR [**(Enhanced Video Renderer)**](enhanced-video-renderer-filter.md) può inviare questo messaggio all'EVR per notificare all'EVR se il presentatore è in ritardo rispetto alla pianificazione o in anticipo rispetto alla pianificazione.

Il modo più semplice per calcolare *lParam1* è: *QPC now*   *QPC target*, dove *QPC* è ora l'ora dell'orologio e *QPC target* è l'ora di presentazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Come scrivere un presentatore EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

