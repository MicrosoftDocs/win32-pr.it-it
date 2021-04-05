---
description: Quando viene installato un provider di rete, l'applicazione deve creare le chiavi del registro di sistema e i valori descritti in questo argomento.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Chiavi del registro di sistema di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967720"
---
# <a name="authentication-registry-keys"></a>Chiavi del registro di sistema di autenticazione

Quando viene installato un provider di rete, l'applicazione deve creare le chiavi del registro di sistema e i valori descritti in questo argomento. Queste chiavi e i valori forniscono informazioni a MPR sui provider di rete installati nel sistema. L'MPR controlla queste chiavi all'avvio e carica le dll del provider di rete trovate.

Prima di creare un set di chiavi che contenga le informazioni sul provider di rete, è necessario aggiungere il nome del provider di rete alla chiave dell' **ordine** . Questa chiave è una sottochiave della chiave seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

La chiave **Order** contiene un solo valore, **ProviderOrder**, che elenca i provider installati e specifica l'ordine in cui devono essere tentati durante le operazioni che consentono di scorrere i provider fino a quando non viene trovato un provider di accettazione.

Il valore **ProviderOrder** contiene un elenco delimitato da virgole di nomi di chiave. Ogni nome di chiave in **ProviderOrder** identifica un provider di rete. Quando MPR scorre i provider, li chiama nell'ordine in cui sono visualizzati nell'elenco.

Il nome del provider impostato in **ProviderOrder** deve essere usato anche come nome della chiave del registro di sistema che contiene informazioni su tale provider. Le chiavi del registro di sistema specifiche del provider vengono create come sottochiavi della chiave seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

In altre parole, i nomi di provider specificati in **ProviderOrder** sono il percorso del registro di sistema delle chiavi specifiche del provider di rete, relativo al percorso seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Quando il servizio provider di rete è installato, l'applicazione di installazione deve aggiungere una chiave come indicato di seguito:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Dove *providerName* è il nome del provider di rete, come specificato nel valore **ProviderOrder** della chiave **Order** . Il valore del **gruppo** sotto la chiave *providerName* deve essere impostato su "NetworkProvider". Identifica il servizio come nel gruppo provider di rete.

È inoltre necessario creare una sottochiave di *providerName*, **NetworkProvider**. Questa chiave contiene i valori seguenti che descrivono il provider di rete.



| Valore                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome**<br/>         | Contiene il nome del provider. Questo nome viene visualizzato all'utente come nome della rete nelle finestre di dialogo di esplorazione e deve corrispondere al campo **lpProvider** restituito nelle strutture [**netresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) . Questo nome deve essere una variante del nome del prodotto, preferibilmente con alcune indicazioni della società, in modo che sia chiaro e univoco. "MS-LanMan", ad esempio, è un nome valido, mentre "NET" sarebbe una scelta scadente.<br/> |
| **ProviderPath**<br/> | Contiene il percorso completo della DLL che implementa il provider di rete. MPR chiama [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) su questo percorso.<br/>                                                                                                                                                                                                                                                                                                                                |



 

I valori seguenti vengono usati solo dai provider di rete che supportano le funzioni di gestione delle credenziali, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).



| Valore                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Classe**<br/>               | **DWORD** che identifica la classe, o tipo, della funzionalità del provider supportata da questo provider. Quando appropriato, i valori possono essere Uniti dall'operatore **or** . I valori validi per questo documento sono la classe di rete, la classe della \_ \_ \_ credenziale, la classe AUTHENT e la classe di \_ \_ \_ \_ \_ servizio \_ .<br/> Sebbene un provider possa supportare la funzionalità di autenticazione primaria, verrà usato un altro metodo per determinare quale autenticatore è primario.<br/> **Windows XP/2000:** Il cambio di autenticatori primari non è supportato, pertanto questo valore viene ignorato. <br/> |
| **AuthentProviderPath**<br/> | Si tratta del nome file completo per la DLL che esporta le funzioni di gestione delle credenziali. Questo valore è utile, ma non obbligatorio, solo quando il provider viene identificato come una classe CREDENTIAL \_ o un \_ provider di \_ classi AUTHENT primario. Se questo valore non è presente per un provider di questa classe, le funzioni di gestione delle credenziali dovrebbero essere esportate dalla DLL identificata dal valore ProviderPath. Questo valore viene utilizzato solo se si desidera creare il pacchetto delle funzioni di rete e delle funzioni di gestione delle credenziali in DLL separate.<br/>  |



 

Oltre ai valori utilizzati per registrare i provider di rete e i gestori delle credenziali, è possibile aggiungere un valore al registro di sistema per registrare una DLL per ricevere le notifiche di connessione. A tale scopo, creare un \_ valore reg Expand \_ SZ nella chiave seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Questo valore deve specificare il percorso di una DLL che implementa l' [API di notifica della connessione](connection-notification-api.md). Il nome di questo valore può essere qualsiasi elemento desiderato, purché non sia in conflitto con i nomi dei valori preesistenti.

## <a name="example"></a>Esempio

Nell'esempio seguente vengono illustrate le chiavi del registro di sistema per un sistema in cui sono installati due provider di rete: LanmanWorkStation e AnotherNetSvc. AnotherNetSvc è anche una gestione credenziali. Nell'esempio i nomi delle chiavi sono in grassetto e i nomi di valore sono in corsivo.

**HKEY \_ \_** \\  \\  \\  \\  \\ **Ordine** NetworkProvider del controllo CurrentControlSet del computer locale

*ProviderOrder* = "LanmanWorkStation, AnotherNetSvc"

**HKEY \_ \_** \\  \\  \\  \\  \\ **Avvisi** NetworkProvider del controllo CurrentControlSet del computer locale

*MyNotifyApp* = "c: \\ Connect \\connect.dll"

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**\\

*Group* = "NetworkProvider"

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Classe* = 0x00000001 ( \_ classe di rete \_ )

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**\\

*Group* = "NetworkProvider"

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "un'altra rete"*ProviderPath* = "c: \\ un'altra \\anet.dll"

*Classe* = 0x00000003 (classe di rete di una classe di \_ \_ \| \_ credenziali \_ )

*AuthentProviderPath* = "c: \\ un'altra \\anetCM.dll"

 

