---
description: Utilizzare la procedura seguente per eseguire il debug di esperti scritti in Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Debug di un esperto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314177"
---
# <a name="debugging-an-expert"></a><span data-ttu-id="9853a-103">Debug di un esperto</span><span class="sxs-lookup"><span data-stu-id="9853a-103">Debugging an Expert</span></span>

<span data-ttu-id="9853a-104">Utilizzare la procedura seguente per eseguire il debug di esperti scritti in Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9853a-104">Use the following procedure to debug experts written in Microsoft Visual C++.</span></span>

<span data-ttu-id="9853a-105">**Debug di un esperto**</span><span class="sxs-lookup"><span data-stu-id="9853a-105">**Debugging an Expert**</span></span>

1.  <span data-ttu-id="9853a-106">Installare l'esperto (file DLL) e il file di database di programma (con estensione pdb) generato durante la compilazione dell'esperto nella posizione corretta.</span><span class="sxs-lookup"><span data-stu-id="9853a-106">Install the expert (DLL file) and the program database file (.pdb) generated when you compiled the expert in the correct location.</span></span> <span data-ttu-id="9853a-107">Per ulteriori informazioni, vedere [installazione di un esperto in Network Monitor 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="9853a-107">For further details, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="9853a-108">Avviare Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9853a-108">Start Microsoft Visual C++.</span></span>
3.  <span data-ttu-id="9853a-109">Scegliere **Apri** dal menu **file** e selezionare il nome della DLL di esperti.</span><span class="sxs-lookup"><span data-stu-id="9853a-109">From the **File** menu, click **Open** and select the name of your expert DLL.</span></span>
4.  <span data-ttu-id="9853a-110">Al termine del caricamento di Microsoft Visual C++, fare clic sul menu **progetto** , quindi su **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="9853a-110">After Microsoft Visual C++ loads, click the **Project** menu and then click **Settings**.</span></span>
5.  <span data-ttu-id="9853a-111">Fare clic su **debug**.</span><span class="sxs-lookup"><span data-stu-id="9853a-111">Click **Debug**.</span></span> <span data-ttu-id="9853a-112">In **eseguibile per sessione di debug** Digitare il percorso completo di Netmon.exe, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9853a-112">Under **Executable for debug session**, type the full path of Netmon.exe, for example:</span></span>

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  <span data-ttu-id="9853a-113">Impostare i punti di interruzione nel codice.</span><span class="sxs-lookup"><span data-stu-id="9853a-113">Set the breakpoints in your code.</span></span>

 

 



