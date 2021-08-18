---
description: L'evento DVDNotify notifica a un'applicazione molti eventi DVD e istruzioni su disco diversi.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988deaf53fb2b50555b4cf19a38684610aa0822a270dfba079defab92ce8aec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148704"
---
# <a name="dvdnotify"></a>DVDNotify

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

`DVDNotify`L'evento notifica a un'applicazione molti eventi DVD e istruzioni su disco diversi.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Specifica il codice di notifica degli eventi DVD.

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

[Dvd Event Notification Codes (Codici](dvd-notification-codes.md) di notifica eventi DVD) fornisce una spiegazione completa di tutti i codici di notifica degli eventi DVD e dei relativi parametri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segment.h</dt> </dl> |



 

 




