---
description: IMPOSTAZIONI \_ LOCALI IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: da0d8697e8a02bb6943f4a4154a1ea89c4e01cbaed7576631e3a61d161e80503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147424"
---
# <a name="locale_ifirstweekofyear"></a>IMPOSTAZIONI \_ LOCALI IFIRSTWEEKOFYEAR

Prima settimana dell'anno.



| Valore | Significato                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | La settimana contenente 1/1 è la prima settimana dell'anno. Si noti che può trattarsi di un singolo giorno, se 1/1 cade l'ultimo giorno della settimana. |
| 1     | La prima settimana completa successiva all'1/1 è la prima settimana dell'anno.                                                                     |
| 2     | La prima settimana contenente almeno quattro giorni è la prima settimana dell'anno. Compatibile con ISO 8601.                                     |

Se LOCALE_IFIRSTWEEKOFYEAR è 2, LOCALE_IFIRSTDAYOFWEEK è 0 (lunedì) e LOCALE_ICALENDARTYPE è gregoriano, la prima settimana segue la definizione ISO 8601 in cui la prima settimana è la settimana con il primo giovedì dell'anno gregoriano.


 

 

 



