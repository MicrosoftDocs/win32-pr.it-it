---
description: Windows Il programma di installazione implementa una serie di controlli standard che gli autori di pacchetti possono inserire nelle finestre di dialogo. Tuttavia, non tutti i controlli standard di Microsoft Windows sono disponibili e i controlli personalizzati non possono essere creati per l'uso con l'interfaccia utente del programma di installazione.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Panoramica sui controlli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee9d03f0f21f9cc0611a1fae4831b6ccbbda9f40eda873cdf4c26b259ec43f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638523"
---
# <a name="controls-overview"></a>Panoramica sui controlli

Windows Il programma di installazione implementa una serie di controlli standard che gli autori di pacchetti possono inserire nelle finestre di dialogo. Tuttavia, non tutti i controlli standard di Microsoft Windows sono disponibili e i controlli personalizzati non possono essere creati per l'uso con l'interfaccia utente del programma di installazione.

I controlli vengono creati nelle finestre di dialogo nel programma di installazione in modo simile a come le finestre di dialogo vengono create a livello di codice usando l'API dell'interfaccia utente Windows Microsoft. Un controllo viene creato da un modello registrato nella tabella Control. Questo modello è leggermente diverso in quanto contiene il nome univoco della finestra di dialogo in cui viene visualizzato il controllo .

Nell'API Windows dell'interfaccia utente di Microsoft, l'interazione dell'utente viene eseguita creando una funzione di callback per gestire i messaggi inviati dal controllo. Inoltre, la maggior parte Windows Microsoft riceve messaggi, ad esempio quelli inviati dalla [funzione SendMessage.](/windows/win32/api/winuser/nf-winuser-sendmessage)

La comunicazione tra l'utente e i controlli viene eseguita nel programma di installazione tramite [l'uso di ControlEvents](controlevent-overview.md). Tuttavia, esiste un set limitato di ControlEvent specifici per ogni controllo nel set limitato di controlli in Windows Installer. I controlli possono inviare più eventi ControlEvent e possono ricevere più eventi ControlEvent.

I controlli possono pubblicare eventi ControlEvent specifici tramite l'uso della tabella ControlEvent. I controlli possono ricevere ControlEvents tramite la [tabella EventMapping](eventmapping-table.md).

Windows Il programma di installazione pubblica anche ControlEvents durante l'esecuzione di alcune azioni e i controlli sottoscritti a questi ControlEvents nella tabella EventMapping li ricevono.

 

 
