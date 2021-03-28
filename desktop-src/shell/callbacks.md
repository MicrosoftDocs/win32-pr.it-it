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
# <a name="shell-callback-functions"></a><span data-ttu-id="b1f43-103">Funzioni di callback della shell</span><span class="sxs-lookup"><span data-stu-id="b1f43-103">Shell Callback Functions</span></span>

<span data-ttu-id="b1f43-104">In questa sezione vengono descritte le funzioni di callback della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="b1f43-104">This section describes the Windows Shell callback functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b1f43-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b1f43-105">In this section</span></span>



| <span data-ttu-id="b1f43-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="b1f43-106">Topic</span></span>                                                                     | <span data-ttu-id="b1f43-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1f43-107">Description</span></span>                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f43-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1f43-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span></span><br/>                      | <span data-ttu-id="b1f43-109">Specifica una funzione di callback definita dall'applicazione utilizzata per inviare e elaborare messaggi da una finestra di dialogo di **esplorazione** visualizzata in risposta a una chiamata a [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="b1f43-109">Specifies an application-defined callback function used to send messages to, and process messages from, a **Browse** dialog box displayed in response to a call to [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span><br/> |
| [<span data-ttu-id="b1f43-110">*FMExtensionProc*</span><span class="sxs-lookup"><span data-stu-id="b1f43-110">*FMExtensionProc*</span></span>](fmextensionproc.md)<br/>                       | <span data-ttu-id="b1f43-111">Specifica una funzione di callback definita dall'applicazione chiamata da file Manager per comunicare con un'estensione di file Manager.</span><span class="sxs-lookup"><span data-stu-id="b1f43-111">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span><br/>                                                                                            |
| [<span data-ttu-id="b1f43-112">*MRUCMPPROC*</span><span class="sxs-lookup"><span data-stu-id="b1f43-112">*MRUCMPPROC*</span></span>](mrucmpproc.md)<br/>                                 | <span data-ttu-id="b1f43-113">Usato per determinare se un elemento è presente in un elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="b1f43-113">Used to determine whether an item is present in a most recently used (MRU) list.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="b1f43-114">**\_routine di modifica PAPPSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="b1f43-114">**PAPPSTATE\_CHANGE\_ROUTINE**</span></span>](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | <span data-ttu-id="b1f43-115">Specifica una funzione di callback definita dall'app che invia una notifica all'app quando l'app entra o esce da uno stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="b1f43-115">Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.</span></span><br/>                                                                                            |
| [<span data-ttu-id="b1f43-116">**SUBCLASSPROC**</span><span class="sxs-lookup"><span data-stu-id="b1f43-116">**SUBCLASSPROC**</span></span>](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | <span data-ttu-id="b1f43-117">Definisce il prototipo per la funzione di callback utilizzata da [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) e [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span><span class="sxs-lookup"><span data-stu-id="b1f43-117">Defines the prototype for the callback function used by [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) and [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span></span><br/>                                                   |
| [<span data-ttu-id="b1f43-118">**procedura di \_ annullamento dell'eliminazione di FM \_**</span><span class="sxs-lookup"><span data-stu-id="b1f43-118">**FM\_UNDELETE\_PROC**</span></span>](undeletefile.md)<br/>                     | <span data-ttu-id="b1f43-119">Specifica una funzione di callback definita dall'applicazione chiamata da file Manager quando l'utente sceglie il comando **Annulla eliminazione** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="b1f43-119">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span><br/>                                                                   |



 

 

 
