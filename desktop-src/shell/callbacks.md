---
description: In questa sezione vengono descritte le funzioni di callback della shell di Windows.
title: Funzioni di callback della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401624"
---
# <a name="shell-callback-functions"></a>Funzioni di callback della shell

In questa sezione vengono descritte le funzioni di callback della shell di Windows.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                     | Descrizione                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Specifica una funzione di callback definita dall'applicazione utilizzata per inviare e elaborare messaggi da una finestra di dialogo di **esplorazione** visualizzata in risposta a una chiamata a [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).<br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | Specifica una funzione di callback definita dall'applicazione chiamata da file Manager per comunicare con un'estensione di file Manager.<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | Usato per determinare se un elemento è presente in un elenco degli ultimi elementi usati (MRU).<br/>                                                                                                                                   |
| [**\_routine di modifica PAPPSTATE \_**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Specifica una funzione di callback definita dall'app che invia una notifica all'app quando l'app entra o esce da uno stato sospeso.<br/>                                                                                            |
| [**SUBCLASSPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Definisce il prototipo per la funzione di callback utilizzata da [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) e [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).<br/>                                                   |
| [**procedura di \_ annullamento dell'eliminazione di FM \_**](undeletefile.md)<br/>                     | Specifica una funzione di callback definita dall'applicazione chiamata da file Manager quando l'utente sceglie il comando **Annulla eliminazione** dal menu **file** .<br/>                                                                   |



 

 

 
