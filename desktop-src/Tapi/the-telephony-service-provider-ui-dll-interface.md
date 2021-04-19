---
description: In telefonia Microsoft i provider di servizi di telefonia vengono eseguiti in un processo separato dalle applicazioni di telefonia.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: Interfaccia DLL dell'interfaccia utente del provider di servizi di telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311853"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>Interfaccia DLL dell'interfaccia utente del provider di servizi di telefonia

In telefonia Microsoft i provider di servizi di telefonia vengono eseguiti in un processo separato dalle applicazioni di telefonia. I provider di servizi comunicano con TAPISRV tramite l'interfaccia TSPI (telefonia Service Provider Interface) ed eseguono nel processo. interfaccia delle applicazioni per TAPI, che vengono caricati nel contesto dell'applicazione.

I componenti di TAPI utilizzano vari meccanismi di comunicazione interprocesso per trasferire richieste di funzioni e messaggi tra le applicazioni e i provider di servizi. È possibile che le applicazioni e i provider di servizi siano in esecuzione non solo in processi distinti, ma in sistemi completamente distinti. I provider di servizi non possono pertanto visualizzare le finestre di dialogo nel processo o anche nel computer in cui sono in esecuzione; L'interfaccia utente deve essere richiamata dall'interno del contesto dell'applicazione, nel computer in cui è in esecuzione l'applicazione.

In questa sezione viene definito il meccanismo mediante il quale vengono caricate e richiamate le funzioni dell'interfaccia utente del provider di servizi nel contesto dell'applicazione Un meccanismo è definito anche da quali provider di servizi possono aprire spontaneamente le finestre di dialogo nel contesto dell'applicazione quando non sono altrimenti previste dall'applicazione. Un esempio di questo secondo caso è la finestra di dialogo **Talk/hangup** visualizzata da un provider di servizi del modem dati quando il modem viene usato come dialer per le chiamate vocali interattive e all'utente deve essere richiesto di prelevare il telefono e informare il provider di servizi quando inserire il modem OnHook.

 

 



