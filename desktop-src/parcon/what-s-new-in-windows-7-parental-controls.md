---
description: Fornisce una panoramica delle modifiche apportate ai controlli padre di Windows introdotti in Windows 7.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Novità dei controlli padre di Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8282021c81ee8611fb7206d75f7e6aab48ebf2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314536"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Novità dei controlli padre di Windows 7

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Panoramica delle modifiche ai controlli padre per Windows 7

Lo scopo di questo documento è fornire una panoramica delle modifiche apportate ai controlli padre di Windows introdotti in Windows 7 e per consentire ai provider di soluzioni di controllo parentale di terze parti di sfruttare queste modifiche. In questo documento si presuppone la familiarità dei lettori con i controlli padre per Windows Vista e verranno riportate solo le modifiche apportate a questa funzionalità di Windows 7 che sono rilevanti per lo sviluppo di soluzioni di controllo parentale di terze parti. Un aggiornamento completo della documentazione del controllo padre di Windows per MSDN seguirà in un secondo momento.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Decisioni di progettazione principali per le modifiche ai controlli padre di Windows 7

Le modifiche apportate ai controlli padre introdotti in Windows 7 continuano l'obiettivo generale di promuovere la coesistenza di soluzioni di controllo padre di terze parti con la funzionalità predefinita. È necessario apportare le modifiche seguenti:

-   Rimozione del filtro Web e della creazione di report delle attività dalla funzionalità dei controlli padre in-box. I controlli padre in-box forniscono le restrizioni implementate da Microsoft offline, ad esempio i limiti di tempo, le restrizioni delle applicazioni e le restrizioni relative ai giochi. Il filtro Web, la creazione di report delle attività e altre funzionalità possono essere forniti da soluzioni di controllo parentale di Microsoft o di terze parti. Ad esempio, la soluzione di sicurezza famiglia di Windows Live fornisce filtri Web, gestione remota e monitoraggio delle attività, nonché la gestione dei contatti per tutte le applicazioni Windows Live.
-   Consentire a soluzioni di terze parti di sostituire l'interfaccia utente di configurazione del provider nel riquadro continuando a basarsi sull'implementazione in-box di tempo, applicazione e restrizioni di gioco.
-   Abilitazione della scoperta e dell'abilitazione di soluzioni di terze parti nel computer da parte di un genitore o tutore (account amministratore).

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Controllo parentale modifiche all'interfaccia utente di livello superiore in Windows 7

Windows 7 apporta le seguenti modifiche all'interfaccia utente di livello superiore del pannello di controllo dei controlli padre:

-   La sezione controlli aggiuntivi è stata introdotta in cui è possibile selezionare i controlli che forniscono funzionalità aggiuntive, ad esempio il filtro Web, la creazione di report delle attività e così via, da una casella di riepilogo a discesa. I provider Microsoft o di terze parti devono registrare le proprie soluzioni con i controlli padre di Windows 7 affinché siano selezionabili dall'elenco a discesa controlli aggiuntivi. Per informazioni sulla registrazione di una soluzione, vedere registrazione del provider, più avanti in questo argomento.
-   L'immagine del logo del provider attualmente selezionato viene visualizzata nell'angolo superiore destro della pagina.
-   I riquadri utente gestiti possono visualizzare un riepilogo delle impostazioni padre fornite dal provider attualmente selezionato.

Il provider attualmente selezionato può scegliere di usare la propria interfaccia utente per le schermate di controllo utente per gli utenti gestiti o potrebbe selezionare di basarsi sull'implementazione di WPC in-box di questa schermata. Per l'implementazione in-box sono state apportate le modifiche seguenti ai relativi elementi:

-   La sezione report attività è stata rimossa.
-   Il collegamento per visualizzare i report delle attività è stato rimosso.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Cenni preliminari sull'API dei controlli padre: modifiche di Windows 7

Il meccanismo di integrazione per i provider di soluzioni di terze parti è stato ampliato in modo da consentire:

-   Registrazione del provider. Al momento della registrazione, un provider diventa selezionabile nella casella di riepilogo a discesa controlli aggiuntivi della schermata del pannello di controllo dei controlli padre.
-   Esecuzione di query per il provider attualmente selezionato. Per abilitare questa funzionalità, viene esposta un'interfaccia COM pubblica.
-   Inoltre, è il set di interfacce COM che devono essere implementate dai provider per consentire:
    -   Abilitazione o disabilitazione del provider da WPC alla selezione da parte dell'utente di controlli aggiuntivi.
    -   WPC per passare il controllo al provider per configurare le impostazioni di controllo padre dell'utente gestito.
    -   WPC per eseguire una query sul provider per il riepilogo delle impostazioni di controllo padre dell'utente gestito.

## <a name="third-party-provider-integration"></a>Integrazione di provider di terze parti

### <a name="provider-registration"></a>Registrazione del provider

Per registrare un nuovo provider con controlli padre, è necessario scrivere un valore del registro di sistema nella chiave Providers dei controlli padre di Windows. Il nome del valore è un GUID univoco usato per identificare il provider. I dati del valore saranno un percorso di una chiave del registro di sistema nel **\_ \_ computer locale HKEY** che contiene informazioni sul provider.

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

Nel percorso della chiave del registro di sistema specificato, sono previsti i valori seguenti.



| Termine                                                                                                                 | Descrizione                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**<br/>         | Percorso completo di un file binario di risorsa con un ID di risorsa negativo per l'immagine del logo del provider (archiviato come **\_ bitmap immagine**).<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**<br/> | Percorso completo di un file binario di risorsa con ID di risorsa negativo per il nome del provider. La lunghezza di **DisplayName** non deve superare i 50 caratteri.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**<br/> | Percorso completo di un file binario di risorsa con un ID di risorsa negativo per la descrizione del provider. La lunghezza della descrizione non deve superare i 200 caratteri.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | ID classe della classe del provider che implementa IWPCProviderState.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | ID classe della classe del provider che implementa IWPCProviderConfig. **StateCLSID** e **ConfigCLSID** possono essere uguali.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | Valore **DWORD** facoltativo diverso da zero che specifica che i controlli padre di Windows visualizzano un collegamento alla schermata del sistema di classificazione dei giochi dopo che un provider è stato selezionato come nuovo provider corrente.<br/> |



 

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

Il pannello di controllo Parental Controls USA **LogoImage**, **DisplayName** e **Description** per modificare la pagina principale del pannello di controllo Parental Controls quando tale provider è selezionato. Il valore **StateCLSID** viene usato quando il provider è abilitato o disabilitato. Il valore **ConfigCLSID** viene usato quando l'interfaccia utente ottiene informazioni dinamiche su ogni utente, ovvero solo se il provider è attualmente selezionato.

 

 




