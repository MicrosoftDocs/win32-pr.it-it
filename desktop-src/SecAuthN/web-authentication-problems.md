---
description: In questo argomento vengono descritti i suggerimenti per la risoluzione dei problemi relativi all'utilizzo delle API del broker di autenticazione Web per le pagine Web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problemi relativi all'autenticazione Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554571"
---
# <a name="web-authentication-problems"></a>Problemi relativi all'autenticazione Web

In questo argomento vengono descritti i suggerimenti per la risoluzione dei problemi relativi all'utilizzo delle API del broker di autenticazione Web per le pagine Web.

-   [Log operativi](#operational-logs)
-   [Uso di Fiddler con il broker di autenticazione Web](#using-fiddler-with-web-authentication-broker)
-   [Argomenti correlati](#related-topics)

## <a name="operational-logs"></a>Log operativi

Spesso, per identificare l'elemento problematico puoi usare i log operativi. È disponibile un canale di log eventi dedicato Microsoft-Windows-WebAuth \\ operativo che consente agli sviluppatori di siti Web di comprendere il modo in cui vengono elaborate le pagine Web dal broker di autenticazione Web. Per abilitarla, avviare eventvwr.exe e abilitare il log operativo sotto l'applicazione e servizi \\ Microsoft \\ Windows \\ WebAuth. Inoltre, il broker di autenticazione Web Accoda una stringa univoca alla stringa agente utente per identificarsi sul server Web. Tale stringa è "MSAuthHost/1.0". Ricorda che il numero di versione può cambiare in futuro, pertanto il tuo codice non deve dipendere da tale valore. Di seguito è riportato un esempio di stringa agente utente completa:

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

Esempio di utilizzo dei log operativi

1.  Abilitare i log operativi
2.  Eseguire contoso Social Application![log operativi webauth visualizzati nel visualizzatore eventi](images/wab-figure15.png)
3.  Le voci di log generate possono essere usate per comprendere in modo più dettagliato il comportamento del broker di autenticazione Web. In questo caso, tali voci possono includere:
    -   Inizio esplorazione: registra l'avvio di AuthHost e contiene informazioni sugli URL di inizio e di fine.
    -   ![illustra in dettaglio l'inizio dell'esplorazione](images/wab-figure16.png)
    -   Completamento esplorazione: registra il completamento del caricamento di una pagina Web.
    -   Tag META: registra il momento del rilevamento di un tag META, inclusi i dettagli.
    -   Termine esplorazione: termine dell'esplorazione da parte dell'utente.
    -   Errore di esplorazione: AuthHost rileva un errore di esplorazione per l'URL che include HttpStatusCode.
    -   Fine esplorazione: rilevamento dell'URL di fine.

## <a name="using-fiddler-with-web-authentication-broker"></a>Uso di Fiddler con il broker di autenticazione Web

Il debugger Web Fiddler può essere usato con le app di Windows 8.

1.  Poiché AuthHost viene eseguito nel proprio contenitore di app per garantire la funzionalità di rete privata, devi impostare una chiave del Registro di sistema: Editor del Registro di sistema di Windows versione 5.00

    **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001<dl> <dt>

                     Data type
</dt> <dd>                     DWORD</dd> </dl>

2.  Aggiungi una regola per AuthHost in quanto esso genera il traffico in uscita.
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  Aggiungi una regola firewall per il traffico in entrata in Fiddler.

Per altre informazioni, vedere [il Blog sull'uso del debugger Web Fiddler con le app di Windows Store](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni relative allo sviluppo di pagine Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Domande frequenti sul broker di autenticazione Web](faq-for-web-authentication-broker.md)
</dt> <dt>

[App di esempio SDK Web Authentication broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
