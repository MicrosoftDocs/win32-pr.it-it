---
description: L'API shell fornisce funzioni che è possibile usare per gestire le stampanti di rete. Se a un file è associato il verbo di stampa, è possibile usare il comando ShellExecuteEx per stamparlo.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Gestione delle stampanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979954"
---
# <a name="managing-printers"></a><span data-ttu-id="21591-104">Gestione delle stampanti</span><span class="sxs-lookup"><span data-stu-id="21591-104">Managing Printers</span></span>

<span data-ttu-id="21591-105">L'API shell fornisce funzioni che è possibile usare per gestire le stampanti di rete.</span><span class="sxs-lookup"><span data-stu-id="21591-105">The Shell API provides functions that you can use to manage networked printers.</span></span> <span data-ttu-id="21591-106">Se a un file è associato il verbo di **stampa** , è possibile usare il comando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per stamparlo.</span><span class="sxs-lookup"><span data-stu-id="21591-106">If a file has the **print** verb associated with it, you can use the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) command to print it.</span></span>

-   [<span data-ttu-id="21591-107">Gestione stampanti</span><span class="sxs-lookup"><span data-stu-id="21591-107">Printer Management</span></span>](#printer-management)
-   [<span data-ttu-id="21591-108">Stampa di file con ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="21591-108">Printing Files with ShellExecuteEx</span></span>](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a><span data-ttu-id="21591-109">Gestione stampanti</span><span class="sxs-lookup"><span data-stu-id="21591-109">Printer Management</span></span>

<span data-ttu-id="21591-110">È possibile gestire le stampanti in un sistema con la funzione [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) .</span><span class="sxs-lookup"><span data-stu-id="21591-110">You can manage printers on a system with the [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) function.</span></span> <span data-ttu-id="21591-111">Questa funzione consente di:</span><span class="sxs-lookup"><span data-stu-id="21591-111">This function allows you to:</span></span>

-   <span data-ttu-id="21591-112">Installare le stampanti.</span><span class="sxs-lookup"><span data-stu-id="21591-112">Install printers.</span></span>
-   <span data-ttu-id="21591-113">Aprire stampanti.</span><span class="sxs-lookup"><span data-stu-id="21591-113">Open printers.</span></span>
-   <span data-ttu-id="21591-114">Ottenere le proprietà della stampante.</span><span class="sxs-lookup"><span data-stu-id="21591-114">Get printer properties.</span></span>
-   <span data-ttu-id="21591-115">Creare collegamenti alla stampante.</span><span class="sxs-lookup"><span data-stu-id="21591-115">Create printer links.</span></span>
-   <span data-ttu-id="21591-116">Stampare una pagina di prova.</span><span class="sxs-lookup"><span data-stu-id="21591-116">Print a test page.</span></span>

## <a name="printing-files-with-shellexecuteex"></a><span data-ttu-id="21591-117">Stampa di file con ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="21591-117">Printing Files with ShellExecuteEx</span></span>

<span data-ttu-id="21591-118">Se a un tipo di file è associato un comando stampa, è possibile stampare il file chiamando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con **Print** come verbo.</span><span class="sxs-lookup"><span data-stu-id="21591-118">If a file type has a print command associated with it, you can print the file by calling [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) with **print** as the verb.</span></span> <span data-ttu-id="21591-119">Questo comando è spesso identico a quello usato per il verbo **aperto** , con l'aggiunta di un flag per indicare all'applicazione di stampare il file.</span><span class="sxs-lookup"><span data-stu-id="21591-119">This command is often the same as that used for the **open** verb, with the addition of a flag to tell the application to print the file.</span></span> <span data-ttu-id="21591-120">Ad esempio, i file con estensione txt possono essere stampati da Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="21591-120">For instance, .txt files can be printed by Microsoft WordPad.</span></span> <span data-ttu-id="21591-121">Il verbo **Open** per un file con estensione txt corrisponderebbe quindi a un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="21591-121">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



<span data-ttu-id="21591-122">Quando si usa [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per stampare un file con estensione txt, WordPad apre il file, lo stampa e quindi lo chiude, restituendo il controllo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21591-122">When you use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to print a .txt file, WordPad opens the file, prints it, and then closes, returning control to the application.</span></span> <span data-ttu-id="21591-123">La funzione di esempio seguente accetta un percorso completo e USA **ShellExecuteEx** per stamparlo, usando il comando Print associato all'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="21591-123">The following sample function takes a fully qualified path, and uses **ShellExecuteEx** to print it, using the print command associated with its file name extension.</span></span>


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



