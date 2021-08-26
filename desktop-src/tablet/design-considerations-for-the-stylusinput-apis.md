---
description: Panoramica delle considerazioni per la progettazione di un'applicazione che usa le API (Application Programming Interface) StylusInput.
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: Considerazioni sulla progettazione per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd97a5bad203dd23611acf3d6cb07bead1e1744a10b9ac39afe8a53e65597d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936631"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>Considerazioni sulla progettazione per l'API StylusInput

Di seguito sono riportate considerazioni di progettazione per l'API StylusInput.

-   È possibile aggiornare la [**proprietà WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e la proprietà [**ClipRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle) dell'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) mentre la penna è in giù. Ciò può essere utile quando si vuole avere un'area di disegno dinamica mentre l'applicazione sta raccogliendo l'input penna.
-   Per ottimizzare il riutilizzo e la manutenzione del codice plug-in, i plug-in non devono effettuare chiamate direttamente all'applicazione, ma devono usare [**l'oggetto CustomStylusData**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) [(oggetto CustomeStylusData](/previous-versions/ms824747(v=msdn.10)) nel codice gestito) per comunicare con l'applicazione.
-   Le raccolte plug-in dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) vengono ordinate. La posizione relativa dei plug-in all'interno di queste raccolte può essere molto importante. Ad esempio, è probabile che un plug-in che modifica le informazioni sui pacchetti venga aggiunto alla raccolta di plug-in sincroni prima di un plug-in del renderer dinamico.
-   La possibilità di aggiungere dati dello stilo personalizzati al flusso di dati della penna del tablet deve essere usata con parsimonio. Usare questa funzionalità solo se un altro plug-in deve ricevere queste informazioni come parte del flusso di dati. Evitare inoltre di aggiungere dati dello stilo personalizzati in risposta ad altri dati dello stilo personalizzati in arrivo nel plug-in, in quanto ciò può creare un ciclo infinito.
-   Le raccolte di plug-in possono essere modificate mentre [**l'oggetto RealTimeStylus**](realtimestylus-class.md) è abilitato. Tuttavia, ciò può rendere il comportamento dell'applicazione più difficile da prevedere. Quando viene aggiunto un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama Microsoft.StylusInput.IStylusSyncPlugin del plug-in. Metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) [(metodo Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) nel codice gestito). Quando un plug-in viene rimosso mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il metodo [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) del plug-in (metodo [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) nel codice gestito). Ciò consente al plug-in di mantenere lo stato corretto senza dover controllare la [**proprietà Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled) dell'oggetto **RealTimeStylus.** Quando un plug-in viene aggiunto mentre l'oggetto **RealTimeStylus** è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non contenere informazioni sufficienti per stabilire in modo adeguato il contesto dei dati iniziali. Ad esempio, il plug-in appena aggiunto potrebbe iniziare a ricevere i dati del pacchetto da una penna a metà corsa. Analogamente, quando un plug-in viene rimosso mentre l'oggetto **RealTimeStylus** è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non essere sufficienti per completare l'elaborazione dei dati.
    > [!Note]  
    > Per la stabilità complessiva, reimpostare lo stato interno di un plug-in quando viene chiamato il metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled)

     

-   [**L'oggetto RealTimeStylus**](realtimestylus-class.md) genera un'eccezione se un plug-in modifica la raccolta di plug-in a cui è collegato. Ciò si verifica solo quando il plug-in esegue questa operazione mentre viene chiamato dall'oggetto **RealTimeStylus** come membro di tale raccolta.

 

 
