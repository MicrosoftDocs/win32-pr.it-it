---
description: Dopo aver creato un documento HTML di origine della pagina di riferimento a un evento, è necessario denominarlo prima che Network Monitor possa visualizzarlo nella Visualizzatore eventi.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Denominazione di una pagina di riferimento a un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319934"
---
# <a name="naming-an-event-reference-page"></a>Denominazione di una pagina di riferimento a un evento

Dopo aver creato un documento HTML di origine della pagina di riferimento a un evento, è necessario denominarlo prima che Network Monitor possa visualizzarlo nella Visualizzatore eventi.

Nome e file ERP di esperti con il formato seguente:

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**Expertname**
</dt> <dd>

Nome del file DLL, esclusa l'estensione del nome file.

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**
</dt> <dd>

Identificatore dell'evento ERP esperto.

L'identificatore di evento è disponibile anche nel membro **EventIdent** della struttura **NMEVENTDATA** .

</dd> </dl>

Per ulteriori informazioni sulla creazione di un ERP, vedere gli argomenti seguenti:

-   [Creazione di pagine di riferimento per gli eventi Expert e monitor](creating-expert-and-monitor-event-reference-pages.md)
-   [Scrittura di una pagina di riferimento a un evento](writing-an-event-reference-page.md)
-   [Test di una pagina di riferimento a un evento](testing-an-event-reference-page.md)

 

 



