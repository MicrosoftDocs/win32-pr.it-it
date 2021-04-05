---
title: Consentire all'utente di specificare i dispositivi e i file
description: Consentire all'utente di specificare i dispositivi e i file
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog (macro)
- MCIWndOpen (macro)
- MCIWndOpenInterface (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710984"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a><span data-ttu-id="cc9b5-106">Consentire all'utente di specificare i dispositivi e i file</span><span class="sxs-lookup"><span data-stu-id="cc9b5-106">Allowing the User to Specify Devices and Files</span></span>

<span data-ttu-id="cc9b5-107">È possibile associare un dispositivo o un file a una finestra MCIWnd esistente usando le macro [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)e [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) e la funzione [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .</span><span class="sxs-lookup"><span data-stu-id="cc9b5-107">You can associate a device or file with an existing MCIWnd window by using the [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen), and [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macros, and the [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) function.</span></span>

<span data-ttu-id="cc9b5-108">Per consentire a un utente dell'applicazione di selezionare un file da riprodurre, usare **MCIWndOpenDialog**.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-108">To let a user of your application select a file to play, use **MCIWndOpenDialog**.</span></span> <span data-ttu-id="cc9b5-109">Questa macro Visualizza la finestra di dialogo **Apri** (mostrata nella schermata seguente) per la scelta di un file e associa il file selezionato alla finestra MCIWnd corrente.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-109">This macro displays the **Open** dialog box (shown in the following screen shot) for choosing a file and associates the selected file with the current MCIWnd window.</span></span>

![immagine della finestra MCIWnd](images/mciwnd3.gif)

<span data-ttu-id="cc9b5-111">È possibile consentire a un utente dell'applicazione di selezionare un file da associare a una finestra MCIWnd e di visualizzare in anteprima il file usando [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) e [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span><span class="sxs-lookup"><span data-stu-id="cc9b5-111">You can let a user of your application select a file to associate with an MCIWnd window and preview that file by using [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span></span> <span data-ttu-id="cc9b5-112">La funzione **GetOpenFileNamePreview** Visualizza la finestra di dialogo **Apri** per la scelta di un file e consente all'utente di visualizzare in anteprima (riprodurre) il contenuto.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-112">The **GetOpenFileNamePreview** function displays the **Open** dialog box for choosing a file and lets the user preview (play) its contents.</span></span> <span data-ttu-id="cc9b5-113">Quando si specifica il nome di un file esistente nella finestra di dialogo, **GetOpenFileNamePreview** fornisce un piccolo controllo che consente all'utente di visualizzare in anteprima il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-113">When the name of an existing file is specified in the dialog box, **GetOpenFileNamePreview** provides a small control to let the user preview the contents of the file.</span></span> <span data-ttu-id="cc9b5-114">È possibile associare un file specificato, selezionato con **GetOpenFileNamePreview** o specificato in un altro modo, con una finestra MCIWnd usando **MCIWndOpen**.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-114">You can associate a specified file, selected with **GetOpenFileNamePreview** or specified in another manner, with an MCIWnd window by using **MCIWndOpen**.</span></span>

<span data-ttu-id="cc9b5-115">È anche possibile usare **MCIWndOpen** per specificare un dispositivo da associare a una finestra di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-115">You can also use **MCIWndOpen** to specify a device to associate with an MCIWnd window.</span></span> <span data-ttu-id="cc9b5-116">Ad esempio, è possibile usare un nome di dispositivo, ad esempio "CDAudio".</span><span class="sxs-lookup"><span data-stu-id="cc9b5-116">For example, you can use a device name, such as "CDAudio".</span></span>

<span data-ttu-id="cc9b5-117">Per associare una finestra MCIWnd con un'interfaccia di file o un'interfaccia del flusso di dati ai dati multimediali, usare la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="cc9b5-117">To associate an MCIWnd window with a file interface or data-stream interface to multimedia data, use the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span> <span data-ttu-id="cc9b5-118">Per altre informazioni sulle interfacce di flusso di dati e file, vedere [funzioni e macro di avifile](avifile-functions-and-macros.md).</span><span class="sxs-lookup"><span data-stu-id="cc9b5-118">For more information about file and data-stream interfaces, see [AVIFile Functions and Macros](avifile-functions-and-macros.md).</span></span>

> [!Note]  
> <span data-ttu-id="cc9b5-119">Prima di associare un nuovo file o dispositivo a una finestra MCIWnd, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) e [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) chiudono tutti i dispositivi attualmente associati alla finestra.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-119">Before associating a new file or device with an MCIWnd window, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) close any device currently associated with the window.</span></span> <span data-ttu-id="cc9b5-120">Non è necessario che l'applicazione chiuda tutti i dispositivi aperti prima di usare queste macro.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-120">Your application does not need to close any open devices before using these macros.</span></span>

 

 

 




