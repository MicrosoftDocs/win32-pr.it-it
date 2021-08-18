---
description: È possibile acconsentire esplicitamente a un computer Microsoft Update servizio e quindi registrare il servizio con Aggiornamenti automatici.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In da Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d034f0b224d8170a52ce359589693c601cb9598d716e9663493e8ac99edf2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994280"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In da Microsoft Update

È possibile acconsentire esplicitamente a un computer Microsoft Update servizio e quindi registrare il servizio con Aggiornamenti automatici.

L'esempio di scripting in questo argomento illustra come usare Windows Update Agent (WUA) per registrare il servizio Microsoft Update con Aggiornamenti automatici. In alternativa, per registrare il servizio, l'utente può visitare Microsoft Update.

Prima di provare a eseguire questo esempio, verificare che la versione di WUA installata nel computer sia 7.0.6000 o successiva. Per altre informazioni su come determinare la versione di WUA installata, vedere [Determinazione della versione corrente di WUA.](determining-the-current-version-of-wua.md)

## <a name="example"></a>Esempio

L'esempio di scripting seguente illustra come usare l'agente di aggiornamento di Windows (WUA) per registrare il servizio Microsoft Update con Aggiornamenti automatici. L'esempio consente l'elaborazione posticipata o offline, se necessario.

> [!IMPORTANT]
> Questo script ha lo scopo di illustrare l'uso delle API dell'agente di aggiornamento di Windows e fornisce un esempio di come gli sviluppatori possono usare queste API per risolvere i problemi. Questo script non è da intendersi come codice di produzione e lo script stesso non è supportato da Microsoft (anche se sono supportate le API Windows Update Agent sottostanti).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



Nelle versioni precedenti di WUA (versione minima wua 7.0.6000), è possibile semplificare il processo di consenso esplicito usando un'impostazione del Registro di sistema. Dopo aver configurato la chiave del Registro di sistema e i valori, Microsoft Update il processo di consenso esplicito alla successiva esecuzione di una ricerca da parte di WUA. Il processo di consenso esplicito può essere attivato da Aggiornamenti automatici o da un chiamante API.

Ad esempio, il percorso completo della chiave del Registro di sistema e i valori da impostare per il processo di consenso esplicito sono i seguenti:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsUpdate** \\ **PendingServiceRegistration** \\ **7971f918-a847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = My App

**RegisterWithAU** = 1

> [!Note]
>
> La chiave del Registro di sistema viene rispettata una sola volta quando WUA viene aggiornato da una versione precedente alla 7.0.6000 alla versione 7.0.6000 o a una versione successiva. È consigliabile sovrascrivere i valori esistenti del Registro di sistema perché la sovrascrittura dei valori può modificare il risultato di una richiesta di registrazione del servizio precedente.
>
> La creazione di questa chiave del Registro di sistema richiede credenziali amministrative. Per Windows Vista, il chiamante deve creare la chiave del Registro di sistema in un processo con privilegi elevati.

 

 

 



