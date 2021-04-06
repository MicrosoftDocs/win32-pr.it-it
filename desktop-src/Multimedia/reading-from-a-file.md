---
title: Lettura da un file
description: Lettura da un file
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045131"
---
# <a name="reading-from-a-file"></a><span data-ttu-id="18634-104">Lettura da un file</span><span class="sxs-lookup"><span data-stu-id="18634-104">Reading from a File</span></span>

<span data-ttu-id="18634-105">È possibile recuperare informazioni su un file aperto utilizzando la funzione [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) .</span><span class="sxs-lookup"><span data-stu-id="18634-105">You can retrieve information about an open file by using the [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) function.</span></span> <span data-ttu-id="18634-106">Questa funzione riempie la struttura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) con informazioni quali la velocità massima dei dati, il numero di flussi nel file, se il file usa un indice e se il file è protetto da copyright.</span><span class="sxs-lookup"><span data-stu-id="18634-106">This function fills the [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) structure with such information as the maximum data rate, the number of streams in the file, whether the file uses an index, and whether the file is copyrighted.</span></span>

<span data-ttu-id="18634-107">Per recuperare informazioni supplementari in un file AVI, usare la funzione [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) .</span><span class="sxs-lookup"><span data-stu-id="18634-107">To retrieve supplementary information in an AVI file, use the [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) function.</span></span> <span data-ttu-id="18634-108">Le informazioni supplementari sono applicabili all'intero file e non sono incluse nelle intestazioni dei file normali.</span><span class="sxs-lookup"><span data-stu-id="18634-108">Supplementary information is applicable to the entire file and is not included in the normal file headers.</span></span> <span data-ttu-id="18634-109">Ad esempio, il nome della società o della persona che possiede il copyright di un file può essere costituito da informazioni supplementari.</span><span class="sxs-lookup"><span data-stu-id="18634-109">For example, the name of the company or person who holds the copyrights of a file could be supplementary information.</span></span> <span data-ttu-id="18634-110">Le informazioni supplementari non rispettano un formato specifico; può trattarsi di un file specifico.</span><span class="sxs-lookup"><span data-stu-id="18634-110">Supplementary information does not adhere to a specific format; it can be file specific.</span></span> <span data-ttu-id="18634-111">**AVIFileReadData** restituisce le informazioni supplementari in un buffer fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18634-111">**AVIFileReadData** returns the supplementary information in an application-supplied buffer.</span></span>

 

 




