---
description: In Telefonia Microsoft i provider di servizi di telefonia vengono eseguiti in un processo separato dalle applicazioni di telefonia.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: Interfaccia DLL dell'interfaccia DLL del provider di servizi di telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6aea6dfd68773dcd96602803230bd160552eab1414135b75a3205a0fac88dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119403941"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>Interfaccia DLL dell'interfaccia DLL del provider di servizi di telefonia

In Telefonia Microsoft i provider di servizi di telefonia vengono eseguiti in un processo separato dalle applicazioni di telefonia. I provider di servizi comunicano con TAPISRV tramite l'interfaccia del provider di servizi di telefonia (TSPI) ed eseguono il processo; interfaccia delle applicazioni per TAPI, che vengono caricate nel contesto dell'applicazione.

I componenti di TAPI usano vari meccanismi di comunicazione interprocesso per trasmettere richieste di funzioni e messaggi tra applicazioni e provider di servizi. Le applicazioni e i provider di servizi possono essere in esecuzione non solo in processi separati, ma in sistemi completamente separati. I provider di servizi non possono pertanto visualizzare finestre di dialogo nel processo o anche nel computer in cui sono in esecuzione. L'interfaccia utente deve essere richiamata dall'interno del contesto dell'applicazione, nel computer in cui è in esecuzione l'applicazione.

Questa sezione definisce il meccanismo tramite il quale le funzioni dell'interfaccia utente del provider di servizi vengono caricate e richiamate all'interno del contesto dell'applicazione. Viene inoltre definito un meccanismo tramite il quale i provider di servizi possono aprire finestre di dialogo nel contesto dell'applicazione quando non sarebbero altrimenti previste dall'applicazione. Un esempio di questo secondo caso è la finestra di dialogo **Talk/Hangup** visualizzata da un provider di servizi modem dati quando il modem viene usato come dialer per le chiamate vocali interattive e all'utente deve essere detto di prelevare il telefono e informare il provider di servizi quando posizionare il modem onhook.

 

 



