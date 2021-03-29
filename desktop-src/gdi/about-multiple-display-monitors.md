---
description: Quando più monitoraggi fanno parte del desktop, gli oggetti possono spostarsi facilmente tra i monitoraggi.
ms.assetid: eb7576c6-322c-48d0-abbb-bdc3b34976c3
title: Informazioni su più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5997e39768d01522ae1fdd2e976c611e67826350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978191"
---
# <a name="about-multiple-display-monitors"></a>Informazioni su più monitor di visualizzazione

Quando più monitoraggi fanno parte del desktop, gli oggetti possono spostarsi facilmente tra i monitoraggi. Ovvero è possibile trascinare le finestre o i collegamenti da un monitoraggio a un altro ed è possibile ridimensionare le finestre per coprire più di un monitor. Inoltre, se un monitoraggio viene installato al di sopra di un altro, viene visualizzato un cursore che lascia la parte inferiore del monitor superiore nella parte superiore del monitor inferiore.

In genere, un utente dispone i monitoraggi nel sistema in modo da riflettere la disposizione delle unità di visualizzazione fisiche; ad esempio, Side-by-side o One-on-top-of-other. L'utente esegue questa operazione con la scheda monitoraggi, che sostituisce la scheda **Impostazioni** della finestra di dialogo **proprietà di visualizzazione** tramite il pannello di controllo. I monitoraggi devono formare un'area contigua, ovvero ogni monitoraggio tocca un altro monitor in almeno una parte di un bordo.

Quando una finestra viene spostata o ridimensionata, parte della didascalia è sempre visibile in modo che l'utente possa spostare e ridimensionare la finestra usando il mouse. Il movimento del cursore è limitato all'area dei monitoraggi, quindi è sempre visibile. Le icone della shell sono posizionate sullo stesso monitor della barra delle applicazioni e la barra delle applicazioni può trovarsi su qualsiasi monitoraggio, vedere [più considerazioni sul monitoraggio per i programmi meno recenti](multiple-monitor-considerations-for-older-programs.md).

Un sistema A più monitor influiscono su determinate combinazioni di chiavi. La combinazione di tasti ALT + STAMP acquisisce uno snapshot della finestra in primo piano, come sempre. Tuttavia, la chiave Stamp acquisisce uno snapshot del monitoraggio con il mouse. La combinazione di tasti CTRL + STAMP acquisisce uno snapshot dell'intero schermo virtuale, vedere [lo schermo virtuale](the-virtual-screen.md).

Il supporto per più monitor non influisce sulle prestazioni delle applicazioni quando viene eseguito in un unico ambiente di visualizzazione. Ovvero, quando viene eseguito in un unico sistema di visualizzazione, nessun overhead aggiuntivo sarà presente nel codice delle operazioni grafiche ad alte prestazioni. Tuttavia, in un sistema a più monitor, le prestazioni sono leggermente interessate se un'applicazione viene eseguita solo su uno dei dispositivi grafici. Inoltre, le prestazioni possono essere influenzate significativamente se un'applicazione si estende su più visualizzazioni, in particolare per le operazioni a elevato utilizzo di grafica.

*Schermo intero* è una funzionalità fornita dal sistema operativo che consente a un utente di impostare un'applicazione in uno stato speciale in cui l'applicazione può accedere direttamente all'hardware della grafica VGA. Si tratta di una funzionalità chiave per giochi e altre applicazioni incentrate su grafica che richiedono prestazioni elevate. Inoltre, viene spesso utilizzata dagli sviluppatori per la modifica del testo poiché consente lo scorrimento del testo molto rapido.

In un ambiente con più monitor, solo un dispositivo grafico può essere compatibile con VGA. Si tratta di una limitazione dell'hardware del computer che richiede che un solo dispositivo risponda a qualsiasi indirizzo hardware. Poiché lo standard di compatibilità hardware VGA richiede indirizzi hardware specifici, in un computer può essere presente un solo dispositivo grafico VGA e solo questo dispositivo può rispondere fisicamente agli indirizzi VGA. Pertanto, le applicazioni che richiedono la visualizzazione a schermo intero verranno eseguite solo sul dispositivo specifico che supporta la compatibilità hardware VGA.

In questa panoramica vengono fornite informazioni sui seguenti argomenti.

-   [Schermata virtuale](the-virtual-screen.md)
-   [HMONITOR e il contesto di dispositivo](hmonitor-and-the-device-context.md)
-   [Enumerazione e controllo di visualizzazione](enumeration-and-display-control.md)
-   [Più metriche del sistema di monitoraggio](multiple-monitor-system-metrics.md)
-   [Uso di più monitor come visualizzazioni indipendenti](using-multiple-monitors-as-independent-displays.md)
-   [Colori su più monitor di visualizzazione](colors-on-multiple-display-monitors.md)
-   [Posizionamento di oggetti su più monitor di visualizzazione](positioning-objects-on-multiple-display-monitors.md)
-   [Più applicazioni di monitoraggio su sistemi diversi](multiple-monitor-applications-on-different-systems.md)
-   [Considerazioni su più monitor per i programmi precedenti](multiple-monitor-considerations-for-older-programs.md)

 

 



