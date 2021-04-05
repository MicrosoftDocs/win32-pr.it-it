---
title: Stato della finestra di acquisizione
description: Stato della finestra di acquisizione
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- Messaggio WM_CAP_GET_STATUS
- capGetStatus (macro)
- Struttura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045108"
---
# <a name="capture-window-status"></a><span data-ttu-id="39bd4-106">Stato della finestra di acquisizione</span><span class="sxs-lookup"><span data-stu-id="39bd4-106">Capture Window Status</span></span>

<span data-ttu-id="39bd4-107">È possibile recuperare lo stato corrente di una finestra di acquisizione usando il messaggio di [**\_ \_ \_ stato WM Cap Get**](wm-cap-get-status.md) (o la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ).</span><span class="sxs-lookup"><span data-stu-id="39bd4-107">You can retrieve the current status of a capture window by using the [**WM\_CAP\_GET\_STATUS**](wm-cap-get-status.md) message (or the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro).</span></span> <span data-ttu-id="39bd4-108">Questo messaggio recupera una copia della struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) con i valori correnti dei relativi membri.</span><span class="sxs-lookup"><span data-stu-id="39bd4-108">This message retrieves a copy of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure with the current values of its members.</span></span> <span data-ttu-id="39bd4-109">La struttura **CAPSTATUS** contiene informazioni riguardanti le dimensioni dell'immagine, la posizione di scorrimento e se è abilitata la sovrapposizione o l'anteprima dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="39bd4-109">The **CAPSTATUS** structure contains information regarding the dimensions of the image, scroll position, and whether overlay or preview of the image is enabled.</span></span> <span data-ttu-id="39bd4-110">Poiché le informazioni rappresentate in **CAPSTATUS** sono dinamiche, l'applicazione deve aggiornare il contenuto della struttura ogni volta che è possibile che la dimensione o il formato del flusso video acquisito venga modificato (ad esempio dopo aver visualizzato il formato video del driver di acquisizione).</span><span class="sxs-lookup"><span data-stu-id="39bd4-110">Because the information represented in **CAPSTATUS** is dynamic, your application should refresh the contents of the structure whenever the size or format of the captured video stream might have changed (such as after displaying the video format of the capture driver).</span></span>

<span data-ttu-id="39bd4-111">La modifica delle dimensioni della finestra di acquisizione non ha effetto sulle dimensioni del flusso video acquisito effettivo.</span><span class="sxs-lookup"><span data-stu-id="39bd4-111">Changing the dimensions of the capture window has no effect on the dimensions of the actual captured video stream.</span></span> <span data-ttu-id="39bd4-112">La finestra di dialogo formato visualizzata dal driver del dispositivo di acquisizione video controlla le dimensioni del flusso video acquisito.</span><span class="sxs-lookup"><span data-stu-id="39bd4-112">The format dialog box displayed by the video capture device driver controls the dimensions of the captured video stream.</span></span>

 

 




