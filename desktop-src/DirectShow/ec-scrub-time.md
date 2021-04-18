---
description: Specifica il timestamp per il passaggio del frame più recente.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329261"
---
# <a name="ec_scrub_time"></a>\_tempo di scrub EC \_

Specifica il timestamp per il passaggio del frame più recente.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Inferiore 32 bit del timestamp.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) 32 bit superiori del timestamp.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il presentatore per il filtro EVR ( [**Enhanced video renderer**](enhanced-video-renderer-filter.md) ) Invia questo messaggio al EVR quando completa un passaggio del frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> </dl>

 

 




