---
description: Windows Explorer controlla la creazione di un connettore di ricerca per un gestore di protocollo tramite le voci della chiave del Registro di sistema. Tramite il Registro di sistema sia gli implementatori che le terze parti possono consentire ai gestori di protocollo nuovi e legacy di partecipare alla ricerca Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Creazione di un connettore di ricerca per un gestore di protocollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec9c7830f61c0dcbf6682e6dfaea0feb30ebfa5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881691"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a>Creazione di un connettore di ricerca per un gestore di protocollo

Windows Explorer controlla la creazione di un connettore di ricerca per un gestore di protocollo tramite le voci della chiave del Registro di sistema. Tramite il Registro di sistema sia gli implementatori che le terze parti possono consentire ai gestori di protocollo nuovi e legacy di partecipare alla ricerca Windows 7.

Questo argomento è organizzato come segue:

-   [Informazioni sui connettori di ricerca per i gestori di protocollo in Windows 7](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [Abilitazione dei gestori di protocollo per la partecipazione alla ricerca](#enabling-protocol-handlers-to-participate-in-search)
    -   [Disabilitazione della creazione del connettore di ricerca del gestore di protocollo](#disabling-protocol-handler-search-connector-creation)
    -   [Personalizzazione del nome, della descrizione o del tipo di cartella per un connettore di ricerca del gestore di protocollo](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [Uso del reindirizzamento delle stringhe del Registro di sistema](#using-registry-string-redirection)
    -   [Ripristino di un connettore di ricerca del gestore di protocollo eliminato](#restoring-a-deleted-protocol-handler-search-connector)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a>Informazioni sui connettori di ricerca per i gestori di protocollo in Windows 7

In Windows 7, le ricerche nel menu **Start** o Windows Explorer includono solo i file nei percorsi indicizzati e gli elementi non file system, ad esempio gli archivi dati remoti o gli elementi del gestore del protocollo che dispongono di un connettore di ricerca. Oltre a includere le voci del gestore di protocollo nell'ambito del menu **Start** e delle ricerche shell, il connettore di ricerca consente al menu **Start** di raggruppare le voci del gestore di protocollo nei risultati del menu **Start,** con il vantaggio risultante che l'utente può fare clic sull'intestazione del gruppo e visualizzare i risultati solo dal gestore del protocollo. In alternativa, l'utente  può passare alla cartella Ricerche, aprire il file del connettore di ricerca ed eseguire una ricerca che include solo gli elementi del gestore del protocollo specifico associato al connettore di ricerca.

Quando un utente avvia per la prima volta un'applicazione che registra un gestore di protocollo, Windows Explorer genera un file del connettore di ricerca (.searchConnector-ms) per il gestore del protocollo nella cartella **Ricerche** dell'utente. Le applicazioni con gestori di protocollo possono scegliere di disabilitare questo comportamento o personalizzare il nome e la descrizione del connettore di ricerca del gestore di protocollo.

> [!Note]  
> Il percorso della cartella **Ricerche** dell'utente è %userprofile% \\ Ricerche o FOLDERID \_ SavedSearches. Il GUID per FOLDERID \_ SavedSearches è {7d1d3a04-debb-4115-95cf-2f29da2920da}.

 

Windows Explorer controlla la creazione di un connettore di ricerca per un gestore di protocollo tramite le voci della chiave del Registro di sistema descritte nelle sezioni seguenti:

-   [Abilitazione dei gestori di protocollo per la partecipazione alla ricerca](#enabling-protocol-handlers-to-participate-in-search)
-   [Disabilitazione della creazione del connettore di ricerca del gestore di protocollo](#disabling-protocol-handler-search-connector-creation)
-   [Personalizzazione del nome, della descrizione o del tipo di cartella per un connettore di ricerca del gestore di protocollo](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [Ripristino di un connettore di ricerca del gestore di protocollo eliminato](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> Non esistono mezzi a livello di codice per creare un connettore di ricerca per un gestore di protocollo. Devono essere configurati tramite il Registro di sistema.

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a>Abilitazione dei gestori di protocollo per la partecipazione alla ricerca

Le chiavi del Registro di sistema e i relativi valori possibili sono descritti nella tabella seguente. Un gestore di protocollo può popolare alcune o tutte queste chiavi del Registro di sistema in cui il protocollo viene sostituito con il nome effettivo del protocollo, ad esempio &lt; &gt; MAPI, file o csc, ad esempio.



| Chiave del Registro di sistema                                                                                                                 | Valori possibili                                                                                                                     | Tipo       | Commenti                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY \_ LOCAL MACHINE Software Microsoft Windows ricerca \_ \\ \\ \\ \\ PHSearchConnectors \\ &lt; protocol &gt; \\ Version                     | Non esiste (impostazione predefinita). In caso contrario, è 1 o maggiore di 1.                                                                               | REG \_ DWORD | Questo valore viene usato per rilevare le modifiche alle registrazioni del modello di posizione per le radici di ricerca già elaborate. Se non esiste, usare 0 come valore predefinito. In alternativa, incrementare la versione per informare Windows Explorer che il connettore di ricerca deve essere rigenerato perché è stata installata una versione più recente del gestore del protocollo. |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ PhSearchConnectors \\ &lt; protocol &gt; \\ DoNotCreateSearchConnectors | Non esiste (impostazione predefinita). In caso contrario, impostare su 1.                                                                                         | REG \_ DWORD | Se non esiste, creare un file con estensione searchconnector-ms nella cartella Ricerche. Se 1, contrassegnare come elaborato e non eseguire alcuna operazione.                                                                                                                                                                                                                                   |
| HKEY LOCAL MACHINE Software Microsoft Windows Search PHSearchConnectors protocol Default Description (Descrizione predefinita del protocollo \_ \_ \\ \\ \\ \\ PHSearchConnectors) \\ &lt; &gt; \\ \\        | Stringa localizzabile contenente la descrizione del connettore di ricerca.                                                              | REG \_ SZ    | facoltativo. Viene usato nell'elemento Description del file .searchconnector-ms.                                                                                                                                                                                                                                                                          |
| HKEY LOCAL MACHINE Software Microsoft Windows Search PHSearchConnectors protocol Default Name (Nome predefinito del protocollo \_ \_ \\ \\ \\ \\ PHSearchConnectors) \\ &lt; &gt; \\ \\               | Stringa localizzata per assegnare un nome al connettore di ricerca. Usato come nome del file con estensione searchconnector-ms.                                    | REG \_ SZ    | Ogni località deve avere un nome univoco. In assenza di questo valore, verrà usato il nome visualizzato fornito dall'interfaccia [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) del gestore del protocollo.                                                                                                                             |
| HKEY \_ LOCAL MACHINE Software Microsoft Windows Search \_ \\ \\ \\ \\ PHSearchConnectors \\ &lt; protocol Default &gt; \\ \\ FolderType         | GUID che identifica [folderTYPEID](../shell/foldertypeid.md) da applicare al connettore di ricerca. | REG \_ SZ    | facoltativo. Usato nell'elemento folderType del file .searchconnector-ms per indicare i modelli da usare per visualizzare i risultati. Ad esempio, il valore GUID di FOLDERTYPEID \_ Documents.                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a>Disabilitazione della creazione del connettore di ricerca del gestore di protocollo

Se l'applicazione espone elementi tramite un gestore di protocollo per l'uso nell'applicazione stessa e non si vogliono esporre gli elementi tramite shell (nel menu **Start** e nelle ricerche di esplora Windows), è necessario disabilitare la creazione di un connettore di ricerca per il gestore del protocollo.

Per disabilitare la creazione del connettore di ricerca, impostare DoNotCreateSearchConnectors su 0x00000001(1), come illustrato nell'esempio di chiave del Registro di sistema seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

Se DoNotCreateSearchConnectors è impostato su 1, è consigliabile esporre la proprietà [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) in ogni elemento esposto dal gestore del protocollo e impostare il valore di questa proprietà su **TRUE.** In questo modo, gli elementi del gestore del protocollo non verranno visualizzati nel gruppo File **del** menu **Start.**

Se DoNotCreateSearchConnectors è presente e impostato su zero, Windows Explorer creerà un connettore di ricerca per il gestore del protocollo e gli elementi del gestore del protocollo verranno restituiti in nel menu **Start** e nelle ricerche Windows Explorer.

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a>Personalizzazione del nome, della descrizione o del tipo di cartella per un connettore di ricerca del gestore di protocollo

Il nome del connettore di ricerca viene usato non solo per identificare il connettore di ricerca nella cartella **Ricerche,** ma anche come intestazione di gruppo per i risultati nelle ricerche nel menu **Start.** È quindi importante specificare un nome descrittivo per il connettore di ricerca. Se non viene specificato un nome nella chiave del Registro di sistema, per impostazione predefinita Windows Explorer usa il nome fornito dall'interfaccia [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) per la radice di ricerca del gestore del protocollo e una descrizione vuota. È possibile eseguire l'override del nome predefinito tramite una voce della chiave del Registro di sistema senza dover rinominare l'interfaccia IShellFolder. Anche se non è visibile come nome del connettore di ricerca, è anche possibile eseguire l'override della descrizione per il connettore di ricerca specificando la propria descrizione.

Per eseguire l'override del nome o della descrizione predefinita, impostare le voci come illustrato nell'esempio del Registro di sistema seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

Inoltre, la voce FolderType può essere impostata su uno dei [GUID FOLDERTYPEID.](../shell/foldertypeid.md) Il valore deve essere il GUID effettivo e non il relativo nome. Ad esempio, {94d6ddcc-4a68-4175-a374-bd584a510b78} anziché FOLDERTYPEID \_ Musica. Il GUID per folderTYPEID può essere ottenuto nel file di intestazione Shlguid.h in [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a>Uso del reindirizzamento delle stringhe del Registro di sistema

È possibile usare una [stringa reindirizzata](../intl/using-registry-string-redirection.md) per assicurarsi che il nome specificato per il connettore di ricerca possa essere localizzato. È possibile includere stringhe localizzabili per le chiavi del Registro di sistema name e description anziché immettere la stringa effettiva nel Registro di sistema.

Per includere una stringa localizzabile per i valori Name o Description, impostare il valore come illustrato nell'esempio di chiave del Registro di sistema seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

La stringa localizzabile ha il formato seguente:

-   @dllname.dll,-resourceID, dove:
    -   @dllname.dll è il percorso della DLL che contiene la risorsa stringa
    -   resourceID è l'ID risorsa integer della risorsa stringa

Il formato per una stringa indiretta e una stringa indiretta aggiunta con un modificatore di versione è descritto in [Funzione SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a>Ripristino di un connettore di ricerca del gestore di protocollo eliminato

Poiché i connettori di ricerca sono file nel computer dell'utente, possono essere erroneamente eliminati. Per ripristinare tutti i connettori di ricerca del gestore di protocollo eliminati, ripristinare le librerie predefinite. A tale scopo, aprire Windows Explorer, fare clic con il pulsante destro del mouse sulla **cartella Librerie** e quindi scegliere **Ripristina librerie predefinite**.

![Screenshot che mostra l'opzione di menu Ripristina librerie predefinite](images/libraries.png)

## <a name="additional-resources"></a>Risorse aggiuntive

-   [IShellItem::GetDisplayName](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [SIGDN \_ NORMALDISPLAY](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui gestori di protocollo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notifica all'indice delle modifiche](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Aggiunta di icone e menu di scelta rapida](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Esempio di codice: Estensioni della shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Debug di gestori di protocollo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
