---
description: Il dispositivo scanner Windows Image Acquisition (WIA) viene implementato come albero gerarchico di oggetti IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivi scanner WIA in WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751759"
---
# <a name="wia-scanner-devices-in-wia-10"></a>Dispositivi scanner WIA in WIA 1,0

> [!Note]  
> Questo argomento illustra l'albero del dispositivo dello scanner per le applicazioni che usano il servizio Windows Image Acquisition (WIA) 1,0, supportato in Windows XP o versioni precedenti. Per informazioni sull'albero dei dispositivi degli elementi di acquisizione immagini Windows (WIA) 2,0, supportati in Windows Vista o versioni successive, vedere [informazioni sull'albero degli elementi di IWiaItem2](-wia-about-item-tree.md).

 

Il dispositivo scanner Windows Image Acquisition (WIA) viene implementato come albero gerarchico di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . Dall'elemento radice è possibile che un'applicazione:

-   Funzionalità di query scanner
-   Impostare le proprietà del dispositivo scanner
-   Controllare il feeder di documenti

Un dispositivo scanner WIA è diverso da un dispositivo della fotocamera WIA perché, in generale, non archivia più immagini in memoria.

Sotto l'elemento radice, un oggetto scanner tipico ha un singolo oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) che rappresenta la funzionalità di raccolta dati del dispositivo, l'elemento di analisi. Questo elemento ha il flag [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) impostato per indicare che i trasferimenti di dati in questo elemento sono possibili. Un'applicazione imposta un'analisi impostando le proprietà dell'elemento Scan, quindi esegue l'analisi e trasferisce i dati utilizzando un'interfaccia di trasferimento dati.

Il diagramma seguente illustra l'implementazione di WIA per uno scanner tipico:

![implementazione WIA di uno scanner tipico](images/wiscantr.gif)

Un tipico scanner duplex viene rappresentato in WIA con un oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . Viene eseguito l'accesso ai dati della pagina iniziale e in sequenza a un trasferimento dati per pagina. La rappresentazione di uno scanner duplex è pertanto identica alla rappresentazione di uno scanner tipico.

Uno scanner scorrevole in grado di analizzare più diapositive in un'unica operazione di analisi rappresenta ciascuna immagine separata come oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) separato.

Il diagramma seguente illustra la rappresentazione WIA di uno scanner diapositiva:

![scanner diapositiva](images/wislscan.gif)

 

 



