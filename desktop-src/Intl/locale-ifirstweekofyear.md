---
description: impostazioni locali \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320219"
---
# <a name="locale_ifirstweekofyear"></a>impostazioni locali \_ IFIRSTWEEKOFYEAR

Prima settimana dell'anno.



| Valore | Significato                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | La settimana che contiene la 1/1 è la prima settimana dell'anno. Si noti che può essere un singolo giorno, se 1/1 rientra nell'ultimo giorno della settimana. |
| 1     | La prima settimana completa successiva alla 1/1 è la prima settimana dell'anno.                                                                     |
| 2     | La prima settimana che contiene almeno quattro giorni è la prima settimana dell'anno. Compatibile con ISO 8601.                                     |

Se LOCALE_IFIRSTWEEKOFYEAR è 2, LOCALE_IFIRSTDAYOFWEEK è 0 (lunedì) e LOCALE_ICALENDARTYPE è gregoriano, la prima settimana segue la definizione ISO 8601 dove la prima settimana è la settimana con il primo giovedì dell'anno gregoriano.


 

 

 



