---
description: Alcuni movimenti dell'applicazione possono essere in conflitto con caratteri asiatici orientali o combinazioni di caratteri asiatici orientali.
ms.assetid: 56ff773f-ef95-47f8-ba04-2593330867ee
title: Conflitti con caratteri East-Asian
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb12b9fab1389395b249f35da3dc5ffbfc91af83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128127"
---
# <a name="conflicts-with-east-asian-characters"></a>Conflitti con caratteri East-Asian

Alcuni *movimenti dell'applicazione* possono essere in conflitto con caratteri asiatici orientali o combinazioni di caratteri asiatici orientali. Nella tabella seguente sono elencati i possibili conflitti tra i movimenti dell'applicazione e i caratteri delle applicazioni con input di caratteri asiatici orientali specifici.



| Movimento                 | Cinese (semplificato) | Cinese (tradizionale) | Giapponese     | Coreano       |
|-------------------------|----------------------|-----------------------|--------------|--------------|
| Giù<br/>         | X<br/>         | X<br/>          | X<br/> | X<br/> |
| Destra<br/>        | X<br/>         | X<br/>          | X<br/> | X<br/> |
| DownRight<br/>    | -<br/>         | X<br/>          | -<br/> | X<br/> |
| RightDown<br/>    | -<br/>         | -<br/>          | X<br/> | X<br/> |
| Circle<br/>       | -<br/>         | -<br/>          | -<br/> | X<br/> |
| ChevronRight<br/> | -<br/>         | -<br/>          | -<br/> | X<br/> |



 

Microsoft resta impegnata nello sviluppo di *movimenti*. Microsoft riconosce che nella creazione di applicazioni, i fornitori di software indipendenti (ISV) devono saper quali azioni verranno mappate ai movimenti. [Glifi non implementati](unimplemented-glyphs.md) elenca un set di azioni penna che Microsoft prevede di mappare ai movimenti, oltre a movimenti riservati per le azioni. Queste informazioni vengono fornite in modo da comprendere quali azioni e movimenti verranno fornite in futuro.

Oltre a utilizzare i movimenti disponibili in Microsoft Windows XP Tablet PC Edition, le applicazioni sono gratuite per creare i propri movimenti. Questi movimenti possono quindi essere riconosciuti da un *riconoscitore di movimento Microsoft* che lo sviluppatore di applicazioni compila. Se si intende implementare uno dei propri movimenti, consultare [glifi non implementati](unimplemented-glyphs.md) per evitare sovrapposizioni con i movimenti che Microsoft intende implementare.

 

 




