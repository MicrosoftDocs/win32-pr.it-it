---
description: In questa sezione vengono descritti Windows oggetti implementati dalla shell.
title: Oggetti shell per script e Microsoft Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e4d367b836516259a4c0f73cea9da20e7e13326
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465028"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>Oggetti shell per script e Microsoft Visual Basic

In questa sezione vengono descritti Windows oggetti implementati dalla shell.

## <a name="in-this-section"></a>Contenuto della sezione




| Argomento | Descrizione | 
|-------|-------------|
| <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br /> | Consente a un client di gestire le impostazioni di quota disco globale di un volume NTFS. Questo oggetto rende disponibili le funzionalità essenziali <a href="didiskquotauser-object.md"><strong>dell'interfaccia DIDiskQuotaUser</strong></a> per le applicazioni basate Visual Basic Microsoft.<br /> | 
| <a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br /> | Consente a un amministratore di gestire le proprietà della quota disco di un volume. Il file system NTFS consente a un amministratore di gestire l'utilizzo del disco in un volume condiviso allocando una quantità specificata di spazio su disco, o limite di <em>quota,</em>a ogni utente. È possibile usare questo oggetto per impostare il limite di quota predefinito che verrà assegnato automaticamente a tutti i nuovi utenti.<br /> | 
| <a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br /> | Riceve gli <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>eventi di registrazione della finestra IShellWindows.</strong></a> <br /> | 
| <a href="folder.md"><strong>Cartella</strong></a><br /> | Rappresenta una cartella shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla cartella.<br /> | 
| <a href="folder2-object.md"><strong>Cartella2</strong></a><br /> | Estende <a href="folder.md"><strong>l'oggetto Folder</strong></a> per supportare le cartelle offline.<br /> | 
| <a href="folderitem.md"><strong>FolderItem</strong></a><br /> | Rappresenta un elemento in una cartella shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sull'elemento.<br /> | 
| <a href="folderitems.md"><strong>FolderItems</strong></a><br /> | Rappresenta la raccolta di elementi in una cartella shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.<br /> | 
| <a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br /> | Estende <a href="folderitems.md"><strong>l'oggetto FolderItems.</strong></a> Supporta un metodo aggiuntivo.<br /> | 
| <a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br /> | Estende <a href="folderitems2-object.md"><strong>l'oggetto FolderItems2.</strong></a> Questo oggetto supporta un metodo e una proprietà aggiuntivi.<br /> | 
| <a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br /> | Rappresenta un singolo verbo disponibile per un elemento. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sul verbo.<br /> | 
| <a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br /> | Rappresenta la raccolta di verbi per un elemento in una cartella shell. Questo oggetto contiene proprietà e metodi che consentono di recuperare informazioni sulla raccolta.<br /> | 
| <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br /> | Rappresenta un oggetto nella shell. Vengono forniti metodi per controllare la shell ed eseguire comandi all'interno della shell. Sono disponibili anche metodi per ottenere altri oggetti correlati alla shell. <br /><blockquote>[!Note]<br /><a href="ishelldispatch.md"><strong>IShellDispatch viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br /> | Estende <a href="ishelldispatch.md"><strong>l'oggetto IShellDispatch</strong></a> con un'ampia gamma di nuove funzionalità. <br /><blockquote>[!Note]<br /><a href="ishelldispatch2-object.md"><strong>IShellDispatch2 viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br /> | Estende <a href="ishelldispatch2-object.md"><strong>l'oggetto IShellDispatch2.</strong></a> <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> supporta un nuovo metodo oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch2.</strong> <br /><blockquote>[!Note]<br /><a href="ishelldispatch3.md"><strong>IShellDispatch3 viene implementato</strong></a> e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br /> | Estende <a href="ishelldispatch3.md"><strong>l'oggetto IShellDispatch3.</strong></a> Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch3,</strong> <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> supporta quattro metodi aggiuntivi. <br /><blockquote>[!Note]<br /><a href="ishelldispatch4.md"><strong>IShellDispatch4 viene implementato</strong></a> e accessibile tramite l'oggetto <a href="shell.md"><strong>Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br /> | Estende <a href="ishelldispatch4.md"><strong>l'oggetto IShellDispatch4.</strong></a> Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch4,</strong> <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> aggiunge un metodo che visualizza le finestre aperte in uno stack 3D. <br /><blockquote>[!Note]<br /><a href="ishelldispatch5.md"><strong>IShellDispatch5 viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br /> | Estende <a href="ishelldispatch5.md"><strong>l'oggetto IShellDispatch5.</strong></a> Oltre alle proprietà e ai metodi supportati da <strong>IShellDispatch5,</strong> <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> aggiunge un metodo che visualizza il riquadro Ricerca app. <br /><blockquote>[!Note]<br /><a href="ishelldispatch6.md"><strong>IShellDispatch6 viene</strong></a> implementato e accessibile tramite <a href="shell.md"><strong>l'oggetto Shell.</strong></a></blockquote><br /> | 
| <a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br /> | Estende <a href="shelllinkobject-object.md"><strong>l'oggetto ShellLinkObject</strong></a> e supporta una proprietà aggiuntiva.<br /> | 
| <a href="newwdevents.md"><strong>NewWDEvents</strong></a><br /> | Estende <a href="webwizardhost.md"><strong>l'oggetto WebWizardHost</strong></a> abilitando le pagine sul lato server ospitate in una procedura guidata per verificare che l'utente sia stato autenticato tramite un account Microsoft.<br /> | 
| <a href="shell.md"><strong>Shell</strong></a><br /> | Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare la shell ed eseguire comandi all'interno della shell. Sono disponibili anche metodi per ottenere altri oggetti correlati alla shell.<br /> | 
| <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br /> | Estende <a href="folderitem.md"><strong>l'oggetto FolderItem.</strong></a> Oltre alle proprietà e ai metodi supportati da <strong>FolderItem,</strong> <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> dispone di due metodi aggiuntivi.<br /> | 
| <a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br /> | Rappresenta gli oggetti in una visualizzazione e fornisce le proprietà e i metodi utilizzati per ottenere informazioni sul contenuto della visualizzazione.<br /> | 
| <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br /> | Inoltra gli eventi generati da un oggetto <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> specificato ai gestori <a href="shellfolderviewoc-object.md"><strong>eventi ShellFolderViewOC</strong></a> corrispondenti.<br /> | 
| <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br /> | Gestisce i collegamenti della shell. Questo oggetto rende disponibile gran parte delle funzionalità <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>dell'interfaccia IShellLink</strong></a> alle applicazioni di scripting. <br /> | 
| <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br /> | Implementato dalla shell per consentire agli sviluppatori Visual Basic script di usare alcune delle funzionalità disponibili nella shell. <a href="shelluihelper.md"><strong>L'oggetto ShellUIHelper</strong></a> non ha proprietà o eventi. Vengono forniti metodi per aggiungere elementi alla shell.<br /> | 
| <a href="shellwindows.md"><strong>ShellWindows</strong></a><br /> | Rappresenta una raccolta di finestre aperte che appartengono alla shell. I metodi associati a questi oggetti possono controllare ed eseguire comandi all'interno della shell e ottenere altri oggetti correlati alla shell.<br /> | 
| <a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br /> | Espone metodi che consentono alle pagine HTML ospitate in un'estensione della procedura guidata di comunicare con la procedura guidata.<br /> | 




 

 

 




