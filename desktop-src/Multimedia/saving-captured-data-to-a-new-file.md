---
title: Salvataggio dei dati acquisiti in un nuovo file
description: Salvataggio dei dati acquisiti in un nuovo file
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- Messaggio WM_CAP_FILE_SAVEAS
- capFileSaveAs (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710450"
---
# <a name="saving-captured-data-to-a-new-file"></a><span data-ttu-id="d17d8-105">Salvataggio dei dati acquisiti in un nuovo file</span><span class="sxs-lookup"><span data-stu-id="d17d8-105">Saving Captured Data to a New File</span></span>

<span data-ttu-id="d17d8-106">Se l'utente desidera salvare i dati acquisiti, l'applicazione deve salvare il contenuto del file di acquisizione in un altro file usando il [**messaggio \_ \_ \_ SaveAs del file di WM Cap**](wm-cap-file-saveas.md) (o la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ).</span><span class="sxs-lookup"><span data-stu-id="d17d8-106">If the user wants to save captured data, the application should save the contents of the capture file to another file by using the [**WM\_CAP\_FILE\_SAVEAS**](wm-cap-file-saveas.md) message (or the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro).</span></span> <span data-ttu-id="d17d8-107">Questo messaggio non modifica il nome o il contenuto del file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d17d8-107">This message does not change the name or contents of the capture file.</span></span> <span data-ttu-id="d17d8-108">L'applicazione deve specificare un nome per il nuovo file perché il file di acquisizione mantiene il nome file originale.</span><span class="sxs-lookup"><span data-stu-id="d17d8-108">Your application must specify a name for the new file because the capture file retains its original filename.</span></span>

<span data-ttu-id="d17d8-109">In genere, un file di acquisizione è preallocato per il segmento di acquisizione più grande previsto e solo una parte di esso potrebbe essere usato per acquisire i dati.</span><span class="sxs-lookup"><span data-stu-id="d17d8-109">Typically, a capture file is preallocated for the largest capture segment anticipated, and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="d17d8-110">Questo messaggio copia solo la parte del file di acquisizione contenente i dati di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d17d8-110">This message copies only the portion of the capture file containing the capture data.</span></span>

 

 




