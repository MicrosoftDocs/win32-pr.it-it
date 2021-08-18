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
ms.openlocfilehash: cd44bfe1090f25cb93d8a6fa8162901eb730a53cfb9dfec7ae3f1986fa65e1db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720410"
---
# <a name="known-folders"></a>Cartelle note

Windows Vista introduce nuovi scenari di archiviazione e un nuovo spazio dei nomi del profilo utente. Per risolvere questi nuovi fattori, è stato sostituito il sistema precedente di riferimento alle cartelle standard con un [**valore CSIDL.**](csidl.md) Al Windows Vista, a tali cartelle viene fatto riferimento da un nuovo set di valori GUID denominato ID cartella nota.

Il sistema di cartelle note offre i vantaggi seguenti:

-   I fornitori di software indipendenti (ISV) possono estendere il set di ID cartella noti con i propri. Possono definire le cartelle, assegnare loro GLI ID e registrarle con il sistema. Non è stato possibile estendere i valori CSIDL.
-   È possibile enumerare tutte le cartelle note in un sistema. Nessuna API ha fornito questa funzionalità per i valori CSIDL. Per [**altre informazioni, vedere IKnownFolderManager::GetFolderIds.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids)
-   Una cartella nota aggiunta da un ISV può aggiungere proprietà personalizzate che ne spiegano lo scopo e l'uso previsto.
-   Molte cartelle note possono essere reindirizzate a nuovi percorsi, inclusi i percorsi di rete. Nel sistema CSIDL è possibile **reindirizzare solo Documenti** cartella.
-   Le cartelle note possono avere gestori personalizzati da usare durante la creazione o l'eliminazione.

Il sistema CSIDL e le API che usano i valori CSIDL sono ancora supportati per la compatibilità. Tuttavia, non è consigliabile usarli in qualsiasi nuovo sviluppo.


Negli argomenti seguenti vengono illustrate le specifiche del sistema cartelle note.

-   [Uso di cartelle note nelle applicazioni](working-with-known-folders.md)
-   [Come estendere cartelle note con cartelle personalizzate](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

Le pagine di riferimento seguenti illustrano le funzioni di Cartelle note Win32, che possono essere usate per recuperare il percorso delle cartelle note o reindirizzarle a un nuovo percorso. Queste funzioni sostituiscono le funzioni Win32 precedenti. Le nuove funzioni vengono fornite per fornire un comportamento equivalente alle funzioni precedente, ma ogni nuova funzione viene duplicata anche da un'API Component Object Model (COM).



| Nuova funzione                                             | Sostituisce                                           | Equivalente COM                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**Shgetfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**IKnownFolder::GetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**SHGetKnownFolderIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**IKnownFolder::GetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**IKnownFolder::SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

Le pagine di riferimento seguenti illustrano le API delle cartelle note COM, che forniscono tutte le funzionalità delle API Win32 elencate in precedenza, oltre alla possibilità di enumerare tutte le cartelle note, accedere alle proprietà delle cartelle note ed estendere il set standard di cartelle note.

-   [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

Un esempio C++ che illustra le API cartella nota è incluso in Windows Software Development Kit (SDK). Dopo aver installato Windows SDK nel computer, l'esempio è disponibile in %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v6.0 Samples WinUI Shell AppPlatform KnownFolders (%ProgramFiles% Microsoft SDK Windows v6.0 \\ Samples \\ WinUI Shell \\ \\ AppPlatform \\ KnownFolders).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di cartelle note](/windows/win32/shell/samples-knownfolders)
</dt> </dl>
