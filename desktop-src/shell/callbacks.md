---
description: Questa sezione descrive le funzioni di callback Windows Shell.
title: Funzioni di callback della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d3fd334dd49d2b9cec3322630866fde4a99ccad0b5f253dd7253e551264737a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460844"
---
# <a name="shell-callback-functions"></a>Funzioni di callback della shell

Questa sezione descrive le funzioni di callback Windows Shell.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                     | Descrizione                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Specifica una funzione di callback definita dall'applicazione utilizzata per inviare ed elaborare messaggi da una finestra di dialogo Sfoglia visualizzata in risposta a una chiamata a [**SHBrowseForFolder.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) <br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | Specifica una funzione di callback definita dall'applicazione chiamata da File Manager per comunicare con un'estensione di File Manager.<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | Consente di determinare se un elemento è presente in un elenco degli elementi usati più di recente.<br/>                                                                                                                                   |
| [**ROUTINE DI MODIFICA \_ \_ PAPPSTATE**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Specifica una funzione di callback definita dall'app che notifica all'app quando l'app entra o esce da uno stato sospeso.<br/>                                                                                            |
| [**SUBCLASSPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Definisce il prototipo per la funzione di callback usata [**da RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) e [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).<br/>                                                   |
| [**FM \_ UNDELETE \_ PROC**](undeletefile.md)<br/>                     | Specifica una funzione di callback definita dall'applicazione chiamata da  File Manager quando l'utente sceglie il comando Annulla eliminazione dal menu **File.**<br/>                                                                   |



 

 

 
