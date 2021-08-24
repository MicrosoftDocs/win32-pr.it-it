---
description: Panoramica delle considerazioni sul threading quando si usa l'API StylusInput.
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Considerazioni sul threading per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f9a26da86295a322d926278eda87388c0105132eafd2dfa3d7a9f6c6655e48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819641"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Considerazioni sul threading per l'API StylusInput

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) è progettato per fornire l'accesso in tempo reale al flusso di dati dalla penna del tablet. I plug-in, gli oggetti che implementano l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) possono essere aggiunti a un **oggetto RealTimeStylus.** I plug-in sincroni vengono in genere chiamati direttamente dall'oggetto **RealTimeStylus** in un thread ad alta priorità, mentre i plug-in asincroni vengono in genere chiamati nel thread dell'interfaccia utente dell'applicazione. Creare o usare plug-in sincroni per le attività che richiedono l'accesso in tempo reale al flusso di dati e non vengono eseguite dal calcolo, ad esempio il filtro dei pacchetti. Creare o usare plug-in asincroni per le attività che non richiedono l'accesso in tempo reale al flusso di dati, ad esempio la raccolta input penna.

Poiché i dati del plug-in per la raccolta di plug-in asincroni dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) vengono accodati, i plug-in asincroni possono ricevere dati prima di ricevere una chiamata al relativo metodo [RealTimeStylusDisabled,](/previous-versions/ms824774(v=msdn.10)) ma dopo la disabilitazione **dell'oggetto RealTimeStylus.** Si noti che alcuni metodi e proprietà **dell'oggetto RealTimeStylus** generano un'eccezione se l'oggetto **RealTimeStylus** è disabilitato.

I metodi [**di interfaccia IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) seguenti possono chiamare su un thread diverso dal thread di dati della penna del tablet.

-   I metodi [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) e [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) vengono chiamati sul thread che aggiorna la proprietà [Enabled](/previous-versions/ms585380(v=vs.100)) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) o aggiunge o rimuove il plug-in mentre l'oggetto **RealTimeStylus** è abilitato.
-   Il [metodo CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) viene chiamato sul thread che chiama il metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) dell'oggetto [**RealTimeStylus.**](realtimestylus-class.md)
-   Il [metodo Error](/previous-versions/ms824754(v=msdn.10)) viene chiamato sul thread in cui è in esecuzione il plug-in sincrono quando genera un'eccezione.

Per interagire con l'applicazione da un plug-in sincrono, usare il metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e gestire i dati dello stilo personalizzati in uno dei plug-in asincroni. Se si effettua una chiamata sincrona a un altro thread da un plug-in sincrono, è possibile bloccare l'oggetto **RealTimeStylus** e quindi bloccare la raccolta di input penna.

Alcune attività possono essere impegnative dal punto di vista del calcolo, ma richiedono comunque l'accesso in tempo reale al flusso di dati della penna del tablet, ad esempio per il riconoscimento dei movimenti a più sequenze. Le API StylusInput forniscono un modello [**RealTimeStylus**](realtimestylus-class.md) a catena che consente di usare due oggetti **RealTimeStylus,** ognuno dei quali chiama i plug-in sincroni da thread diversi. Per altre informazioni sul modello **RealTimeStylus** a catena, vedere [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

> [!Note]  
> Non è possibile collegare [**l'oggetto RealTimeStylus**](realtimestylus-class.md) a una finestra o a un controllo in un processo diverso.

 

Per altre informazioni generali sulle considerazioni sul threading per Tablet PC, vedere [Considerazioni sul threading per Tablet PC](tablet-pc-threading-considerations.md)

 

 
