---
description: Usare i controlli Windows standard, laddove possibile, perché sono completamente compatibili con le linee guida di Microsoft Active Accessibility. Sono inclusi i controlli forniti da Windows (User32.dll) e dalla libreria di controlli comuni di Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Utilizzo di controlli Windows standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343286"
---
# <a name="using-standard-windows-controls"></a>Utilizzo di controlli Windows standard

Usare i controlli Windows standard, laddove possibile, perché sono completamente compatibili con le linee guida di Microsoft Active Accessibility. Sono inclusi i controlli forniti da Windows (User32.dll) e dalla libreria di controlli comuni di Windows (Comctl32.dll).

Ogni controllo Windows standard è una finestra separata di una classe specifica, quindi l'assistenza per l'accessibilità riceve una notifica quando lo stato attivo si sposta su un nuovo controllo. Gli aiuti possono determinare la classe della finestra controlli e tutti i messaggi aggiuntivi che può inviare per eseguire query o modificare lo stato dei controlli. L'assistenza può inoltre identificare tutti i controlli figlio contenuti in una finestra padre e identificare l'elemento padre di qualsiasi controllo.

Alcuni controlli comuni sono estremamente flessibili e spesso possono sostituire i controlli personalizzati meno accessibili e quelli creati dal proprietario. Una visualizzazione elenco, ad esempio, può sostituire una casella di riepilogo creata dal proprietario per visualizzare una casella di controllo accanto a ogni elemento. Come altro esempio, il controllo pulsante avanzato può visualizzare sia immagini che testo. In precedenza, era necessario usare un controllo personalizzato.

 

 



