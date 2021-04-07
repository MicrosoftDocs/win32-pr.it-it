---
description: Panoramica delle considerazioni relative al threading quando si usa il Application Programming Interface di StylusInput (API).
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Considerazioni relative al threading per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530ac95fdf0e74e30c83a437b6ed573d03bb2c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103881933"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Considerazioni relative al threading per l'API StylusInput

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) è progettato per fornire l'accesso in tempo reale al flusso di dati dalla penna del Tablet PC. I plug-in, ovvero gli oggetti che implementano l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , possono essere aggiunti a un oggetto **RealTimeStylus** . I plug-in sincroni vengono generalmente chiamati direttamente dall'oggetto **RealTimeStylus** su un thread ad alta priorità, mentre i plug-in asincroni vengono in genere chiamati sul thread dell'interfaccia utente dell'applicazione. Creare o usare plug-in sincroni per le attività che richiedono l'accesso in tempo reale al flusso di dati e non richiedono un calcolo, ad esempio il filtro dei pacchetti. Creare o usare plug-in asincroni per le attività che non richiedono l'accesso in tempo reale al flusso di dati, ad esempio la raccolta di input penna.

Poiché i dati del plug-in per la raccolta di plug-in asincrona dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) sono accodati, i plug-in asincroni possono ricevere dati prima di ricevere una chiamata al metodo [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) , ma dopo che l'oggetto **RealTimeStylus** è stato disabilitato. Si noti che alcuni metodi e proprietà dell'oggetto **RealTimeStylus** generano un'eccezione se l'oggetto **RealTimeStylus** è disabilitato.

I metodi di interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) seguenti possono chiamare su un thread diverso dal thread di dati della penna del Tablet PC.

-   I metodi [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) e [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) vengono chiamati sul thread che aggiorna la proprietà [Enabled](/previous-versions/ms585380(v=vs.100)) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) o che aggiunge o rimuove il plug-in mentre l'oggetto **RealTimeStylus** è abilitato.
-   Il metodo [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) viene chiamato sul thread che chiama il metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) .
-   Il metodo [Error](/previous-versions/ms824754(v=msdn.10)) viene chiamato sul thread in cui è in esecuzione il plug-in sincrono quando viene generata un'eccezione.

Per interagire con l'applicazione da un plug-in sincrono, usare il metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e gestire i dati dello stilo personalizzati in uno dei plug-in asincroni. Se si effettua una chiamata sincrona a un altro thread da un plug-in sincrono, è possibile bloccare l'oggetto **RealTimeStylus** e quindi bloccare la raccolta di input penna.

Alcune attività possono essere richieste dal punto di vista del calcolo, ma richiedono comunque l'accesso in tempo reale al flusso di dati della penna del tablet, ad esempio per il riconoscimento dei movimenti a più tratti. Le API StylusInput forniscono un modello [**RealTimeStylus**](realtimestylus-class.md) a cascata che consente di usare due oggetti **RealTimeStylus** , ciascuno dei quali chiama i relativi plug-in sincroni da thread diversi. Per ulteriori informazioni sul modello **RealTimeStylus** a cascata, vedere [il modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md).

> [!Note]  
> Non è possibile aggiungere l'oggetto [**RealTimeStylus**](realtimestylus-class.md) a una finestra o a un controllo in un processo diverso.

 

Per ulteriori informazioni sulle considerazioni relative al threading per Tablet PC in generale, vedere [considerazioni sul threading del Tablet PC](tablet-pc-threading-considerations.md) .

 

 
