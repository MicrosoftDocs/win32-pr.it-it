---
description: L'evento DVDNotify notifica a un'applicazione di molti eventi DVD e istruzioni per i dischi diversi.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329262"
---
# <a name="dvdnotify"></a>DVDNotify

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

L' `DVDNotify` evento invia una notifica all'applicazione di molti eventi DVD e istruzioni per i dischi diversi.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Specifica il codice di notifica dell'evento DVD.

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*
</dt> <dd>

Può contenere informazioni aggiuntive correlate all'evento.

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

Può contenere informazioni aggiuntive correlate all'evento.

</dd> </dl>

## <a name="remarks"></a>Commenti

I [codici di notifica degli eventi DVD](dvd-notification-codes.md) forniscono una spiegazione completa di tutti i codici di notifica degli eventi DVD e dei relativi parametri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segmento. h</dt> </dl> |



 

 




