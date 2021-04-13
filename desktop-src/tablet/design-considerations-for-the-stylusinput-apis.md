---
description: Panoramica delle considerazioni per la progettazione di un'applicazione che usa le API (Application Programming Interface) di StylusInput.
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: Considerazioni di progettazione per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff526d8e073f00156730d79ea2caf1a02c5e5af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348686"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>Considerazioni di progettazione per l'API StylusInput

Di seguito sono riportate considerazioni di progettazione per l'API StylusInput.

-   È possibile aggiornare la proprietà [**WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e la proprietà [**ClipRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle) dell'oggetto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) mentre la penna è inattiva. Questa operazione può essere utile quando si vuole avere un'area di disegno dinamica mentre l'applicazione raccoglie l'input penna.
-   Per ottimizzare il riutilizzo e la manutenzione del codice del plug-in, i plug-in non devono effettuare chiamate direttamente all'applicazione, ma devono usare l'oggetto [**CustomStylusData**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) ([CustomeStylusData](/previous-versions/ms824747(v=msdn.10)) nel codice gestito) per comunicare con l'applicazione.
-   Le raccolte di plug-in dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) sono ordinate. La posizione relativa dei plug-in all'interno di queste raccolte può essere molto importante. È ad esempio possibile aggiungere un plug-in che modifica le informazioni sui pacchetti alla raccolta di plug-in sincrona prima di un plug-in di renderer dinamico.
-   La possibilità di aggiungere dati dello stilo personalizzati al flusso di dati della penna del Tablet PC deve essere utilizzata in modo sporadico. Usare questa funzionalità solo se un altro plug-in deve ricevere queste informazioni come parte del flusso di dati. Evitare inoltre di aggiungere dati stilo personalizzati in risposta ad altri dati dello stilo personalizzati in arrivo nel plug-in, in quanto questo può creare un ciclo infinito.
-   È possibile modificare le raccolte di plug-in mentre l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato; Questo può tuttavia rendere più difficile la stima del comportamento dell'applicazione. Quando si aggiunge un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il plug-in Microsoft. StylusInput. IStylusSyncPlugin. Metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) (il metodo [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) nel codice gestito). Quando si rimuove un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** chiama il metodo [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) del plug-in, ovvero il metodo [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) nel codice gestito. In questo modo il plug-in è in grado di mantenere lo stato appropriato senza dover controllare la proprietà [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled) dell'oggetto **RealTimeStylus** . Quando si aggiunge un plug-in mentre l'oggetto **RealTimeStylus** è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non contenere informazioni sufficienti per stabilire adeguatamente il contesto dei dati iniziali. Ad esempio, il plug-in appena aggiunto potrebbe iniziare a ricevere i dati dei pacchetti da una penna a metà tratto. Analogamente, quando un plug-in è stato rimosso mentre l'oggetto **RealTimeStylus** è abilitato, i dati del plug-in ricevuti dal plug-in potrebbero non essere sufficienti per completare l'elaborazione dei dati.
    > [!Note]  
    > Per la stabilità complessiva, reimpostare lo stato interno di un plug-in quando viene chiamato il metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) .

     

-   L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione se un plug-in modifica la raccolta di plug-in a cui è collegata. Questa situazione si verifica solo quando il plug-in lo fa mentre viene chiamato dall'oggetto **RealTimeStylus** come membro di tale raccolta.

 

 
