---
description: Disponibilità degli SKU di Controllo genitori
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Disponibilità degli SKU di Controllo genitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21184a383a28e3ae06198f203475c1c03334e5d678278bbb3b4988b52971e79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461201"
---
# <a name="parental-controls-sku-availability"></a>Disponibilità degli SKU di Controllo genitori

Le interfacce utente, le funzionalità e le API di Controllo genitori descritte in questa sezione sono attualmente disponibili solo per SKU incentrati sugli utenti, ad esempio:

-   Windows Vista Starter
-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Ultimate

Controllo genitori viene installato solo su questi SKU. Le soluzioni con un requisito per la distribuzione in SKU aziendali dovranno:

-   Rilevare e non fornire funzionalità di controllo genitori sugli SKU aziendali.
-   Rilevare e fornire un mezzo alternativo per la configurazione, la registrazione e le restrizioni.

È consigliabile che le soluzioni rilevino la disponibilità dell'infrastruttura di controllo genitori verificando l'esito positivo di COM CoCreateInstance nell'API di conformità.

Le applicazioni compatibili con il controllo genitori a seconda dell'infrastruttura di Windows Vista possono anche voler eliminare qualsiasi interfaccia utente che espone impostazioni o altre funzionalità quando l'interfaccia utente di Controllo genitori viene eliminata in uno SKU supportato. Viene fornita una funzione per la determinazione della visibilità che copre casi come l'eliminazione di un dominio.

 

 



