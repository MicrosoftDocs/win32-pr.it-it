---
description: Dopo aver creato un documento HTML di origine ERP (Event Reference Page), è necessario assegnare un nome prima Network Monitor possibile visualizzarlo nel Visualizzatore eventi.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Assegnazione di un nome a una pagina di riferimento eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569991c5e5ac24e18476fe27727f4fad1c310c8fd4e9439062fdf91bfb344005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799691"
---
# <a name="naming-an-event-reference-page"></a>Assegnazione di un nome a una pagina di riferimento eventi

Dopo aver creato un documento HTML di origine ERP (Event Reference Page), è necessario assegnare un nome prima Network Monitor possibile visualizzarlo nel Visualizzatore eventi.

Assegnare un nome al monitoraggio e ai file ERP esperti con questo formato:

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**
</dt> <dd>

Nome file DLL, esclusa l'estensione di file.

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**
</dt> <dd>

Identificatore dell'evento dell'ERP esperto.

L'identificatore dell'evento si trova anche nel **membro EventIdent** della **struttura NMEVENTDATA.**

</dd> </dl>

Per altre informazioni sulla creazione di un ERP, vedere gli argomenti seguenti:

-   [Creazione di pagine di riferimento per gli eventi expert e monitor](creating-expert-and-monitor-event-reference-pages.md)
-   [Scrittura di una pagina di riferimento eventi](writing-an-event-reference-page.md)
-   [Test di una pagina di riferimento eventi](testing-an-event-reference-page.md)

 

 



