---
description: È possibile scegliere un computer nel servizio Microsoft Update e quindi registrare il servizio con Aggiornamenti automatici.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128271"
---
# <a name="opt-in-to-microsoft-update"></a>Opt-In Microsoft Update

È possibile scegliere un computer nel servizio Microsoft Update e quindi registrare il servizio con Aggiornamenti automatici.

Nell'esempio di scripting in questo argomento viene illustrato come utilizzare Windows Update Agent (WUA) per registrare il servizio Microsoft Update con Aggiornamenti automatici. In alternativa, per registrare il servizio, l'utente può visitare Microsoft Update.

Prima di provare a eseguire l'esempio, verificare che la versione di WUA installata nel computer sia la versione 7.0.6000 o una versione successiva. Per ulteriori informazioni su come determinare la versione di WUA installata, vedere [determinazione della versione corrente di WUA](determining-the-current-version-of-wua.md).

## <a name="example"></a>Esempio

Nell'esempio di scripting seguente viene illustrato come utilizzare l'agente di Windows Update (WUA) per registrare il servizio Microsoft Update con Aggiornamenti automatici. L'esempio consente l'elaborazione posticipata o offline, se necessario.

> [!IMPORTANT]
> Questo script ha lo scopo di illustrare l'uso delle API dell'agente Windows Update e fornisce un esempio di come gli sviluppatori possono usare queste API per risolvere i problemi. Questo script non è destinato al codice di produzione e lo script non è supportato da Microsoft (anche se sono supportate le API di Windows Update Agent sottostanti).

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



Nelle versioni precedenti di WUA (una versione minima di WUA di 7.0.6000), è possibile semplificare il processo di consenso esplicito usando un'impostazione del registro di sistema. Dopo la configurazione della chiave e dei valori del registro di sistema, il Microsoft Update processo di consenso esplicito si verifica alla successiva esecuzione di una ricerca da parte di WUA. Il processo di consenso esplicito può essere attivato da Aggiornamenti automatici o da un chiamante dell'API.

Il percorso completo della chiave del registro di sistema e i valori da impostare per il processo di consenso esplicito, ad esempio, sono i seguenti:

**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **PendingServiceRegistration** \\ **7971f918-A847-4430-9279-4a52d1efe18d**

**ClientApplicationID** = app personale

**RegisterWithAU** = 1

> [!Note]
>
> La chiave del registro di sistema viene rispettata una volta solo quando WUA viene aggiornato da una versione precedente alla versione 7.0.6000 alla versione 7.0.6000 o a una versione successiva. Quando si sovrascrivono i valori del registro di sistema esistenti, è consigliabile utilizzare la massima discrezione, in quanto la sovrascrittura dei valori può modificare il risultato di una richiesta di registrazione
>
> Per creare questa chiave del registro di sistema sono necessarie credenziali amministrative. Per Windows Vista, il chiamante deve creare la chiave del registro di sistema in un processo con privilegi elevati.

 

 

 



