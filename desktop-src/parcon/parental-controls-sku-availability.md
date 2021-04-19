---
description: Controllo parentale disponibilità SKU
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Controllo parentale disponibilità SKU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311581"
---
# <a name="parental-controls-sku-availability"></a>Controllo parentale disponibilità SKU

Le interfacce utente, le funzionalità e le API dei controlli padre descritti in questa sezione sono attualmente pianificate per essere disponibili solo per gli SKU incentrati sul cliente, ad esempio:

-   Windows Vista Starter
-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Ultimate

I controlli padre vengono installati solo in questi SKU. Le soluzioni che hanno un requisito per la distribuzione negli SKU aziendali dovranno:

-   Rilevare e non fornire funzionalità di controllo parentale negli SKU aziendali.
-   Rilevare e fornire un metodo alternativo di configurazione, registrazione e restrizioni.

È consigliabile che le soluzioni rilevino la disponibilità dell'infrastruttura dei controlli padre controllando la riuscita di COM CoCreateInstance nell'API di conformità.

Le applicazioni in grado di riconoscere i controlli padre, a seconda dell'infrastruttura di Windows Vista, possono anche voler evitare di visualizzare le impostazioni dell'interfaccia utente o altre funzionalità quando l'interfaccia utente dei controlli padre viene disattivata in uno SKU supportato. Viene fornita una funzione per la determinazione della visibilità che copre casi come l'eliminazione aggiunta a un dominio.

 

 



