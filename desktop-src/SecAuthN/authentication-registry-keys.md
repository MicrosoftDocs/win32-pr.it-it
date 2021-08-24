---
description: Quando installa un provider di rete, l'applicazione deve creare le chiavi del Registro di sistema e i valori descritti in questo argomento.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Chiavi del Registro di sistema per l'autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c245cdb27a0d661e7e6df82ed0d1d0ed35a59ea05bf74bf98ebd39ba3dc791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883681"
---
# <a name="authentication-registry-keys"></a>Chiavi del Registro di sistema per l'autenticazione

Quando installa un provider di rete, l'applicazione deve creare le chiavi del Registro di sistema e i valori descritti in questo argomento. Queste chiavi e valori forniscono informazioni alla MPR sui provider di rete installati nel sistema. La MPR controlla queste chiavi all'avvio e carica le DLL del provider di rete trovate.

Prima di creare un set di chiavi per contenere le informazioni sul provider di rete, è necessario aggiungere il nome del provider di rete alla **chiave dell'ordine.** Questa chiave è una sottochiave della chiave seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

La **chiave order** contiene un singolo valore, **ProviderOrder**, che elenca i provider installati e specifica l'ordine in cui devono essere provati durante le operazioni che passano attraverso i provider fino a quando non viene trovato un provider di accettazione.

Il **valore ProviderOrder** contiene un elenco delimitato da virgole di nomi di chiave. Ogni nome di chiave in **ProviderOrder** identifica un provider di rete. Quando MPR scorre i provider, li chiama nell'ordine in cui vengono visualizzati nell'elenco.

Il nome del provider impostato in **ProviderOrder** deve essere usato anche come nome della chiave del Registro di sistema che contiene informazioni su tale provider. Le chiavi del Registro di sistema specifiche del provider vengono create come sottochiavi della chiave seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

In altre parole, i nomi dei provider specificati in **ProviderOrder** sono il percorso del Registro di sistema delle chiavi specifiche del provider di rete, rispetto al percorso seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Quando viene installato il servizio del provider di rete, l'applicazione di installazione deve aggiungere una chiave come indicato di seguito:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Dove *ProviderName* è il nome del provider di rete come specificato nel **valore ProviderOrder** della **chiave dell'ordine.** Il **valore** Group sotto la *chiave ProviderName* deve essere impostato su "NetworkProvider". In questo modo il servizio viene identificato come in un gruppo di provider di rete.

È anche necessario creare una sottochiave *di ProviderName*, **networkprovider**. Questa chiave contiene i valori seguenti che descrivono il provider di rete.



| Valore                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome**<br/>         | Contiene il nome del provider. Questo nome viene visualizzato all'utente come nome della rete nelle finestre di dialogo di esplorazione e deve corrispondere al campo **lpProvider** restituito nelle [**strutture NETRESOURCE.**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) Questo nome deve essere una variante del nome del prodotto, preferibilmente con un'indicazione dell'azienda, in modo che sia chiaro e univoco. "MS-LanMan", ad esempio, è un nome valido, mentre "The Net" sarebbe una scelta non ottimale.<br/> |
| **ProviderPath**<br/> | Contiene il percorso completo della DLL che implementa il provider di rete. La funzione MPR [**chiama LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) in questo percorso.<br/>                                                                                                                                                                                                                                                                                                                                |



 

I valori seguenti vengono usati solo dai provider di rete che supportano le funzioni di gestione delle credenziali, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) [**e NPPasswordChangeNotify.**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)



| Valore                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Classe**<br/>               | Valore **DWORD** che identifica la classe, o tipo, delle funzionalità del provider supportate da questo provider. I valori possono essere uniti dall'operatore **OR** quando appropriato. I valori validi per questa classe sono WN \_ NETWORK \_ CLASS, WN \_ CREDENTIAL \_ CLASS, WN \_ PRIMARY \_ AUTHENT \_ CLASS e WN SERVICE \_ \_ CLASS.<br/> Anche se un provider può supportare la funzionalità dell'autenticatore primario, verrà usato un altro mezzo per determinare quale autenticatore è primario.<br/> **Windows XP/2000:** Il cambio di autenticatori primari non è supportato, quindi questo valore viene ignorato. <br/> |
| **AuthentProviderPath**<br/> | Si tratta del nome file completo per la DLL che esporta le funzioni di gestione delle credenziali. Questo valore è utile (ma non obbligatorio) solo quando il provider viene identificato come provider CREDENTIAL CLASS o \_ PRIMARY \_ AUTHENT \_ CLASS. Se questo valore non è presente per un provider di questa classe, è previsto che le funzioni di gestione delle credenziali siano esportate dalla DLL identificata dal valore ProviderPath. Questo valore viene usato solo se è consigliabile creare un pacchetto delle funzioni di rete e delle funzioni di gestione delle credenziali in DLL separate.<br/>  |



 

Oltre ai valori utilizzati per registrare i provider di rete e i gestori delle credenziali, è possibile aggiungere un valore al Registro di sistema per registrare una DLL per ricevere le notifiche di connessione. A tale scopo, creare un valore \_ REG EXPAND \_ SZ sotto la chiave seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Questo valore deve specificare il percorso di una DLL che implementa l'interfaccia [di Notification API](connection-notification-api.md). Il nome di questo valore può essere qualsiasi valore, purché non sia in conflitto con nomi di valore preesistenti.

## <a name="example"></a>Esempio

L'esempio seguente mostra le chiavi del Registro di sistema per un sistema in cui sono installati due provider di rete: LanmanWorkStation e AnotherNetSvc. AnotherNetSvc è anche un gestore di credenziali. Nell'esempio i nomi delle chiavi sono in grassetto e i nomi dei valori sono in corsivo.

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet Controllare** \\ **l'ordine** \\ **NetworkProvider** \\ 

*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"

**HKEY \_ Local \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **Notifyees**

*MyNotifyApp* = "c: \\ connect \\connect.dll"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**\\

*Group* = "NetworkProvider"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Class* = 0x00000001 (WN \_ NETWORK \_ CLASS)

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**\\

*Group* = "NetworkProvider"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "Another Network"*ProviderPath* = "c: \\ another \\anet.dll"

*Classe* = 0x00000003 (CLASSE WN \_ NETWORK \_ \| WN \_ \_ CREDENTIAL)

*AuthentProviderPath* = "c: \\ another \\anetCM.dll"

 

