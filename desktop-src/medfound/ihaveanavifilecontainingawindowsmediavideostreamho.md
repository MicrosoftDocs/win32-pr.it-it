---
description: Ho un file AVI contenente un flusso di Windows Media Video.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Ho un file AVI contenente un flusso di Windows Media Video. Come è possibile convertirlo in un file WMV?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320461"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a><span data-ttu-id="dd888-104">Ho un file AVI contenente un flusso di Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="dd888-104">I have an AVI file containing a Windows Media Video stream.</span></span> <span data-ttu-id="dd888-105">Come è possibile convertirlo in un file WMV?</span><span class="sxs-lookup"><span data-stu-id="dd888-105">How can I convert it to a WMV file?</span></span>

<span data-ttu-id="dd888-106">Le interfacce Windows Media Audio e codec video non forniscono metodi per creare file usando il formato ASF (Advanced Systems Format), che è il formato usato per i file WMV.</span><span class="sxs-lookup"><span data-stu-id="dd888-106">The Windows Media Audio and Video codec interfaces do not provide methods to create files using the Advanced Systems Format (ASF), which is the format used for WMV files.</span></span> <span data-ttu-id="dd888-107">Se si desidera convertire un file (utilizzando qualsiasi contenitore) in un file ASF, è necessario utilizzare gli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="dd888-107">If you want to convert a file (using any container) to an ASF file, you must use the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="dd888-108">Recuperare gli esempi di Windows Media compressi dal file di origine e passarli all'oggetto writer come esempi di flusso.</span><span class="sxs-lookup"><span data-stu-id="dd888-108">Retrieve the compressed Windows Media samples from the source file and pass them to the writer object as stream samples.</span></span> <span data-ttu-id="dd888-109">Per ulteriori informazioni, vedere la documentazione di Windows Media Format 9 Series SDK.</span><span class="sxs-lookup"><span data-stu-id="dd888-109">For more information, see the Windows Media Format 9 Series SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd888-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd888-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd888-111">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="dd888-111">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



