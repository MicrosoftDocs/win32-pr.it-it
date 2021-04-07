---
description: Conversione manuale da MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversione manuale da MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748298"
---
# <a name="manual-conversion-from-mts"></a><span data-ttu-id="6f2ca-103">Conversione manuale da MTS</span><span class="sxs-lookup"><span data-stu-id="6f2ca-103">Manual Conversion from MTS</span></span>

<span data-ttu-id="6f2ca-104">Potrebbe essere necessario isolare la conversione dei pacchetti MTS in applicazioni COM+ in modo che si trovino all'esterno del processo di installazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="6f2ca-104">You might want to isolate conversion of MTS packages to COM+ applications so that it is outside the Windows setup process.</span></span> <span data-ttu-id="6f2ca-105">La procedura seguente offre un approccio alternativo:</span><span class="sxs-lookup"><span data-stu-id="6f2ca-105">The following procedure offers an alternate approach:</span></span>

1.  <span data-ttu-id="6f2ca-106">Esportare i pacchetti MTS usando la funzionalità di esportazione del pacchetto MTS 2,0, ottenendo un file di pacchetto MTS e una raccolta di altri file.</span><span class="sxs-lookup"><span data-stu-id="6f2ca-106">Export the MTS packages using the MTS 2.0 Package Export feature (resulting in an MTS package file and a collection of other files).</span></span>
2.  <span data-ttu-id="6f2ca-107">Eliminare i pacchetti MTS e aggiornare le finestre oppure eseguire un'installazione pulita di Windows.</span><span class="sxs-lookup"><span data-stu-id="6f2ca-107">Delete the MTS packages and upgrade Windows, or perform a clean installation of Windows.</span></span>
3.  <span data-ttu-id="6f2ca-108">Installare i file del pacchetto MTS (. Pak) in un sistema Windows 2000 o versione successiva utilizzando l'installazione guidata dell'applicazione dello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="6f2ca-108">Install the MTS package (.pak) files on a Windows 2000 or later system by using the Component Services administrative tool's Application Install wizard.</span></span> <span data-ttu-id="6f2ca-109">Sarà inoltre necessario reimpostare l'identità "RunAs" dell'applicazione nel registro di sistema in **HKEY \_ Local \_ Machine \\ software \\ Classes \\ AppID \\ RunAs**.</span><span class="sxs-lookup"><span data-stu-id="6f2ca-109">You will also need to reset the application's "Run As" identity in the system registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\APPID\\RunAs**.</span></span>

> [!Note]  
> <span data-ttu-id="6f2ca-110">Solo la procedura di conversione automatica (tramite l'installazione di Windows o l'esecuzione dell'utilità MTSTOCOM) genera il file di log MTSTOCOM.</span><span class="sxs-lookup"><span data-stu-id="6f2ca-110">Only the automatic conversion procedure (through Windows setup or by running the MTSTOCOM utility) generates the MTSTOCOM log file.</span></span> <span data-ttu-id="6f2ca-111">Questo file non viene generato quando si segue la procedura di conversione manuale.</span><span class="sxs-lookup"><span data-stu-id="6f2ca-111">This file is not generated when following the manual conversion procedure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6f2ca-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f2ca-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f2ca-113">Conversione automatica da MTS</span><span class="sxs-lookup"><span data-stu-id="6f2ca-113">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="6f2ca-114">Risultati e problemi di conversione COM+</span><span class="sxs-lookup"><span data-stu-id="6f2ca-114">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="6f2ca-115">Libreria di amministrazione MTS</span><span class="sxs-lookup"><span data-stu-id="6f2ca-115">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



