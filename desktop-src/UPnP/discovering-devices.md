---
title: Individuazione di dispositivi
description: È possibile cercare i dispositivi in tre modi per tipo, da UDN e da ricerca asincrona (Ricerca per tipo di dispositivo).
ms.assetid: 511fb119-ad4e-406a-8a1e-fb508eceff2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055d08db76edd5bcc5591d3254613462c00fc974
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856750"
---
# <a name="discovering-devices"></a>Individuazione di dispositivi

È possibile cercare i dispositivi in tre modi: per tipo, per UDN e per ricerca asincrona (Ricerca per tipo di dispositivo).

![finestra Individua dispositivi](images/ucp-disc.png)

**Per individuare i dispositivi**

1.  Selezionare il tipo di ricerca da usare: **trova per tipo**, **trova per UDN** o ricerca **asincrona**.
2.  Consente di selezionare il tipo di dispositivo o il UDN che si desidera trovare dall'elenco (per le ricerche in base al tipo o UDN). Il contenuto dell'elenco è basato sul contenuto del udn.txt e devtype.txt file modificati in precedenza.
3.  Fare clic su **Avvia individuazione**. La ricerca è stata avviata. I risultati vengono visualizzati nell'elenco **dispositivi trovati** . Se non vengono trovati dispositivi, viene visualizzato un messaggio che indica questa condizione. Lo stato dello stato di avanzamento della ricerca viene visualizzato nel campo **stato** .

Quando si usa la ricerca asincrona, i nuovi dispositivi trovati vengono visualizzati nell'elenco **dispositivi trovati** e nella barra di **stato** . Al termine della ricerca asincrona, nella barra di **stato** viene visualizzato un messaggio di nota. Tuttavia, poiché una ricerca asincrona viene eseguita fino a quando non viene arrestata manualmente, i nuovi dispositivi vengono visualizzati nell'elenco **dispositivi trovati** e nella barra di **stato** quando i dispositivi vengono visualizzati nella rete.

Dopo aver individuato i dispositivi, è possibile [controllarli](controlling-a-device.md).

 

 




