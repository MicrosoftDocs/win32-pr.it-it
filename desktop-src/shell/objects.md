---
description: In questa sezione vengono descritti Windows oggetti implementati da Shell.
title: Oggetti shell per script e Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bd2c924d9b66194c8f016fc8b1c16bed8a7e3c62f82e3673837e0e31c8563fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858800"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Oggetti shell per script e Microsoft Visual Basic

In questa sezione vengono descritti Windows oggetti implementati da Shell.

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
<td>Consente a un client di gestire le impostazioni della quota disco globale di un volume NTFS. Questo oggetto rende disponibili le funzionalità essenziali <a href="didiskquotauser-object.md"><strong>dell'interfaccia DIDiskQuotaUser</strong></a> per gli script e le applicazioni basate Visual Basic Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br/></td>
<td>Consente a un amministratore di gestire le proprietà della quota disco di un volume. Il file system NTFS consente a un amministratore di gestire l'utilizzo del disco in un volume condiviso allocando una quantità specificata di spazio su disco, o limite di <em>quota,</em>a ogni utente. È possibile usare questo oggetto per impostare il limite di quota predefinito che verrà assegnato automaticamente a tutti i nuovi utenti.<br/></td>
</tr>
<tr class="odd">
<td><a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br/></td>
<td>Riceve gli <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>eventi di registrazione della finestra IShellWindows.</strong></a> <br/></td>
</tr>
<tr class="even">
<td><a href="folder.md"><strong>Cartella</strong></a><br/></td>
<td>Rappresenta una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="folder2-object.md"><strong>Cartella2</strong></a><br/></td>
<td>Estende <a href="folder.md"><strong>l'oggetto Folder</strong></a> per supportare le cartelle offline.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitem.md"><strong>FolderItem</strong></a><br/></td>
<td>Rappresenta un elemento in una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems.md"><strong>FolderItems</strong></a><br/></td>
<td>Rappresenta la raccolta di elementi in una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br/></td>
<td>Estende <a href="folderitems.md"><strong>l'oggetto FolderItems.</strong></a> Supporta un metodo aggiuntivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br/></td>
<td>Estende <a href="folderitems2-object.md"><strong>l'oggetto FolderItems2.</strong></a> Questo oggetto supporta un metodo e una proprietà aggiuntivi.<br/></td>
</tr>
<tr class="even">
<td><a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br/></td>
<td>Rappresenta un singolo verbo disponibile per un elemento. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sul verbo.<br/></td>
</tr>
<tr class="odd">
<td><a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br/></td>
<td>Rappresenta la raccolta di verbi per un elemento in una cartella Shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br/></td>
<td>Rappresenta un oggetto nella shell. Vengono forniti metodi per controllare shell ed eseguire comandi all'interno della shell. Esistono anche metodi per ottenere altri oggetti correlati alla shell. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch.md"><strong>IShellDispatch viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br/></td>
<td>Estende <a href="ishelldispatch.md"><strong>l'oggetto IShellDispatch</strong></a> con un'ampia gamma di nuove funzionalità. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch2-object.md"><strong>IShellDispatch2 viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br/></td>
<td>Estende <a href="ishelldispatch2-object.md"><strong>l'oggetto IShellDispatch2.</strong></a> <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supporta un nuovo metodo oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch2.</strong> <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch3.md"><strong>IShellDispatch3 viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br/></td>
<td>Estende <a href="ishelldispatch3.md"><strong>l'oggetto IShellDispatch3.</strong></a> Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch3,</strong> <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supporta quattro metodi aggiuntivi. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch4.md"><strong>IShellDispatch4 viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br/></td>
<td>Estende <a href="ishelldispatch4.md"><strong>l'oggetto IShellDispatch4.</strong></a> Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch4,</strong> <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> aggiunge un metodo che visualizza le finestre aperte in uno stack 3D. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch5.md"><strong>IShellDispatch5 viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br/></td>
<td>Estende <a href="ishelldispatch5.md"><strong>l'oggetto IShellDispatch5.</strong></a> Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch5,</strong> <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> aggiunge un metodo che visualizza il riquadro Ricerca app. <br/>
<blockquote>
[!Note]<br />
<a href="ishelldispatch6.md"><strong>IShellDispatch6 viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br/></td>
<td>Estende <a href="shelllinkobject-object.md"><strong>l'oggetto ShellLinkObject</strong></a> e supporta una proprietà aggiuntiva.<br/></td>
</tr>
<tr class="odd">
<td><a href="newwdevents.md"><strong>NewWDEvents</strong></a><br/></td>
<td>Estende <a href="webwizardhost.md"><strong>l'oggetto WebWizardHost</strong></a> abilitando le pagine sul lato server ospitate in una procedura guidata per verificare che l'utente sia stato autenticato tramite un account Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="shell.md"><strong>Shell</strong></a><br/></td>
<td>Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare shell ed eseguire comandi all'interno della shell. Esistono anche metodi per ottenere altri oggetti correlati alla shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br/></td>
<td>Estende <a href="folderitem.md"><strong>l'oggetto FolderItem.</strong></a> Oltre alle proprietà e ai metodi supportati da <strong>FolderItem,</strong> <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> dispone di due metodi aggiuntivi.<br/></td>
</tr>
<tr class="even">
<td><a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br/></td>
<td>Rappresenta gli oggetti in una vista e fornisce proprietà e metodi utilizzati per ottenere informazioni sul contenuto della vista.<br/></td>
</tr>
<tr class="odd">
<td><a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br/></td>
<td>Inoltra gli eventi generati da un oggetto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> specificato ai gestori <a href="shellfolderviewoc-object.md"><strong>eventi ShellFolderViewOC</strong></a> corrispondenti.<br/></td>
</tr>
<tr class="even">
<td><a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br/></td>
<td>Gestisce i collegamenti di Shell. Questo oggetto rende disponibile gran parte delle funzionalità <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>dell'interfaccia IShellLink</strong></a> per le applicazioni di scripting. <br/></td>
</tr>
<tr class="odd">
<td><a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br/></td>
<td>Implementato da Shell per consentire agli sviluppatori di creare script e Visual Basic usano alcune delle funzionalità disponibili in Shell. <a href="shelluihelper.md"><strong>L'oggetto ShellUIHelper</strong></a> non ha proprietà o eventi. Vengono forniti metodi per aggiungere elementi alla shell.<br/></td>
</tr>
<tr class="even">
<td><a href="shellwindows.md"><strong>ShellWindows</strong></a><br/></td>
<td>Rappresenta una raccolta delle finestre aperte che appartengono alla shell. I metodi associati a questo oggetto possono controllare ed eseguire comandi all'interno della shell e ottenere altri oggetti correlati alla shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br/></td>
<td>Espone metodi che consentono alle pagine HTML ospitate in un'estensione della procedura guidata di comunicare con la procedura guidata.<br/></td>
</tr>
</tbody>
</table>



 

 

 




