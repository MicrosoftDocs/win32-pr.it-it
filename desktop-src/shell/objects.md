---
description: In questa sezione vengono descritti gli oggetti di Windows implementati dalla Shell.
title: Oggetti Shell per gli script e Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 52958c68edfd81771267c7a7ed29e42ab8ed1d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529424"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Oggetti Shell per gli script e Microsoft Visual Basic

In questa sezione vengono descritti gli oggetti di Windows implementati dalla Shell.

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
<td><a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br/></td>
<td>Consente a un client di gestire le impostazioni di quota disco globale del volume NTFS. Questo oggetto rende disponibili le funzionalità essenziali dell'interfaccia <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a> per gli script e le applicazioni basate su Microsoft Visual Basic.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br/></td>
<td>Consente a un amministratore di gestire le proprietà della quota disco di un volume. Il file system NTFS consente a un amministratore di gestire l'utilizzo del disco in un volume condiviso allocando a ogni utente una quantità di spazio su disco specificata o un <em>limite di quota</em>. È possibile utilizzare questo oggetto per impostare il limite di quota predefinito che verrà assegnato automaticamente a tutti i nuovi utenti.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br/></td>
<td>Riceve gli eventi di registrazione della finestra <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>ishellwindows</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Cartella</strong></a><br/></td>
<td>Rappresenta una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Cartella2</strong></a><br/></td>
<td>Estende l'oggetto <a href="folder.md"><strong>Folder</strong></a> per supportare le cartelle offline.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>FolderItem</strong></a><br/></td>
<td>Rappresenta un elemento in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>FolderItems</strong></a><br/></td>
<td>Rappresenta la raccolta di elementi in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Estende l'oggetto <a href="folderitems.md"><strong>FolderItems</strong></a> . Supporta un metodo aggiuntivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Estende l'oggetto <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> . Questo oggetto supporta un metodo e una proprietà aggiuntivi.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br/></td>
<td>Rappresenta un singolo verbo disponibile per un elemento. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sul verbo.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br/></td>
<td>Rappresenta la raccolta di verbi per un elemento in una cartella della shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br/></td>
<td>Rappresenta un oggetto nella shell. Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell. Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Estende l'oggetto <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> con un'ampia gamma di nuove funzionalità. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Estende l'oggetto <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> . <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supporta un nuovo metodo, oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch2</strong>. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Estende l'oggetto <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> . Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch3</strong>, <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supporta quattro metodi aggiuntivi. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Estende l'oggetto <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> . Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch4</strong>, <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> aggiunge un metodo che visualizza le finestre aperte in uno stack 3D. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Estende l'oggetto <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> . Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch5</strong>, <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> aggiunge un metodo che Visualizza il riquadro di ricerca delle app. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> viene implementato e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Estende l'oggetto <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> e supporta una proprietà aggiuntiva.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>NewWDEvents</strong></a><br/></td>
<td>Estende l'oggetto <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> abilitando le pagine lato server ospitate in una procedura guidata per verificare che l'utente sia stato autenticato tramite un account Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell. Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br/></td>
<td>Estende l'oggetto <a href="folderitem.md"><strong>FolderItem</strong></a> . Oltre alle proprietà e ai metodi supportati da <strong>FolderItem</strong>, <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> dispone di due metodi aggiuntivi.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br/></td>
<td>Rappresenta gli oggetti in una visualizzazione e fornisce le proprietà e i metodi utilizzati per ottenere informazioni sul contenuto della visualizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br/></td>
<td>Invia gli eventi generati da un oggetto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> specificato ai gestori eventi <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> corrispondenti.<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br/></td>
<td>Gestisce i collegamenti della shell. Questo oggetto rende la maggior parte delle funzionalità dell'interfaccia <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> disponibili per le applicazioni di scripting. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br/></td>
<td>Implementato dalla Shell per aiutare gli script e Visual Basic sviluppatori a usare alcune delle funzionalità disponibili nella shell. L'oggetto <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a> non dispone di proprietà o eventi. Sono disponibili metodi per aggiungere elementi alla Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>ShellWindows</strong></a><br/></td>
<td>Rappresenta una raccolta di finestre aperte che appartengono alla Shell. I metodi associati a questi oggetti possono controllare ed eseguire comandi all'interno della shell e ottenere altri oggetti correlati alla Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br/></td>
<td>Espone metodi che consentono le pagine HTML ospitate in un'estensione della procedura guidata per comunicare con la procedura guidata.<br/></td>
</tr>
</tbody>
</table>



 

 

 




