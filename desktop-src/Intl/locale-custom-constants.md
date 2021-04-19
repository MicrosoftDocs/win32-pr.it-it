---
description: Costanti personalizzate delle impostazioni locali \_ \*
ms.assetid: a41a7f55-8905-47a1-86c3-74ed40b3834c
title: Costanti LOCALE_CUSTOM *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4e02cc672241fd609a5eda975c0e9e13d29908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305649"
---
# <a name="locale_custom-constants"></a>Costanti personalizzate delle impostazioni locali \_ \*

In questo argomento vengono definite le \_ costanti personalizzate delle impostazioni locali \* utilizzate da NLS per rappresentare [impostazioni locali personalizzate](custom-locales.md).



| Valore                       | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| impostazioni locali \_ personalizzate \_ predefinite     | **Windows Vista e versioni successive:** Impostazioni locali personalizzate predefinite. Quando una funzione NLS deve restituire un identificatore delle impostazioni locali per le [impostazioni locali aggiuntive](custom-locales.md) per l'utente corrente, la funzione restituisce questo valore anziché [impostazioni locali dell' \_ utente \_ ](locale-user-default.md). Il valore predefinito personalizzato delle impostazioni locali \_ \_ è 0x0c00.                                                                                                                                                                  |
| \_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_ | **Windows Vista e versioni successive:** Impostazioni locali personalizzate predefinite per MUI. Le lingue dell'interfaccia utente preferite dall'utente e le lingue dell'interfaccia utente preferite del sistema possono includere al massimo una sola lingua implementata da un LIP (Language Interface Pack) e per il quale l'identificatore di lingua corrisponde a impostazioni locali aggiuntive. Se è presente un linguaggio di questo tipo in un elenco, la costante viene utilizzata per fare riferimento a tale lingua in determinati contesti. Il valore predefinito dell'interfaccia utente personalizzata per le impostazioni locali \_ \_ \_ è 0x1400.                    |
| impostazioni locali \_ personalizzate non \_ specificate | **Windows Vista e versioni successive:** Impostazioni locali personalizzate non specificate, utilizzate per identificare tutte le impostazioni locali aggiuntive ad eccezione delle impostazioni locali per l'utente corrente. Le impostazioni locali supplementari non possono essere distinte l'una dall'altra in base agli identificatori delle impostazioni locali, ma possono essere distinte in base ai [nomi delle impostazioni locali](locale-names.md). Alcune funzioni NLS possono restituire questa costante per indicare che non possono fornire un identificatore utile per determinate impostazioni locali. Il valore di impostazioni locali \_ personalizzato non \_ specificato è 0x1000. |



 

 

 



