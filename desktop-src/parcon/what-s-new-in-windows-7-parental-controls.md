---
description: Offre una panoramica delle modifiche apportate ai controlli Windows genitori introdotti in Windows 7.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Novità di Windows 7 Controllo genitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7b545c6791d286e51ae7a36ed65623d1697a7e742b1ae956e3ef4aaf3425e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951821"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Novità di Windows 7 Controllo genitori

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Panoramica delle modifiche del controllo genitori per Windows 7

Lo scopo di questo documento è fornire una panoramica delle modifiche apportate al controllo genitori di Windows introdotte in Windows 7 e consentire ai provider di soluzioni di controllo genitori di terze parti di sfruttare questi cambiamenti. Questo documento presuppone la familiarità dei lettori con controllo genitori per Windows Vista e rifletterà solo le modifiche apportate a questa funzionalità in Windows 7 rilevanti per lo sviluppo di soluzioni di controllo genitori di terze parti. Un aggiornamento completo della documentazione di MSDN Windows controllo genitori verrà seguito in un secondo momento.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Principali decisioni di progettazione per Windows 7 modifiche del controllo genitori

Le modifiche al controllo genitori introdotte in Windows 7 continuano l'obiettivo generale di promuovere la coesistenza delle soluzioni di controllo genitori di terze parti con la funzionalità in- È necessario apportare le modifiche seguenti:

-   Rimozione dei filtri Web e dei report attività dalla funzionalità di controllo genitori in-box. I controlli genitori predefiniti forniscono restrizioni principali offline implementate da Microsoft, ad esempio limiti di tempo, restrizioni delle applicazioni e restrizioni di gioco. Il filtro Web, la creazione di report sulle attività e altre funzionalità possono essere forniti da soluzioni Microsoft o di terze parti per il controllo genitori. Ad esempio, Windows Live Family Safety offre funzionalità di filtro Web, gestione remota e monitoraggio delle attività, nonché la gestione dei contatti per tutte le Windows Live.
-   Abilitazione di soluzioni di terze parti per sostituire l'interfaccia utente di configurazione del provider in-box, continuando comunque a basarsi sull'implementazione predefinita delle restrizioni di tempo, applicazione e gioco.
-   Abilitazione di soluzioni di terze parti che possono essere individuate e abilitate nel computer da un padre o da un guardiano (account amministratore).

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Controlli genitori Modifiche alle Interfaccia utente di primo livello in Windows 7

Windows 7 introduce le modifiche seguenti al controllo genitori Pannello di controllo'interfaccia utente di primo livello:

-   Viene introdotta la sezione Controlli aggiuntivi in cui i controlli che forniscono funzionalità aggiuntive, ad esempio il filtro Web, la creazione di report attività e così via, possono essere selezionati da una casella di riepilogo a discesa. Microsoft o provider di terze parti devono registrare le proprie soluzioni con Windows 7 Controllo genitori perché siano selezionabili dall'elenco a discesa Controlli aggiuntivi. Per informazioni sulla registrazione di una soluzione, vedere Registrazione del provider più avanti in questo argomento.
-   L'immagine del logo del provider attualmente selezionato viene visualizzata nell'angolo superiore destro della pagina.
-   I riquadri utente gestito possono visualizzare un riepilogo delle impostazioni dei genitori fornite dal provider attualmente selezionato.

Il provider attualmente selezionato potrebbe scegliere di usare la propria interfaccia utente per le schermate di Controllo utente per gli utenti gestiti oppure può scegliere di basarsi sull'implementazione WPC predefinita di questa schermata. L'implementazione in-box presenta le modifiche seguenti apportate ai relativi elementi:

-   La sezione relativa ai report attività viene rimossa.
-   Il collegamento per visualizzare i report attività viene rimosso.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Panoramica dell'API Controllo genitori: Windows 7 modifiche

Il meccanismo di integrazione per i provider di soluzioni di terze parti è stato ampliato per consentire:

-   Registrazione del provider. Al momento della registrazione, un provider diventa selezionabile nell'elenco a discesa Controlli aggiuntivi nella schermata controllo genitori Pannello di controllo controllo genitori.
-   Esecuzione di query per il provider attualmente selezionato. Per abilitare questa funzionalità, viene esposta un'interfaccia COM pubblica.
-   Nuovo è anche il set di interfacce COM che devono essere implementate dai provider per consentire:
    -   Abilitazione o disabilitazione del provider tramite WPC dopo la selezione di controlli aggiuntivi da parte dell'utente.
    -   WPC per passare il controllo al provider per configurare le impostazioni di controllo genitori dell'utente gestito.
    -   WPC per eseguire una query sul provider per il riepilogo delle impostazioni di controllo genitori dell'utente gestito.

## <a name="third-party-provider-integration"></a>Integrazione di provider di terze parti

### <a name="provider-registration"></a>Registrazione del provider

Per registrare un nuovo provider con Controllo genitori, è necessario scrivere un valore del Registro di sistema nella chiave Providers Windows Controllo genitori. Il nome del valore è un GUID univoco utilizzato per identificare il provider. I dati del valore saranno un percorso di una chiave del Registro di sistema in **HKEY \_ LOCAL \_ MACHINE** che contiene informazioni sul provider.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Parental Controls
                  Providers
                     {45D63315-0824-4df4-B8A4-EF137D8810D1} = SOFTWARE\Microsoft\Family Safety\WPC\
```

Nel percorso della chiave del Registro di sistema specificato sono previsti i valori seguenti.



| Termine                                                                                                                 | Descrizione                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**<br/>         | Percorso completo di un file binario delle risorse con un ID risorsa negativo per l'immagine del logo del provider (archiviato come **IMAGE \_ BITMAP).**<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**<br/> | Percorso completo di un file binario di risorse con un ID risorsa negativo per il nome del provider. **La lunghezza di DisplayName** non deve superare i 50 caratteri.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**<br/> | Percorso completo di un file binario di risorse con un ID risorsa negativo per la descrizione del provider. La lunghezza della descrizione non deve superare i 200 caratteri.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | ID della classe del provider che implementa IWPCProviderState.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | ID della classe del provider, che implementa IWPCProviderConfig. **StateCLSID** e **ConfigCLSID** possono essere uguali.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | Valore **DWORD facoltativo** diverso da zero che specifica che Windows Parent Controls visualizza un collegamento alla schermata Game Rating System dopo che un provider è stato selezionato come nuovo provider corrente.<br/> |



 

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Family Safety
            WPC
               LogoImage = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40001
               DisplayName = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40002
               Description = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40003
               StateCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               ConfigCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               GRSVisible = 0x00000001 (1)
```

L'Pannello di controllo controllo genitori usa **LogoImage,** **DisplayName** e **Description** per modificare la pagina principale del controllo genitori Pannello di controllo quando viene selezionato il provider. Il **valore StateCLSID** viene usato quando il provider è abilitato o disabilitato. Il **valore ConfigCLSID** viene usato quando l'interfaccia utente ottiene informazioni dinamiche su ogni utente (questo è il caso solo se il provider è attualmente selezionato).

 

 




