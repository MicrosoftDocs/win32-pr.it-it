---
description: Windows Installer implementa una serie di controlli standard che gli autori di pacchetti possono inserire nelle finestre di dialogo. Tuttavia, non tutti i controlli standard di Microsoft Windows sono disponibili e non è possibile creare controlli personalizzati per l'uso con l'interfaccia utente del programma di installazione.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Panoramica sui controlli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318290"
---
# <a name="controls-overview"></a>Panoramica sui controlli

Windows Installer implementa una serie di controlli standard che gli autori di pacchetti possono inserire nelle finestre di dialogo. Tuttavia, non tutti i controlli standard di Microsoft Windows sono disponibili e non è possibile creare controlli personalizzati per l'uso con l'interfaccia utente del programma di installazione.

I controlli vengono creati nelle finestre di dialogo del programma di installazione in modo analogo a come le finestre di dialogo vengono create a livello di programmazione tramite l'API dell'interfaccia utente di Microsoft Windows. Viene creato un controllo da un modello registrato nella tabella dei controlli. Questo modello è leggermente diverso perché contiene il nome univoco della finestra di dialogo in cui viene visualizzato il controllo.

Nell'API dell'interfaccia utente di Microsoft Windows, l'interazione dell'utente viene eseguita creando una funzione di callback per gestire i messaggi inviati dal controllo. Inoltre, la maggior parte dei controlli di Microsoft Windows riceve messaggi, ad esempio quelli inviati dalla funzione [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .

La comunicazione tra l'utente e i controlli viene eseguita nel programma di installazione tramite l'uso di [ControlEvents](controlevent-overview.md). Tuttavia, esiste un set limitato di ControlEvents specifici per ogni controllo nel set limitato di controlli in Windows Installer. I controlli possono inviare più di un ControlEvent e possono ricevere più di un ControlEvent.

I controlli possono pubblicare ControlEvents specifiche tramite l'uso della tabella ControlEvent. I controlli possono ricevere ControlEvents tramite l'uso della [tabella EventMapping](eventmapping-table.md).

Windows Installer pubblica ControlEvents anche durante l'esecuzione di alcune azioni e i controlli sottoscritti a questi ControlEvents nella tabella EventMapping li ricevono.

 

 
