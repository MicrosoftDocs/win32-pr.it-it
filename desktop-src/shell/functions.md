---
description: In questa sezione vengono descritte le funzioni della shell di Windows.
title: Funzioni della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f4d6c0c4-8db3-4721-80f5-2a73bb57cd99
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c8e31bdaac8ec581504326c17d5d37012dd019d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994717"
---
# <a name="shell-functions"></a>Funzioni della shell

\[Questa funzione non è più implementata.\]

In questa sezione vengono descritte le funzioni della shell di Windows.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="intsafe-h-functions-bumper.md">Funzioni Intsafe. h</a><br/></td>

</tr>
<tr class="even">
<td><a href="library-functions-bumper.md">Funzioni della libreria</a><br/></td>

</tr>
<tr class="odd">
<td><a href="path-functions.md">Funzioni Path</a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a><br/></td>
<td>Recupera un oggetto che implementa un'interfaccia <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-assocgetdetailsofpropkey"><strong>AssocGetDetailsOfPropKey</strong></a><br/></td>
<td>Recupera il valore per una chiave di proprietà specificata utilizzando le informazioni di associazione file fornite dalle <a href="nse-works.md">estensioni dello spazio dei nomi</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2"><strong>CDefFolderMenu_Create2</strong></a><br/></td>
<td>Consente di creare un menu di scelta rapida per un gruppo selezionato di oggetti cartella di file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/ntquery/nf-ntquery-cishutdown"><strong>CIShutdown</strong></a><br/></td>
<td>Arresta l'indicizzatore di contenuto e chiude tutti i cataloghi aperti. <br/>
<blockquote>
[!Note]<br />
Questa funzione non è supportata a partire da Windows 8.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-commandlinetoargvw"><strong>CommandLineToArgvW</strong></a><br/></td>
<td>Analizza una stringa della riga di comando Unicode e restituisce una matrice di puntatori agli argomenti della riga di comando, insieme a un conteggio di tali argomenti, in modo analogo ai valori <em>argv</em> e <em>argc</em> della fase di esecuzione del linguaggio C standard.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>APPLET_PROC</strong></a><br/></td>
<td>Funge da punto di ingresso per un'applicazione del pannello di controllo. Si tratta di una funzione di callback definita dalla libreria.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createappcontainerprofile"><strong>CreateAppContainerProfile</strong></a><br/></td>
<td>Consente di creare un profilo per singolo utente e per app per le app di Windows Store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a><br/></td>
<td>Recupera le variabili di ambiente per l'utente specificato. Questo blocco può quindi essere passato alla funzione <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera"><strong>CreateProcessAsUser ha</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="createmrulist.md"><strong>CreateMRUListW</strong></a><br/></td>
<td>Consente di creare un nuovo elenco degli ultimi elementi usati (MRU).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createprofile"><strong>CreateProfile</strong></a><br/></td>
<td>Crea un nuovo profilo utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-defscreensaverproc"><strong>DefScreenSaverProc</strong></a><br/></td>
<td>Fornisce l'elaborazione predefinita per tutti i messaggi che non vengono elaborati da un'applicazione screen saver.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-defsubclassproc"><strong>DefSubclassProc</strong></a><br/></td>
<td>Chiama il gestore successivo nella catena di sottoclassi di una finestra. L'ultimo gestore nella catena di sottoclassi chiama la routine della finestra originale per la finestra.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteappcontainerprofile"><strong>DeleteAppContainerProfile</strong></a><br/></td>
<td>Elimina il profilo specificato per singolo utente e per app.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteprofilea"><strong>DeleteProfile</strong></a><br/></td>
<td>Elimina il profilo utente e tutte le impostazioni relative agli utenti dal computer specificato. Il chiamante deve disporre di privilegi amministrativi per eliminare il profilo di un utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock"><strong>DestroyEnvironmentBlock</strong></a><br/></td>
<td>Libera le variabili di ambiente create dalla funzione <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>CreateEnvironmentBlock</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deriveappcontainersidfromappcontainername"><strong>DeriveAppContainerSidFromAppContainerName</strong></a><br/></td>
<td>Ottiene il SID del profilo specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/userenv/nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname"><strong>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName</strong></a><br/></td>
<td>DeriveRestrictedAppContainerSidFromAppContainerSidAndRestrictedName è riservato per un uso futuro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><em>DLLGETVERSIONPROC</em></a><br/></td>
<td>Implementata da molte delle dll della shell di Windows per consentire alle applicazioni di ottenere informazioni sulla versione specifiche della DLL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles"><strong>DragAcceptFiles</strong></a><br/></td>
<td>Registra se una finestra accetta i file eliminati.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragfinish"><strong>DragFinish</strong></a><br/></td>
<td>Rilascia la memoria allocata dal sistema per il trasferimento dei nomi di file all'applicazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea"><strong>DragQueryFile</strong></a><br/></td>
<td>Recupera i nomi dei file eliminati risultanti da un'operazione di trascinamento della selezione riuscita.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint"><strong>DragQueryPoint</strong></a><br/></td>
<td>Recupera la posizione del puntatore del mouse al momento dell'eliminazione di un file durante un'operazione di trascinamento della selezione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-duplicateicon"><strong>DuplicateIcon</strong></a><br/></td>
<td>Crea un duplicato di un'icona specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera"><strong>ExpandEnvironmentStringsForUser</strong></a><br/></td>
<td>Espande la stringa di origine usando il blocco dell'ambiente stabilito per l'utente specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona"><strong>ExtractAssociatedIcon</strong></a><br/></td>
<td>Ottiene un handle per un'icona archiviata come risorsa in un file o un'icona archiviata nel file eseguibile associato a un file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona"><strong>ExtractIcon</strong></a><br/></td>
<td>Ottiene un handle per un'icona dal file eseguibile, dalla DLL o dal file di icona specificati. <br/> Per recuperare una matrice di handle a icone grandi o piccole, utilizzare la funzione <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a><br/></td>
<td>La funzione <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>ExtractIconEx</strong></a> crea una matrice di handle per icone grandi o piccole estratte dal file eseguibile, dalla dll o dal file di icona specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="fileiconinit.md"><strong>FileIconInit</strong></a><br/></td>
<td>Inizializza o reinizializza l'elenco di immagini di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-findexecutablea"><strong>FindExecutable</strong></a><br/></td>
<td>Recupera il nome e l'handle del file eseguibile (con estensione exe) associato a un file di documento specifico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/syncmgr/nf-syncmgr-freeconfirmconflictitem"><strong>FreeConfirmConflictItem</strong></a><br/></td>
<td>Libera le risorse allocate per una struttura <a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarray"><strong>FreeIDListArray</strong></a><br/></td>
<td>Libera la memoria usata da un puntatore a una matrice di elenchi PIDL (Item Identifier List).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarraychild"><strong>FreeIDListArrayChild</strong></a><br/></td>
<td>Rilascia lo spazio di memoria per la matrice di puntatori agli ID elemento figlio. Questa operazione rilascia sia la PITEMID_CHILDs all'interno della matrice sia la matrice stessa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarrayfull"><strong>FreeIDListArrayFull</strong></a><br/></td>
<td>Rilascia lo spazio di memoria per la matrice PIDL. Questa operazione rilascia sia la PIDLIST_ABSOLUTEs all'interno della matrice sia la matrice stessa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields"><strong>FreeKnownFolderDefinitionFields</strong></a><br/></td>
<td>Libera i campi allocati nel risultato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition"><strong>IKnownFolder:: GetFolderDefinition</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="freemrulist.md"><strong>FreeMRUList</strong></a><br/></td>
<td>Libera l'handle associato all'elenco MRU e scrive i dati memorizzati nella cache nel registro di sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya"><strong>GetAllUsersProfileDirectory</strong></a><br/></td>
<td>Recupera il percorso alla radice della directory che contiene i dati del programma condivisi da tutti gli utenti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerfolderpath"><strong>GetAppContainerFolderPath</strong></a><br/></td>
<td>Ottiene il percorso della cartella di dati dell'app locale per il contenitore di app specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerregistrylocation"><strong>GetAppContainerRegistryLocation</strong></a><br/></td>
<td>Ottiene la posizione dell'archiviazione del registro di sistema associata a un contenitore di app.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)"><strong>GetContractDelegateWindow</strong></a><br/></td>
<td>Recupera una finestra che è stata impostata come delegato per la finestra di primo piano principale di un'app allo scopo di associare la finestra del delegato ai contratti dell'app. Usare questa funzione se si è uno sviluppatore che scrive un'app di Windows Store in C++ nativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid"><strong>GetCurrentProcessExplicitAppUserModelID</strong></a><br/></td>
<td>Recupera l'ID del modello utente dell'applicazione esplicita definito dall'applicazione (AppUserModelID) per il processo corrente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya"><strong>GetDefaultUserProfileDirectory</strong></a><br/></td>
<td>Recupera il percorso della radice del profilo utente predefinito.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiforshelluicomponent"><strong>GetDpiForShellUiComponent</strong></a><br/></td>
<td>Recupera i punti per pollice (dpi) occupati da un <a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a> in base al fattore di scala e al <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness"><strong>PROCESS_DPI_AWARENESS</strong></a>corrente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid"><strong>GetMenuContextHelpId</strong></a><br/></td>
<td>Recupera l'identificatore di contesto della Guida associato al menu specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya"><strong>GetProfilesDirectory</strong></a><br/></td>
<td>Recupera il percorso della directory radice in cui sono archiviati i profili utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofiletype"><strong>GetProfileType</strong></a><br/></td>
<td>Recupera il tipo di profilo caricato per l'utente corrente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a><br/></td>
<td>Ottiene il fattore di scala preferito per un dispositivo di visualizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorformonitor"><strong>GetScaleFactorForMonitor</strong></a><br/></td>
<td>Ottiene il fattore di scala di un monitoraggio specifico. Questa funzione sostituisce <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>GetScaleFactorForDevice</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya"><strong>GetUserProfileDirectory</strong></a><br/></td>
<td>Recupera il percorso della directory radice del profilo utente specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid"><strong>GetWindowContextHelpId</strong></a><br/></td>
<td>Recupera l'identificatore di contesto della guida, se presente, associato alla finestra specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-getwindowsubclass"><strong>GetWindowSubclass</strong></a><br/></td>
<td>Recupera i dati di riferimento per il callback della sottoclasse della finestra specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idlistcontainerisconsistent"><strong>IDListContainerIsConsistent</strong></a><br/></td>
<td>Verifica che la struttura del contenitore di un IDList sia valida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid"><strong>ILAppendID</strong></a><br/></td>
<td>Aggiunge o antepone una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> a una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone"><strong>ILClone</strong></a><br/></td>
<td>Clona una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonechild"><strong>ILCloneChild</strong></a><br/></td>
<td>Clona una struttura figlio <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst"><strong>ILCloneFirst</strong></a><br/></td>
<td>Clona la prima struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> in una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefull"><strong>ILCloneFull</strong></a><br/></td>
<td>Clona una struttura completa, o assoluta, <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine"><strong>ILCombine</strong></a><br/></td>
<td>Combina due strutture <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcreatefrompath"><strong>ILCreateFromPath</strong></a><br/></td>
<td>Restituisce la struttura di <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ID</strong></a> oggetto associata a un percorso di file specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindchild"><strong>ILFindChild</strong></a><br/></td>
<td>Determina se una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> specificata è l'elemento figlio di un'altra struttura <strong>ItemId</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid"><strong>ILFindLastID</strong></a><br/></td>
<td>Restituisce un puntatore all'ultima struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> in una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree"><strong>ILFree</strong></a><br/></td>
<td>Libera una struttura di <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ID</strong></a> oggetto allocata dalla Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetnext"><strong>ILGetNext</strong></a><br/></td>
<td>Recupera la struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> successiva in una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetsize"><strong>ILGetSize</strong></a><br/></td>
<td>Restituisce la dimensione, in byte, di una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisaligned"><strong>ILIsAligned</strong></a><br/></td>
<td>Verifica se un elemento <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> costante è allineato a un limite del puntatore, ovvero un <strong>valore DWORD</strong> nelle architetture a 32 bit e un <strong>QWORD</strong> nelle architetture a 64 bit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilischild"><strong>ILIsChild</strong></a><br/></td>
<td>Verifica se un PIDL è un PIDL figlio, ovvero un PIDL con esattamente un <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty"><strong>ILIsEmpty</strong></a><br/></td>
<td>Verifica se una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> è vuota.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisequal"><strong>ILIsEqual</strong></a><br/></td>
<td>Verifica se due strutture <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> sono uguali in un confronto binario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisparent"><strong>ILIsParent</strong></a><br/></td>
<td>Verifica se una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> è l'elemento padre di un'altra struttura <strong>ItemId</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilnext"><strong>ILNext (PCUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Recupera la struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> successiva in una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776455(v=vs.85)"><strong>ILNext (PUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Recupera la struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> successiva in una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilremovelastid"><strong>ILRemoveLastID</strong></a><br/></td>
<td>Rimuove l'ultima struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a> da una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream"><strong>ILSaveToStream</strong></a><br/></td>
<td>Salva una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> in un flusso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilskip"><strong>ILSkip (PCUIDLIST_RELATIVE, UINT)</strong></a><br/></td>
<td>Ignora un determinato numero di byte in una struttura di <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ID</strong></a> oggetto costante, non allineata e relativa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776459(v=vs.85)"><strong>ILSkip (PUIDLIST_RELATIVE, UINT)</strong></a><br/></td>
<td>Ignora un determinato numero di byte in una struttura di <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ID</strong></a> oggetto non allineata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-inetisoffline"><strong>InetIsOffline</strong></a><br/></td>
<td>Determina se il sistema è connesso a Internet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol"><strong>InitNetworkAddressControl</strong></a><br/></td>
<td>Inizializza la classe della finestra di controllo degli indirizzi di rete.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a><br/></td>
<td>Carica il profilo utente specificato. Il profilo può essere un profilo <a href="local-user-profiles.md">utente locale</a> o un <a href="roaming-user-profiles.md">profilo utente mobile</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a><br/></td>
<td>Esegue la finestra di dialogo tipo di contenuto MIME non registrato.<br/>
<blockquote>
[!Note]<br />
Windows XP Service Pack 2 (SP2) o versione successiva: questa funzione non è più supportata.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathmakeuniquename"><strong>PathMakeUniqueName</strong></a><br/></td>
<td>Crea un nome di percorso univoco da un modello.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathyetanothermakeuniquename"><strong>PathYetAnotherMakeUniqueName</strong></a><br/></td>
<td>Crea un nome file univoco in base a un nome file esistente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a><br/></td>
<td>Consente a un'app di registrare una funzione di callback attraverso la quale può ricevere una notifica che la libreria entra o esce da uno stato di sospensione. L'app può usare queste informazioni per eseguire tutte le operazioni necessarie, ad esempio la conservazione dello stato, che devono essere eseguite in quel momento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-registerdialogclasses"><strong>RegisterDialogClasses</strong></a><br/></td>
<td>Registra le classi di finestra non standard richieste dalla finestra di dialogo di configurazione di un screen saver.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a><br/></td>
<td>Registra per un evento che viene attivato quando è possibile che la scala sia stata modificata. Questa funzione sostituisce <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>RegisterScaleChangeNotifications</strong></a><br/></td>
<td>Registra una finestra per la ricezione di callback durante il ridimensionamento delle modifiche delle informazioni.<br/>
<blockquote>
[!Note]<br />
Questa funzione non è supportata a partire da Windows 8.1. In alternativa, usare <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass"><strong>RemoveWindowSubclass</strong></a><br/></td>
<td>Rimuove un callback di sottoclasse da una finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a><br/></td>
<td>Revoca la registrazione di una finestra, impedendo la ricezione di callback durante il ridimensionamento delle modifiche delle informazioni.<br/>
<blockquote>
[!Note]<br />
Questa funzione non è supportata a partire da Windows 8.1. In alternativa, usare <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverconfiguredialog"><strong>ScreenSaverConfigureDialog</strong></a><br/></td>
<td>Riceve i messaggi inviati alla finestra di dialogo di configurazione di un screen saver. Una screen saver che consente la configurazione dell'utente deve definire questa funzione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverproc"><strong>ScreenSaverProc</strong></a><br/></td>
<td>Riceve i messaggi inviati alla finestra screen saver specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcontractdelegatewindow"><strong>SetContractDelegateWindow</strong></a><br/></td>
<td>Associa una finestra dell'app diversa dalla finestra di primo piano primaria ai contratti di un'app. Usare questa funzione se si è uno sviluppatore che scrive un'app di Windows Store in C++ nativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid"><strong>SetCurrentProcessExplicitAppUserModelID</strong></a><br/></td>
<td>Specifica un AppUserModelID univoco definito dall'applicazione che identifica il processo corrente sulla barra delle applicazioni. Questo identificatore consente a un'applicazione di raggruppare i processi e le finestre associati in un unico pulsante della barra delle applicazioni.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid"><strong>SetMenuContextHelpId</strong></a><br/></td>
<td>Associa un identificatore di contesto della guida a un menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid"><strong>SetWindowContextHelpId</strong></a><br/></td>
<td>Associa un identificatore di contesto della Guida alla finestra specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass"><strong>SetWindowSubclass</strong></a><br/></td>
<td>Installa o aggiorna un callback della sottoclasse di finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>Funzione SHAddToRecentDocs</strong></a><br/></td>
<td>Notifica al sistema che è stato eseguito l'accesso a un elemento, allo scopo di tenere traccia degli elementi utilizzati più di recente e con maggiore frequenza. Questa funzione può essere utilizzata anche per cancellare tutti i dati di utilizzo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage"><strong>SHAppBarMessage</strong></a><br/></td>
<td>Invia un messaggio AppBar al sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers"><strong>SHAssocEnumHandlers</strong></a><br/></td>
<td>Restituisce un oggetto di enumerazione per un set specificato di gestori di estensioni di file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlersforprotocolbyapplication"><strong>SHAssocEnumHandlersForProtocolByApplication</strong></a><br/></td>
<td>Ottiene un'interfaccia di enumerazione che fornisce l'accesso ai gestori associati a un protocollo specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a><br/></td>
<td>Dato un elemento dello spazio dei nomi della shell specificato sotto forma di cartella e un elenco di identificatori di elemento relativo a tale cartella, questa funzione viene associata all'elemento padre dell'elemento dello spazio dei nomi e, facoltativamente, restituisce un puntatore al componente finale dell'elenco degli identificatori di elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex"><strong>SHBindToFolderIDListParentEx</strong></a><br/></td>
<td>Estende la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>SHBindToFolderIDListParent</strong></a> consentendo al chiamante di specificare un contesto di associazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoobject"><strong>SHBindToObject</strong></a><br/></td>
<td>Recupera e associa a un oggetto specificato tramite il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> dello spazio dei nomi della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent"><strong>SHBindToParent</strong></a><br/></td>
<td>Accetta un puntatore a un elenco di identificatori di elemento completo (PIDL) e restituisce un puntatore a interfaccia specificato nell'oggetto padre.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a><br/></td>
<td>Visualizza una finestra di dialogo che consente all'utente di selezionare una cartella della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock"><strong>SHChangeNotification_Lock</strong></a><br/></td>
<td>Blocca la memoria condivisa associata a un evento di notifica della modifica della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock"><strong>SHChangeNotification_Unlock</strong></a><br/></td>
<td>Sblocca la memoria condivisa per una notifica di modifica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a><br/></td>
<td>Notifica al sistema un evento che un'applicazione ha eseguito. Un'applicazione deve usare questa funzione se esegue un'azione che può influire sulla Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister"><strong>SHChangeNotifyDeregister</strong></a><br/></td>
<td>Annulla la registrazione del processo della finestra del client dalla ricezione dei messaggi <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>SHChangeNotify</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a><br/></td>
<td>Registra una finestra per ricevere notifiche dalla file system o dalla shell, se il file system supporta le notifiche.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a><br/></td>
<td>Abilita il registro asincrono e Annulla la registrazione di un thread.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateassociationregistration"><strong>SHCreateAssociationRegistration</strong></a><br/></td>
<td>Crea un oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> in base all'implementazione predefinita dell'interfaccia fornita da Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject"><strong>SHCreateDataObject</strong></a><br/></td>
<td>Crea un oggetto dati in una cartella padre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a><br/></td>
<td>Crea un oggetto che rappresenta l'implementazione del menu di scelta rapida predefinito della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatedefaultextracticon"><strong>SHCreateDefaultExtractIcon</strong></a><br/></td>
<td>Crea un estrattore icona standard, i cui valori predefiniti possono essere ulteriormente configurati tramite l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shcreatedefaultpropertiesop"><strong>SHCreateDefaultPropertiesOp</strong></a><br/></td>
<td>Crea un'operazione su file che imposta le proprietà predefinite sull'elemento della shell che non sono già state impostate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a><br/></td>
<td>Crea e Inizializza un oggetto elemento della shell da un PIDL. L'oggetto elemento shell risultante supporta l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a><br/></td>
<td>Crea e inizializza un oggetto Shell da un nome di analisi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename"><strong>SHCreateItemFromRelativeName</strong></a><br/></td>
<td>Crea e Inizializza un oggetto elemento della shell da un nome di analisi relativo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder"><strong>SHCreateItemInKnownFolder</strong></a><br/></td>
<td>Crea un oggetto dell'elemento della Shell per un singolo file esistente all'interno di una cartella nota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a><br/></td>
<td>Creare un elemento della shell, data una cartella padre e un ID elemento figlio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a><br/></td>
<td>Crea una nuova istanza dell'oggetto visualizzazione della cartella della shell predefinita (DefView).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a><br/></td>
<td>Crea una nuova istanza dell'oggetto visualizzazione della cartella della shell predefinita. Si consiglia di usare <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> anziché questa funzione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem"><strong>SHCreateShellItem</strong></a><br/></td>
<td>Crea un oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> . <br/>
<blockquote>
[!Note]<br />
Si consiglia di utilizzare <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>SHCreateItemWithParent</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>SHCreateItemFromIDList</strong></a> anziché questa funzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray"><strong>SHCreateShellItemArray</strong></a><br/></td>
<td>Crea un oggetto matrice di elementi della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject"><strong>SHCreateShellItemArrayFromDataObject</strong></a><br/></td>
<td>Crea un oggetto matrice di elementi della shell da un oggetto dati. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists"><strong>SHCreateShellItemArrayFromIDLists</strong></a><br/></td>
<td>Crea un oggetto matrice di elementi della shell da un elenco di strutture <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem"><strong>SHCreateShellItemArrayFromShellItem</strong></a><br/></td>
<td>Crea una matrice di un elemento da un singolo elemento della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdefextracticona"><strong>SHDefExtractIcon</strong></a><br/></td>
<td>Fornisce un gestore predefinito per estrarre un'icona da un file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop"><strong>SHDoDragDrop</strong></a><br/></td>
<td>Esegue un'operazione di trascinamento della selezione. Supporta la creazione di origini di trascinamento su richiesta, nonché le immagini di trascinamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a><br/></td>
<td>Invia un messaggio all'area dello stato della barra delle applicazioni.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a><br/></td>
<td>Ottiene le coordinate dello schermo del rettangolo di delimitazione di un'icona di notifica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellabouta"><strong>ShellAbout</strong></a><br/></td>
<td>Consente di visualizzare una finestra di dialogo <strong>ShellAbout</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="shellddeinit.md"><strong>ShellDDEInit</strong></a><br/></td>
<td>Registra i servizi di Dynamic Data Exchange della shell (DDE) nel processo corrente, notificando al sistema che il processo corrente desidera ospitare oggetti DDE.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a><br/></td>
<td>Esegue un'operazione su un file specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a><br/></td>
<td>Esegue un'operazione su un file specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shemptyrecyclebina"><strong>SHEmptyRecycleBin</strong></a><br/></td>
<td>Svuota il Cestino sull'unità specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shenumerateunreadmailaccountsa"><strong>SHEnumerateUnreadMailAccounts</strong></a><br/></td>
<td>Enumera gli account utente con messaggi di posta elettronica non letti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shevaluatesystemcommandtemplate"><strong>SHEvaluateSystemCommandTemplate</strong></a><br/></td>
<td>Impone la convalida rigida dei parametri usati in una chiamata a <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> o <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a><br/></td>
<td>Copia, sposta, Rinomina o Elimina un oggetto file system. Questa funzione è stata sostituita in Windows Vista da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfreenamemappings"><strong>SHFreeNameMappings</strong></a><br/></td>
<td>Libera un oggetto mapping dei nomi di file recuperato dalla funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a><br/></td>
<td>Recupera i dati di proprietà estese da un elenco di identificatori relativi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder"><strong>SHGetDesktopFolder</strong></a><br/></td>
<td>Recupera l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> per la cartella desktop, che è la radice dello spazio dei nomi della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdiskfreespaceexa"><strong>SHGetDiskFreeSpaceEx</strong></a><br/></td>
<td>Recupera le informazioni sullo spazio su disco per un volume del disco.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdrivemedia"><strong>SHGetDriveMedia</strong></a><br/></td>
<td>Restituisce il tipo di supporto presente nell'unità specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa"><strong>SHGetFileInfo</strong></a><br/></td>
<td>Recupera le informazioni su un oggetto nel file system, ad esempio un file, una cartella, una directory o una radice dell'unità.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/mt757093(v=vs.85)"><strong>SHGetFolderPathEx</strong></a><br/></td>
<td>Recupera il percorso completo di una cartella nota identificata dal <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>della cartella. Questo consente di estendere <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a> consentendo di impostare la dimensione iniziale del buffer di stringa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa"><strong>SHGetIconOverlayIndex</strong></a><br/></td>
<td>Restituisce l'indice dell'icona di sovrapposizione nell'elenco di immagini di sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject"><strong>SHGetIDListFromObject</strong></a><br/></td>
<td>Recupera l'PIDL di un oggetto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetimagelist"><strong>SHGetImageList</strong></a><br/></td>
<td>Recupera un elenco di immagini.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer"><strong>SHGetInstanceExplorer</strong></a><br/></td>
<td>Recupera un'interfaccia che consente alle estensioni della shell ospitata e ad altri componenti di impedire che il processo host venga chiuso in modo anomalo. Il processo host è in genere Windows Explorer o Windows Internet Explorer, ma questa funzione può essere utilizzata anche da altre applicazioni.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a><br/></td>
<td>Crea un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> o un oggetto correlato in base a un elemento specificato da un <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject"><strong>SHGetItemFromObject</strong></a><br/></td>
<td>Recupera un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> per un oggetto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist"><strong>SHGetKnownFolderIDList</strong></a><br/></td>
<td>Recupera il percorso di una cartella nota come una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ItemId</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem"><strong>SHGetKnownFolderItem</strong></a><br/></td>
<td>Recupera un oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> che rappresenta una cartella nota.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>SHGetKnownFolderPath</strong></a><br/></td>
<td>Recupera il percorso completo di una cartella nota identificata dal <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a>della cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetlocalizedname"><strong>SHGetLocalizedName</strong></a><br/></td>
<td>Recupera il nome localizzato di un file in una cartella della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a><br/></td>
<td>Recupera il nome visualizzato di un elemento identificato dal relativo IDList.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762192(v=vs.85)"><strong>SHGetNameFromPropertyKey</strong></a><br/></td>
<td>Recupera il nome canonico della proprietà dato il relativo <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetnewlinkinfoa"><strong>SHGetNewLinkInfo</strong></a><br/></td>
<td>Crea un nome per un nuovo tasto di scelta rapida basato sulla destinazione proposta del collegamento. Questa funzione non crea il collegamento, bensì solo il nome.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a><br/></td>
<td>Converte un elenco di identificatori di elemento in un percorso di file system.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex"><strong>SHGetPathFromIDListEx</strong></a><br/></td>
<td>Converte un elenco di identificatori di elemento in un percorso di file system. Questa funzione estende <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>SHGetPathFromIDList</strong></a> consentendo di impostare la dimensione iniziale del buffer di stringa e dichiarare le opzioni seguenti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a><br/></td>
<td>Recupera le impostazioni correnti delle opzioni della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a><br/></td>
<td>Recupera informazioni sulle icone della shell definite dal sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem"><strong>SHGetTemporaryPropertyForItem</strong></a><br/></td>
<td>Recupera la proprietà temporanea per l'elemento specificato. Una proprietà temporanea è un archivio di lettura/scrittura che include proprietà solo per la durata dell'oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> , anziché essere salvato in maniera permanente nell'elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetunreadmailcountw"><strong>SHGetUnreadMailCount</strong></a><br/></td>
<td>Recupera il numero di messaggi non letti di un utente specificato per uno o tutti gli account di posta elettronica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shisfileavailableoffline"><strong>SHIsFileAvailableOffline</strong></a><br/></td>
<td>Determina se un file o una cartella è disponibile per l'utilizzo offline. Questa funzione determina anche se il file viene aperto dalla rete, dalla cache File offline locale o da entrambe le posizioni.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shloadinproc"><strong>SHLoadInProc</strong></a><br/></td>
<td>Crea un'istanza della classe di oggetti specificata dall'interno del contesto del processo della shell. <br/> <strong>Windows Vista</strong> e versioni successive: questa funzione è stata disabilitata e restituisce E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shloadnonloadediconoverlayidentifiers"><strong>SHLoadNonloadedIconOverlayIdentifiers</strong></a><br/></td>
<td>Segnala alla shell che durante l'operazione successiva la richiesta di informazioni sovrapposte dovrebbe caricare gli identificatori di sovrimpressione delle icone che non sono riusciti a creare o che non erano presenti per la creazione all'avvio. Gli identificatori che sono già stati caricati non sono interessati.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlocalstrdupa"><strong>SHLocalStrDup</strong></a><br/></td>
<td>Crea una copia di una stringa nella memoria appena allocata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shmultifileproperties"><strong>SHMultiFileProperties</strong></a><br/></td>
<td>Visualizza una finestra delle proprietà unita per un set di file. I valori delle proprietà comuni a tutti i file vengono visualizzati mentre quelli che differiscono visualizzano la stringa <strong>(più valori)</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenfolderandselectitems"><strong>SHOpenFolderAndSelectItems</strong></a><br/></td>
<td>Apre una finestra di Esplora risorse con gli elementi specificati in una determinata cartella selezionata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a><br/></td>
<td>Consente di visualizzare la finestra <strong>di dialogo Apri con</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/showsharefolderui"><strong>ShowShareFolderUI</strong></a><br/></td>
<td>Consente di visualizzare la scheda <strong>condivisione cartelle</strong> nella finestra delle proprietà per la cartella specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname"><strong>SHParseDisplayName</strong></a><br/></td>
<td>Converte il nome visualizzato di un oggetto spazio dei nomi della shell in un elenco di identificatori di elemento e restituisce gli attributi dell'oggetto. Questa funzione è il metodo preferito per convertire una stringa in un PIDL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shpathprepareforwritea"><strong>SHPathPrepareForWrite</strong></a><br/></td>
<td>Verifica se il percorso esiste. Ciò include il rimontaggio delle unità di rete mappate, la richiesta di reinserimento di supporti esportabili, la creazione dei percorsi, la richiesta di formattazione del supporto e la specifica delle interfacce utente appropriate, se necessario. Le autorizzazioni di lettura/scrittura per il supporto non vengono controllate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a><br/></td>
<td>Recupera le dimensioni del cestino e il numero di elementi in esso contenuti, per un'unità specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a><br/></td>
<td>Controlla lo stato del computer per l'utente corrente per determinare se l'invio di una notifica è appropriato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shremovelocalizedname"><strong>SHRemoveLocalizedName</strong></a><br/></td>
<td>Rimuove il nome localizzato di un file in una cartella della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shruncontrolpanel"><strong>SHRunControlPanel</strong></a><br/></td>
<td>Apre un elemento del pannello di controllo. <br/>
<blockquote>
[!Note]<br />
Questa funzione non è supportata a partire da Windows Vista
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shsetdefaultproperties"><strong>SHSetDefaultProperties</strong></a><br/></td>
<td>Applica il set predefinito di proprietà in un elemento della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer"><strong>SHSetInstanceExplorer</strong></a><br/></td>
<td>Fornisce un'interfaccia che consente alle estensioni della shell ospitata e ad altri componenti di impedire la chiusura anomala del processo host. Il processo host è in genere Esplora risorse o Internet Explorer, ma questa funzione può essere utilizzata anche da altre applicazioni.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath"><strong>SHSetKnownFolderPath</strong></a><br/></td>
<td>Reindirizza una cartella nota a una nuova posizione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetlocalizedname"><strong>SHSetLocalizedName</strong></a><br/></td>
<td>Imposta il nome localizzato di un file in una cartella della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem"><strong>SHSetTemporaryPropertyForItem</strong></a><br/></td>
<td>Imposta una proprietà temporanea per l'elemento specificato. Una proprietà temporanea viene mantenuta in un archivio di lettura/scrittura che include proprietà solo per la durata dell'oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> , invece di scriverle nuovamente nell'elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetunreadmailcountw"><strong>SHSetUnreadMailCount</strong></a><br/></td>
<td>Archivia il numero di messaggi non letti dell'utente corrente per un account di posta elettronica specificato nel registro di sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shtesttokenmembership"><strong>SHTestTokenMembership</strong></a><br/></td>
<td>USA <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership"><strong>CheckTokenMembership</strong></a> per verificare se il token specificato è un membro del gruppo locale con il RID specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea"><strong>SHUpdateImage</strong></a><br/></td>
<td>Notifica alla shell che un'immagine nell'elenco di immagini di sistema è stata modificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-softwareupdatemessagebox"><strong>SoftwareUpdateMessageBox</strong></a><br/></td>
<td>Visualizza una finestra di messaggio standard che può essere utilizzata per notificare a un utente che un'applicazione è stata aggiornata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-stgmakeuniquename"><strong>StgMakeUniqueName</strong></a><br/></td>
<td>Crea un nome univoco per un flusso o un oggetto di archiviazione da un modello.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrniw"><strong>StrStrNIW</strong></a><br/></td>
<td>Trova la prima occorrenza di una sottostringa all'interno di una stringa. Il confronto viene eseguito senza distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrnw"><strong>StrStrNW</strong></a><br/></td>
<td>Trova la prima occorrenza di una sottostringa all'interno di una stringa. Il confronto fa distinzione tra maiuscole e minuscole.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TranslateURL</strong></a><br/></td>
<td>Applica le traduzioni comuni a una determinata stringa URL, creando una nuova stringa URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile"><strong>UnloadUserProfile</strong></a><br/></td>
<td>Scarica un profilo utente caricato dalla funzione <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a> . Il chiamante deve disporre di privilegi amministrativi nel computer. Per ulteriori informazioni, vedere la sezione Osservazioni della funzione <strong>LoadUserProfile</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification"><strong>UnregisterAppStateChangeNotification</strong></a><br/></td>
<td>Annulla una notifica di modifica registrata tramite <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>RegisterAppStateChangeNotification</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>UnregisterScaleChangeEvent</strong></a><br/></td>
<td>Annulla la registrazione per l'evento di modifica della scala registrato tramite <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>RegisterScaleChangeEvent</strong></a>. Questa funzione sostituisce <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>RevokeScaleChangeNotifications</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLAssociationDialog</strong></a><br/></td>
<td>Richiama la finestra di dialogo protocollo URL non registrato. Questa finestra di dialogo consente all'utente di selezionare un'applicazione da associare a un protocollo precedentemente sconosciuto.<br/>
<blockquote>
[!Note]<br />
Windows XP SP2 o versione successiva: questa funzione non è più supportata.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb762266(v=vs.85)"><strong>WinExecError</strong></a><br/></td>
<td>Recupera il valore di errore generato se la funzione <a href="/windows/win32/api/winbase/nf-winbase-winexec">WinExec</a> non è in grado di eseguire un'applicazione specificata. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a><br/></td>
<td>Avvia la Guida di Windows (Winhelp.exe) e passa dati aggiuntivi che indicano la natura della guida richiesta dall'applicazione.<br/></td>
</tr>
</tbody>
</table>



 

 

 
