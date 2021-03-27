---
description: Windows Vista introduce nuovi scenari di archiviazione e un nuovo spazio dei nomi del profilo utente.
title: Cartelle note
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980242"
---
# <a name="known-folders"></a>Cartelle note

Windows Vista introduce nuovi scenari di archiviazione e un nuovo spazio dei nomi del profilo utente. Per risolvere questi nuovi fattori, il sistema precedente di riferimento alle cartelle standard da un valore [**CSIDL**](csidl.md) è stato sostituito. A partire da Windows Vista, a tali cartelle viene fatto riferimento da un nuovo set di valori GUID detti ID cartella noti.

Il sistema di cartelle note offre i vantaggi seguenti:

-   I fornitori di software indipendenti (ISV) possono estendere il set di ID cartella note con i rispettivi. Possono definire cartelle, assegnare loro ID e registrarle nel sistema. Non è stato possibile estendere i valori CSIDL.
-   È possibile enumerare tutte le cartelle note in un sistema. Nessuna API ha fornito questa funzionalità per i valori CSIDL. Per ulteriori informazioni, vedere [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) .
-   Una cartella nota aggiunta da un ISV può aggiungere proprietà personalizzate che consentono di spiegarne lo scopo e l'utilizzo previsto.
-   Molte cartelle note possono essere reindirizzate a nuove posizioni, inclusi i percorsi di rete. Nel sistema CSIDL è possibile reindirizzare solo la cartella **documenti** .
-   Le cartelle note possono avere gestori personalizzati da usare durante la creazione o l'eliminazione.

Il sistema CSIDL e le API che usano i valori CSIDL sono ancora supportati per garantire la compatibilità. Tuttavia, non è consigliabile usarli in un nuovo sviluppo.


Negli argomenti seguenti vengono illustrate le specifiche del sistema di cartelle note.

-   [Utilizzo di cartelle note nelle applicazioni](working-with-known-folders.md)
-   [Come estendere le cartelle note con cartelle personalizzate](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

Le pagine di riferimento seguenti illustrano le funzioni delle cartelle note Win32, che possono essere usate per recuperare il percorso delle cartelle note o reindirizzarle a una nuova posizione. Queste funzioni sostituiscono le funzioni Win32 precedenti. Le nuove funzioni vengono fornite per fornire un comportamento equivalente alle funzioni precedenti, ma ogni nuova funzione viene duplicata anche da un'API Component Object Model (COM).



| Nuova funzione                                             | Sostituisce                                           | Equivalente COM                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**IKnownFolder:: GetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**SHGetKnownFolderIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**IKnownFolder::GetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**IKnownFolder:: SEPATH**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

Le pagine di riferimento seguenti illustrano le API di cartelle note di COM, che forniscono tutte le funzionalità delle API Win32 elencate in precedenza, oltre ad aggiungere la possibilità di enumerare tutte le cartelle note, accedere alle proprietà della cartella note ed estendere il set standard di cartelle note.

-   [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

Un esempio di C++ che illustra le API delle cartelle note è incluso in Windows Software Development Kit (SDK). Una volta installato il Windows SDK nel computer, l'esempio si trova in% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppPlatform \\ KnownFolders.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di cartelle note](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
