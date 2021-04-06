---
title: Registrazione dell'oggetto COM del menu di scelta rapida in un identificatore di visualizzazione
description: In questo argomento vengono illustrate le chiavi del registro di sistema che devono essere modificate per registrare un oggetto COM del menu di scelta rapida.
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- Registrazione dell'oggetto COM del menu di scelta rapida in un identificatore di visualizzazione
- ANNUNCIO dell'oggetto COM del menu di scelta rapida, registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae30c1a60a1a0bc5a8ec388a3578ab13829c95
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046491"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>Registrazione dell'oggetto COM del menu di scelta rapida in un identificatore di visualizzazione

Quando si utilizza COM per creare una DLL di estensione del menu di scelta rapida per un servizio di Active Directory directory, l'estensione deve essere registrata con il registro di sistema di Windows e Active Directory Domain Services per inviare una notifica ai Active Directory snap-in MMC amministrativi e la shell di Windows dell'estensione.

## <a name="registering-in-the-windows-registry"></a>Registrazione nel registro di sistema di Windows

Come tutti i server COM, un'estensione del menu di scelta rapida deve essere registrata nel registro di sistema. L'estensione viene registrata con la chiave seguente.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*<clsid>* rappresentazione di stringa del CLSID come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . Sotto la *<clsid>* chiave è presente una chiave **InprocServer32** che identifica l'oggetto come server in-process a 32 bit. Nella chiave **InprocServer32** il percorso della dll viene specificato nel valore predefinito e il modello di Threading viene specificato nel valore **ThreadingModel** . Per tutte le estensioni del menu di scelta rapida è necessario utilizzare il modello di threading "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registrazione con Active Directory Domain Services

La registrazione dell'estensione del menu di scelta rapida è specifica di un'impostazione locale. Se l'estensione del menu di scelta rapida si applica a tutte le impostazioni locali, deve essere registrata nell'oggetto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) della classe di oggetti in tutti i sottocontenitori delle impostazioni locali nel contenitore degli identificatori di visualizzazione. Se l'estensione del menu di scelta rapida è localizzata per determinate impostazioni locali, è necessario registrarla nell'oggetto **displaySpecifier** del sottocontenitore delle impostazioni locali. Per ulteriori informazioni sul contenitore e le impostazioni locali per gli identificatori di visualizzazione, vedere la pagina relativa agli [identificatori di visualizzazione](display-specifiers.md) e al [contenitore DisplaySpecifiers](displayspecifiers-container.md).

Sono disponibili due attributi dell'identificatore di visualizzazione in cui è possibile registrare un elemento di estensione del menu di scelta rapida. Si tratta di [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).

L'attributo [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica i menu di scelta rapida amministrativi da visualizzare in Active Directory snap-in amministrativi. Il menu di scelta rapida viene visualizzato quando l'utente Visualizza il menu di scelta rapida per gli oggetti della classe appropriata in uno dei Active Directory snap-in MMC amministrativi.

L'attributo [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica i menu di scelta rapida dell'utente finale da visualizzare nella shell di Windows. Il menu di scelta rapida viene visualizzato quando l'utente Visualizza il menu di scelta rapida per gli oggetti della classe appropriata in Esplora risorse. A partire da Windows Server 2003, la shell di Windows non Visualizza più gli oggetti di Active Directory Domain Services.

Tutti questi attributi sono multivalore.

Quando si registra un'estensione del menu di scelta rapida, i valori per gli attributi [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) richiedono il formato seguente.


```C++
<order number>,<clsid>
```



Il " &lt; numero di ordine &gt; " è un numero senza segno che rappresenta la posizione dell'elemento nel menu di scelta rapida. Quando viene visualizzato un menu di scelta rapida, i valori vengono ordinati usando un confronto tra il " &lt; numero di ordine" di ogni valore &gt; . Se più di un valore ha lo stesso " &lt; numero &gt; di ordine", le estensioni del menu di scelta rapida vengono caricate nell'ordine in cui vengono lette dal server Active Directory. Se possibile, usare un " &lt; numero di ordine" non esistente &gt; , ovvero uno che non è stato usato da altri valori nella proprietà. Non sono consentite posizioni iniziali e gap nella &lt; sequenza "Order Number &gt; ".

" &lt; CLSID &gt; " è la rappresentazione di stringa del CLSID come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

Nella shell di Windows sono supportate le voci del menu di scelta rapida a selezione multipla. In questo caso, l'estensione del menu di scelta rapida viene richiamata per ogni oggetto selezionato. In Active Directory snap-in amministrazione sono supportati anche gli elementi di estensione del menu di scelta rapida a selezione multipla. In questo caso, la struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) conterrà una struttura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) per ogni oggetto directory selezionato.

> [!IMPORTANT]
> Per la shell di Windows, le informazioni sugli identificatori di visualizzazione vengono recuperate all'accesso dell'utente e memorizzate nella cache per la sessione dell'utente. Per gli snap-in amministrativi, i dati dell'identificatore di visualizzazione vengono recuperati quando lo snap-in viene caricato e viene memorizzato nella cache per la durata del processo. Per la shell di Windows, ciò significa che le modifiche apportate agli identificatori di visualizzazione diventano effettive dopo che un utente si disconnette e si riaccende. Per gli snap-in amministrativi, le modifiche diventano effettive quando lo snap-in o il file della console viene ricaricato, ovvero se si avvia una nuova istanza del file di console o di una nuova istanza di Mmc.exe e si aggiunge lo snap-in, vengono recuperati i dati più recenti dell'identificatore di visualizzazione.

 

Per ulteriori informazioni e un esempio di codice relativo all'implementazione di un'estensione del menu di scelta rapida, vedere [codice di esempio per l'implementazione dell'oggetto com del menu di scelta rapida](example-code-for-implementation-of-the-context-menu-com-object.md).

 

 