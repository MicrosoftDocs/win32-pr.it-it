---
description: Usare controlli Windows standard quando possibile, perché sono completamente compatibili con le linee guida Microsoft Active Accessibility standard. Sono inclusi i controlli forniti da Windows (User32.dll) e dalla libreria Windows controlli comuni (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Uso di controlli Windows standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71beab38b4ee6ea6472a34b4edb190deed97731496eac7101859a9340c65ad0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449274"
---
# <a name="using-standard-windows-controls"></a>Uso di controlli Windows standard

Usare controlli Windows standard quando possibile, perché sono completamente compatibili con le linee guida Microsoft Active Accessibility standard. Sono inclusi i controlli forniti da Windows (User32.dll) e dalla libreria Windows controlli comuni (Comctl32.dll).

Ogni controllo Windows standard è una finestra separata di una classe specifica, quindi il supporto per l'accessibilità viene notificato quando lo stato attivo passa a un nuovo controllo. L'aiuto può determinare la classe della finestra dei controlli ed eventuali messaggi aggiuntivi che può inviare per eseguire query o modificare lo stato dei controlli. Il supporto può anche identificare tutti i controlli figlio contenuti in una finestra padre e identificare l'elemento padre di qualsiasi controllo.

Alcuni controlli comuni sono estremamente flessibili e spesso possono sostituire i controlli personalizzati meno accessibili e i controlli disegnati dal proprietario. Ad esempio, una visualizzazione elenco può sostituire una casella di riepilogo disegnata dal proprietario per visualizzare una casella di controllo accanto a ogni elemento. Come altro esempio, il controllo pulsante avanzato può visualizzare sia immagini che testo. In precedenza, questo richiedeva l'uso di un controllo personalizzato.

 

 



