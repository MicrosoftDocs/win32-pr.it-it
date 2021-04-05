---
title: Salvataggio del contenuto registrato
description: Salvataggio del contenuto registrato
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- MCIWndSave (macro)
- MCIWndSaveDialog (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710447"
---
# <a name="saving-recorded-content"></a><span data-ttu-id="eaac6-105">Salvataggio del contenuto registrato</span><span class="sxs-lookup"><span data-stu-id="eaac6-105">Saving Recorded Content</span></span>

<span data-ttu-id="eaac6-106">Dopo aver completato la registrazione, è possibile salvare il contenuto usando la macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) o [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) oppure usando la funzione [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) con **MCIWndSave**.</span><span class="sxs-lookup"><span data-stu-id="eaac6-106">After completing the recording, you can save the content by using the [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) or [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro, or by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function with **MCIWndSave**.</span></span> <span data-ttu-id="eaac6-107">La macro **MCIWndSave** Salva i dati nel file associato alla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="eaac6-107">The **MCIWndSave** macro saves data in the file associated with the MCIWnd window.</span></span> <span data-ttu-id="eaac6-108">La macro **MCIWndSaveDialog** consente all'utente di specificare un nome file e salvare i dati registrati nel file specificato.</span><span class="sxs-lookup"><span data-stu-id="eaac6-108">The **MCIWndSaveDialog** macro lets the user specify a filename and save the recorded data in the specified file.</span></span> <span data-ttu-id="eaac6-109">La funzione **GetSaveFileNamePreview** Visualizza la finestra di dialogo **SaveAs** per la scelta di un file e consente all'utente di visualizzare l'anteprima (riproduzione) del file.</span><span class="sxs-lookup"><span data-stu-id="eaac6-109">The **GetSaveFileNamePreview** function displays the **SaveAs** dialog box for choosing a file and lets the user preview (play) the file.</span></span> <span data-ttu-id="eaac6-110">Quando si specifica il nome di un file esistente nella finestra di dialogo **SaveAs** , **GetSaveFileNamePreview** fornisce un piccolo controllo nella finestra di dialogo per consentire all'utente di visualizzare in anteprima il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="eaac6-110">When the name of an existing file is specified in the **SaveAs** dialog box, **GetSaveFileNamePreview** provides a small control in the dialog box to let the user preview the contents of the file.</span></span> <span data-ttu-id="eaac6-111">È possibile salvare i dati registrati in un file selezionato con **GetSaveFileNamePreview** usando **MCIWndSave**.</span><span class="sxs-lookup"><span data-stu-id="eaac6-111">You can save the recorded data in a file selected with **GetSaveFileNamePreview** by using **MCIWndSave**.</span></span>

 

 




