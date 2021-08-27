---
title: Registrazione dell'oggetto COM del menu di scelta rapida in un identificatore di visualizzazione
description: In questo argomento vengono illustrate le chiavi del Registro di sistema che devono essere modificate per registrare un oggetto COM del menu di scelta rapida.
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- Registrazione dell'oggetto COM del menu di scelta rapida in un identificatore di visualizzazione
- oggetto COM del menu di scelta rapida AD, registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5650d5864093293728e5c4f1157980c76bffa0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881251"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>Registrazione dell'oggetto COM del menu di scelta rapida in un identificatore di visualizzazione

Quando si utilizza COM per creare una DLL di estensione del menu di scelta rapida per un servizio directory Active Directory, l'estensione deve essere registrata con il Registro di sistema di Windows e Active Directory Domain Services per notificare agli snap-in MMC amministrativi di Active Directory e alla shell Windows dell'estensione.

## <a name="registering-in-the-windows-registry"></a>Registrazione nel Registro Windows registro

Come tutti i server COM, un'estensione del menu di scelta rapida deve essere registrata nel Registro di sistema. L'estensione viene registrata con la chiave seguente.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; clsid &gt; è* la rappresentazione di stringa del CLSID prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) Sotto la *&lt; chiave &gt; clsid* è presente una chiave **InProcServer32** che identifica l'oggetto come server in-process a 32 bit. Nella chiave **InProcServer32** il percorso della DLL viene specificato nel valore predefinito e il modello di threading viene specificato nel **valore ThreadingModel.** Tutte le estensioni del menu di scelta rapida devono usare il modello di threading "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registrazione con Active Directory Domain Services

La registrazione dell'estensione del menu di scelta rapida è specifica per le impostazioni locali. Se l'estensione del menu di scelta rapida si applica a tutte le impostazioni locali, deve essere registrata nella classe di oggetti [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) object in tutti i sottocontenitori delle impostazioni locali nel contenitore Display Specifiers. Se l'estensione del menu di scelta rapida è localizzata per determinate impostazioni locali, deve essere registrata nell'oggetto **displaySpecifier** nel sottocontenitore di tale impostazioni locali. Per altre informazioni sul contenitore Display Specifiers e sulle impostazioni locali, vedere [Display Specifiers](display-specifiers.md) e [DisplaySpecifiers Container.](displayspecifiers-container.md)

Esistono due attributi dell'identificatore di visualizzazione in cui è possibile registrare una voce di estensione del menu di scelta rapida. Si tratta [**di adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu.**](/windows/desktop/ADSchema/a-shellcontextmenu)

[**L'attributo adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica i menu di scelta rapida amministrativi da visualizzare negli snap-in amministrativi di Active Directory. Il menu di scelta rapida viene visualizzato quando l'utente visualizza il menu di scelta rapida per gli oggetti della classe appropriata in uno degli snap-in MMC amministrativi di Active Directory.

[**L'attributo shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica i menu di scelta rapida dell'utente finale da visualizzare nella Windows shell. Il menu di scelta rapida viene visualizzato quando l'utente visualizza il menu di scelta rapida per gli oggetti della classe appropriata in Windows explorer. A partire Windows Server 2003, la shell Windows non visualizza più oggetti di Active Directory Domain Services.

Tutti questi attributi sono multivalore.

Quando si registra un'estensione del menu di scelta rapida, i valori per gli attributi [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) richiedono il formato seguente.


```C++
<order number>,<clsid>
```



" &lt; order number &gt; " è un numero senza segno che rappresenta la posizione dell'elemento nel menu di scelta rapida. Quando viene visualizzato un menu di scelta rapida, i valori vengono ordinati usando un confronto del " numero di ordine" &lt; di ogni &gt; valore. Se più valori hanno lo stesso " numero di ordine ", le estensioni del menu di scelta rapida vengono caricate nell'ordine in cui vengono &lt; &gt; lette dal server Active Directory. Se possibile, usare un " numero d'ordine" non esistente, che non è stato usato da &lt; altri valori nella proprietà &gt; . Non esiste una posizione iniziale prestabilita e sono consentiti spazi nella sequenza &lt; "numero &gt; ordine".

" &lt; clsid " è la rappresentazione di stringa &gt; del CLSID prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)

Nella shell Windows sono supportate le voci del menu di scelta rapida a selezione multipla. In questo caso, l'estensione del menu di scelta rapida viene richiamata per ogni oggetto selezionato. Negli snap-in amministrativi di Active Directory sono supportate anche le voci di estensione del menu di scelta rapida a selezione multipla. In questo caso, la [**struttura DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) conterrà una [**struttura DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) per ogni oggetto directory selezionato.

> [!IMPORTANT]
> Per la shell Windows, le informazioni sull'identificatore di visualizzazione vengono recuperate all'accesso dell'utente e memorizzate nella cache per la sessione dell'utente. Per gli snap-in amministrativi, i dati dell'identificatore di visualizzazione vengono recuperati quando lo snap-in viene caricato e memorizzato nella cache per la durata del processo. Per la shell Windows, ciò significa che le modifiche apportate agli identificatori di visualizzazione vengono applicate dopo che un utente si disconnette e si disconnette di nuovo. Per gli snap-in amministrativi, le modifiche vengono applicate quando viene ricaricato lo snap-in o il file della console, ad esempio se si avvia una nuova istanza del file della console o una nuova istanza di Mmc.exe e si aggiunge lo snap-in, vengono recuperati i dati dell'identificatore di visualizzazione più recenti.

 

Per altre informazioni e un esempio di codice su come implementare un'estensione del menu di scelta rapida, vedere Codice di esempio per l'implementazione [dell'oggetto COM del menu di scelta rapida.](example-code-for-implementation-of-the-context-menu-com-object.md)

 

 
