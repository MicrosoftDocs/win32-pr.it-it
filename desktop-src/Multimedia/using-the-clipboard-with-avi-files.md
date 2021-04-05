---
title: Uso degli Appunti con file AVI
description: Uso degli Appunti con file AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- AVIPutFileOnClipboard (funzione)
- AVIGetFromClipboard (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710621"
---
# <a name="using-the-clipboard-with-avi-files"></a><span data-ttu-id="fad01-105">Uso degli Appunti con file AVI</span><span class="sxs-lookup"><span data-stu-id="fad01-105">Using the Clipboard with AVI Files</span></span>

<span data-ttu-id="fad01-106">Gli appunti forniscono un'archiviazione temporanea e pratica che un'applicazione può usare per copiare o trasferire file AVI.</span><span class="sxs-lookup"><span data-stu-id="fad01-106">The clipboard provides convenient, temporary storage that an application can use to copy or transfer AVI files.</span></span> <span data-ttu-id="fad01-107">AVIFile include funzioni degli appunti che è possibile usare con i file di disco o di memoria.</span><span class="sxs-lookup"><span data-stu-id="fad01-107">AVIFile includes clipboard functions that you can use with disk or memory files.</span></span>

<span data-ttu-id="fad01-108">È possibile copiare un file negli appunti usando la funzione [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) .</span><span class="sxs-lookup"><span data-stu-id="fad01-108">You can copy a file to the clipboard by using the [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) function.</span></span> <span data-ttu-id="fad01-109">Per scrivere un file negli Appunti in memoria o disco, usare la funzione [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .</span><span class="sxs-lookup"><span data-stu-id="fad01-109">To write a file that is on the clipboard to memory or disk, use the [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) function.</span></span>

<span data-ttu-id="fad01-110">È possibile cancellare un file dagli appunti usando la funzione [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) .</span><span class="sxs-lookup"><span data-stu-id="fad01-110">You can clear a file from the clipboard by using the [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) function.</span></span> <span data-ttu-id="fad01-111">Questa funzione non cancella dagli Appunti altri tipi di informazioni, ad esempio testo.</span><span class="sxs-lookup"><span data-stu-id="fad01-111">This function does not clear other types of information, such as text, from the clipboard.</span></span> <span data-ttu-id="fad01-112">Se si utilizzano le funzioni degli Appunti nell'applicazione, cancellare gli appunti con **AVIClearClipboard** prima di chiudere l'applicazione o chiudere il file negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="fad01-112">If you use clipboard functions in your application, clear the clipboard with **AVIClearClipboard** before closing the application or closing the file on the clipboard.</span></span> <span data-ttu-id="fad01-113">È possibile chiamare **AVIClearClipboard** nell'applicazione indipendentemente dall'uso di **AVIPutFileOnClipboard** .</span><span class="sxs-lookup"><span data-stu-id="fad01-113">You can call **AVIClearClipboard** in your application whether or not **AVIPutFileOnClipboard** has been used.</span></span>

> [!Note]  
> <span data-ttu-id="fad01-114">Se l'applicazione copia un file negli Appunti e il file contiene dati di flusso che potrebbero cambiare, è possibile creare un file di memoria di flussi clonati usando la funzione [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) .</span><span class="sxs-lookup"><span data-stu-id="fad01-114">If your application copies a file to the clipboard and the file contains stream data that might change, you can create a memory file of cloned streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="fad01-115">È quindi possibile inserire il file negli Appunti e quindi rilasciare il file originale senza invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="fad01-115">You can then place the file on the clipboard and then release the original file without invalidating it.</span></span>

 

 

 




