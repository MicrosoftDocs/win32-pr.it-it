---
description: Il sistema di cartelle note fornisce un modo per interagire con alcune cartelle di alto profilo che sono presenti per impostazione predefinita in Windows.
ms.assetid: 8b6163b5-e152-47c2-99f1-43e80cf0713e
title: Utilizzo di cartelle note nelle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0981d354e49f569dda229fab32308d8f4a79ff99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484005"
---
# <a name="working-with-known-folders-in-applications"></a>Utilizzo di cartelle note nelle applicazioni

Il sistema di cartelle note fornisce un modo per interagire con alcune cartelle di alto profilo che sono presenti per impostazione predefinita in Windows. Consente inoltre di usare le stesse interazioni con le cartelle installate e registrate con il sistema di cartelle note dalle applicazioni. In questo argomento vengono illustrate le possibili interazioni fornite dalle API di cartelle note.

-   [Interfacce di cartelle note](#known-folder-interfaces)
-   [Reindirizzamento](#redirection)
-   [Argomenti correlati](#related-topics)

> [!IMPORTANT]
> Per reindirizzare i documenti, le immagini o le cartelle desktop a OneDrive, usare lo spostamento della cartella nota OneDrive anziché il metodo di reindirizzamento descritto in questo articolo. Per informazioni, vedere [reindirizzare e spostare cartelle note di Windows in OneDrive](/onedrive/redirect-known-folders).  

## <a name="known-folder-interfaces"></a>Interfacce di cartelle note

Sono disponibili due interfacce di cartelle note: [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) e [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager).

In [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager) sono disponibili molte delle funzioni più generali relative a tali cartelle. I metodi consentono di:

-   Recuperare un [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) basato su [**KNOWNFOLDERID**](knownfolderid.md)di tale cartella, il nome canonico, il percorso espresso come stringa o il percorso espresso come IDList.
-   Converte un CSIDL nell'equivalente [**KNOWNFOLDERID**](knownfolderid.md) o converte un **KNOWNFOLDERID** nell'equivalente CSIDL legacy.
-   Registrare o annullare la registrazione di una cartella nota con il sistema.
-   Recuperare tutti i valori di [**KNOWNFOLDERID**](knownfolderid.md) registrati nel sistema.
-   Reindirizza una cartella nota a una nuova posizione.

[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) fornisce un metodo che consente a una cartella di reindirizzarsi a se stessa fornendo un nuovo percorso. Gli altri metodi ottengono informazioni su una cartella nota specifica, tra cui:

-   Categoria della cartella: virtuale, fissa, comune o per utente.
-   Tipo di cartella, ad esempio compresso, documenti, immagini o file utente.
-   [**KNOWNFOLDERID**](knownfolderid.md) della cartella.
-   Percorso completo della cartella come IDList o sotto forma di stringa. Anche il percorso relativo di una cartella padre.
-   Nome canonico della cartella.
-   Descrizione comando visualizzata per la cartella.
-   Icona visualizzata per la cartella.
-   Descrizione della cartella che ne spiega lo scopo e l'utilizzo.
-   Indica se è in grado di reindirizzare la cartella.

[**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) fornisce inoltre un metodo per recuperare un [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) in base alla cartella. In questo modo è possibile associare la cartella a un gestore, confrontare due cartelle e recuperare gli attributi, il nome visualizzato e la cartella padre della cartella.

## <a name="redirection"></a>Reindirizzamento

Reindirizzamento cartelle è una funzionalità importante del sistema di cartelle note. Tutte le cartelle note della [ **categoria Common** KF \_ Category \_ Common * * * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) o la categoria [KF **per utente** \_ \_ * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) * * sono reindirizzabili. Non è possibile reindirizzare la cartella della categoria Virtual [ KF \_ Category \_ Virtual * * * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category) o fixed di categoria [ KF \_ \_ fixed * *](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category)* *.

È possibile reindirizzare le cartelle in un percorso diverso nello stesso computer o in una posizione in una rete. Nel caso di un reindirizzamento di rete, la cartella può essere memorizzata nella cache localmente attraverso la memorizzazione nella cache sul lato client per consentire l'accesso offline. Tuttavia, anche se esiste una cache locale, è necessario accedere alla cartella reindirizzata tramite la rete.

Il reindirizzamento cartelle non è una novità per Windows Vista. Ad esempio, in Windows XP alcune cartelle identificate tramite il sistema CSIDL possono essere reindirizzate tramite una chiamata a [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha) o modificando la voce di CSIDL nel registro di sistema. In Windows Vista e versioni successive, il reindirizzamento deve essere eseguito tramite [**IKnownFolder:: SEPATH**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath) o [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath).

Per determinare se è possibile reindirizzare una cartella, chiamare [**IKnownFolder:: GetRedirectionCapabilities**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities). Se non è possibile reindirizzare la cartella, questa chiamata può fornire una spiegazione.

Se una cartella viene reindirizzata a un percorso di rete, è ancora possibile chiamare i metodi [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di cartelle note](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
