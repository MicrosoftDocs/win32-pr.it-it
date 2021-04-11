---
description: Questo argomento descrive come compilare un esperto generico fornito con l'SDK Network Monitor.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Creazione di un esperto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227386"
---
# <a name="building-an-expert"></a><span data-ttu-id="3ccf6-103">Creazione di un esperto</span><span class="sxs-lookup"><span data-stu-id="3ccf6-103">Building an Expert</span></span>

<span data-ttu-id="3ccf6-104">Questo argomento descrive come compilare un esperto generico fornito con l'SDK Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-104">This topic describes how to build a generic expert that ships with the Network Monitor SDK.</span></span>

> [!Note]  
> <span data-ttu-id="3ccf6-105">Prima di creare gli esempi di codice seguenti, installare il Network Monitor SDK e inizializzare il file di MySetEnv.bat.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-105">Before creating the following code examples, install the Network Monitor SDK and initialize the MySetEnv.bat file.</span></span>

 

<span data-ttu-id="3ccf6-106">**Per creare un esperto generico**</span><span class="sxs-lookup"><span data-stu-id="3ccf6-106">**To build a generic expert**</span></span>

1.  <span data-ttu-id="3ccf6-107">Aprire un prompt dei comandi di Network Monitor e passare alla \\ sottodirectory Experts, ad esempio C: \\ Program Files \\ NetMonSDK2 \\ Experts.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-107">Open a Network Monitor command prompt and navigate to the \\Experts subdirectory; for example, C:\\Program Files\\NetMonSDK2\\Experts.</span></span>
2.  <span data-ttu-id="3ccf6-108">Digitare **xcopy/e/s/V Blrplate esperto**; quindi, quando richiesto, digitare **D**.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-108">Type **xcopy /e /s /v Blrplate MyExpert**; then, when prompted, type **D**.</span></span>
3.  <span data-ttu-id="3ccf6-109">Passare alla \\ sottodirectory di esperti.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-109">Move to the \\MyExpert subdirectory.</span></span>
4.  <span data-ttu-id="3ccf6-110">Digitare **Ren Blrplate \* . \* Esperto \* . \***.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-110">Type **ren Blrplate\*.\* MyExpert\*.\***.</span></span> <span data-ttu-id="3ccf6-111">Verificare che tutti i file siano stati rinominati correttamente.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-111">Ensure that all files are properly renamed.</span></span> <span data-ttu-id="3ccf6-112">Verificare i nomi dei file confrontando i file nella \\ \\ sottodirectory Experts Blrplate.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-112">Verify the file names by comparing the files in the \\Experts\\Blrplate subdirectory.</span></span>
5.  <span data-ttu-id="3ccf6-113">Modificare il makefile sostituendo tutte le occorrenze di **Blrplate** con l' **esperto**.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-113">Edit the Makefile by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
6.  <span data-ttu-id="3ccf6-114">Modificare entrambi i file con estensione cpp sostituendo tutte le occorrenze di **Blrplate** con l' **esperto**.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-114">Edit both .cpp files by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span> <span data-ttu-id="3ccf6-115">Tenere presente che l'identificatore della finestra di dialogo in config. cpp deve essere in lettere maiuscole (ad esempio, **esperto**).</span><span class="sxs-lookup"><span data-stu-id="3ccf6-115">Be aware that the dialog box identifier in Config.cpp must be capitalized (for example, **MYEXPERT**).</span></span>
7.  <span data-ttu-id="3ccf6-116">Modificare il sottoexpert. h sostituendo tutte le occorrenze di **Blrplate** con l' **esperto**.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-116">Edit MyExpert.h by replacing all occurrences of **Blrplate** with **MyExpert**.</span></span>
8.  <span data-ttu-id="3ccf6-117">Modificare Resrc1. h rinominando **BLRPLATE** in **esperto**.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-117">Edit Resrc1.h by renaming **BLRPLATE** to **MYEXPERT**.</span></span> <span data-ttu-id="3ccf6-118">(Tenere presente che l' **esperto** deve essere in lettere maiuscole).</span><span class="sxs-lookup"><span data-stu-id="3ccf6-118">(Remember, **MYEXPERT** must be capitalized).</span></span>
9.  <span data-ttu-id="3ccf6-119">Modificare il file con estensione RC di esperti rinominando la **finestra di dialogo di configurazione di IDD \_ BLRPLATE \_ \_** nella **finestra di \_ \_ \_ dialogo di configurazione IDD**.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-119">Edit the MyExpert.rc file by renaming **IDD\_BLRPLATE\_CONFIG\_DIALOG** to **IDD\_MYEXPERT\_CONFIG\_DIALOG**.</span></span>
10. <span data-ttu-id="3ccf6-120">Digitare **NMAKE** per compilare il file dll.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-120">Type **nmake** to build the DLL file.</span></span> <span data-ttu-id="3ccf6-121">Per verificare la compilazione, modificare la directory della \\ sottodirectory obj e verificare che il file esista.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-121">To verify the build, change directory to the \\Obj subdirectory and verify that the file exists.</span></span> <span data-ttu-id="3ccf6-122">Per ulteriori informazioni, vedere [visualizzazione delle proprietà](viewing-expert-dll-properties.md)di una DLL di esperti.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-122">For more information, see [Viewing Expert DLL Properties](viewing-expert-dll-properties.md).</span></span>

<span data-ttu-id="3ccf6-123">Al termine della compilazione, sarà presente una DLL di esperti che è possibile testare e distribuire con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="3ccf6-123">When the build is complete, you will have an expert DLL that you can test and deploy with Network Monitor.</span></span> <span data-ttu-id="3ccf6-124">Per ulteriori informazioni sull'installazione di un esperto, vedere [installazione di un esperto in Network Monitor 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="3ccf6-124">For more information about installing an expert, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span> <span data-ttu-id="3ccf6-125">Per ulteriori informazioni sul debug di un esperto, vedere [debug di un esperto](debugging-an-expert.md).</span><span class="sxs-lookup"><span data-stu-id="3ccf6-125">For more information about debugging an expert, see [Debugging an Expert](debugging-an-expert.md).</span></span>

 

 



