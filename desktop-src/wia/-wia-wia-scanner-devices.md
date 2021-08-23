---
description: Il Windows scanner WIA (Image Acquisition) viene implementato come albero gerarchico di oggetti IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivi scanner WIA in WIA 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd22cc9fe330a3acf231034b61c72178f3b282cb9e66a1f455d4b6939a1c3cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592673"
---
# <a name="wia-scanner-devices-in-wia-10"></a>Dispositivi scanner WIA in WIA 1.0

> [!Note]  
> Questo argomento illustra l'albero dei dispositivi dello scanner per le applicazioni che usano il servizio Windows Image Acquisition (WIA) 1.0 (supportato in Windows XP o versioni precedenti). Per informazioni sull'albero dei dispositivi degli elementi di Windows Image Acquisition (WIA) 2.0 (supportati in Windows Vista o versioni successive), vedere About the IWiaItem2 Item Tree (Informazioni sull'albero degli elementi [IWiaItem2).](-wia-about-item-tree.md)

 

Il Windows scanner WIA (Image Acquisition) viene implementato come albero gerarchico di [**oggetti IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) Dall'elemento radice un'applicazione può:

-   Funzionalità dello scanner di query
-   Impostare le proprietà del dispositivo scanner
-   Controllare l'alimentatore di documenti

Un dispositivo scanner WIA è diverso da un dispositivo fotocamera WIA perché, in generale, non archivia più immagini in memoria.

Sotto l'elemento radice, un tipico oggetto scanner ha un singolo [**oggetto IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) che rappresenta la funzionalità di raccolta dei dati del dispositivo, l'elemento di analisi. Questo elemento ha il flag [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) impostato per indicare che i trasferimenti di dati su questo elemento sono possibili. Un'applicazione configura un'analisi impostando le proprietà dell'elemento di analisi, quindi esegue l'analisi e trasferisce i dati usando un'interfaccia di trasferimento dati.

Il diagramma seguente illustra l'implementazione di WIA per uno scanner tipico:

![Implementazione wia di uno scanner tipico](images/wiscantr.gif)

Un tipico scanner duplex è rappresentato in WIA con un [**oggetto IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) Ai dati anteriore e a pagina posteriore si accede in sequenza a un trasferimento di dati per pagina. Di conseguenza, la rappresentazione di uno scanner duplex è identica alla rappresentazione di uno scanner tipico.

Uno scanner di diapositive in grado di analizzare più diapositive in una singola operazione di analisi rappresenta ogni immagine separata come oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) separato.

Il diagramma seguente illustra la rappresentazione WIA di uno scanner di diapositive:

![scanner di diapositive](images/wislscan.gif)

 

 



