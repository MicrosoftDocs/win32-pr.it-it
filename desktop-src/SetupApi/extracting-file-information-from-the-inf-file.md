---
description: Una volta aperto il file INF, è possibile raccogliere informazioni da esso per compilare l'interfaccia utente o per indirizzare il processo di installazione. Le funzioni di installazione forniscono diversi livelli di funzionalità per la raccolta di informazioni da un file INF.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Estrazione di informazioni sui file dal file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879642"
---
# <a name="extracting-file-information-from-the-inf-file"></a><span data-ttu-id="4d367-104">Estrazione di informazioni sui file dal file INF</span><span class="sxs-lookup"><span data-stu-id="4d367-104">Extracting File Information from the INF file</span></span>

<span data-ttu-id="4d367-105">Una volta aperto il file INF, è possibile raccogliere informazioni da esso per compilare l'interfaccia utente o per indirizzare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="4d367-105">After the INF file is opened, you can gather information from it to build the user interface, or to direct the installation process.</span></span> <span data-ttu-id="4d367-106">Le funzioni di installazione forniscono diversi livelli di funzionalità per la raccolta di informazioni da un file INF.</span><span class="sxs-lookup"><span data-stu-id="4d367-106">The setup functions provide several levels of functionality for gathering information from an INF file.</span></span>



| <span data-ttu-id="4d367-107">Per raccogliere informazioni...</span><span class="sxs-lookup"><span data-stu-id="4d367-107">To gather information…</span></span>                | <span data-ttu-id="4d367-108">Usa queste funzioni...</span><span class="sxs-lookup"><span data-stu-id="4d367-108">Use these functions…</span></span>                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="4d367-109">Informazioni sul file INF</span><span class="sxs-lookup"><span data-stu-id="4d367-109">About the INF file</span></span>                    | [<span data-ttu-id="4d367-110">**SetupGetInfInformation**</span><span class="sxs-lookup"><span data-stu-id="4d367-110">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [<span data-ttu-id="4d367-111">**SetupQueryInfFileInformation**</span><span class="sxs-lookup"><span data-stu-id="4d367-111">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | <span data-ttu-id="4d367-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span><span class="sxs-lookup"><span data-stu-id="4d367-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span></span> |
| <span data-ttu-id="4d367-113">Informazioni sui file di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="4d367-113">About source and target files</span></span>         | [<span data-ttu-id="4d367-114">**SetupGetSourceFileLocation**</span><span class="sxs-lookup"><span data-stu-id="4d367-114">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [<span data-ttu-id="4d367-115">**SetupGetSourceFileSize**</span><span class="sxs-lookup"><span data-stu-id="4d367-115">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [<span data-ttu-id="4d367-116">**SetupGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="4d367-116">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [<span data-ttu-id="4d367-117">**SetupGetSourceInfo**</span><span class="sxs-lookup"><span data-stu-id="4d367-117">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| <span data-ttu-id="4d367-118">Da una riga di un file INF</span><span class="sxs-lookup"><span data-stu-id="4d367-118">From a line of an INF file</span></span>            | [<span data-ttu-id="4d367-119">**SetupGetLineText**</span><span class="sxs-lookup"><span data-stu-id="4d367-119">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [<span data-ttu-id="4d367-120">**SetupFindNextLine**</span><span class="sxs-lookup"><span data-stu-id="4d367-120">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [<span data-ttu-id="4d367-121">**SetupFindNextMatchLine**</span><span class="sxs-lookup"><span data-stu-id="4d367-121">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [<span data-ttu-id="4d367-122">**SetupGetLineByIndex**</span><span class="sxs-lookup"><span data-stu-id="4d367-122">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [<span data-ttu-id="4d367-123">**SetupFindFirstLine**</span><span class="sxs-lookup"><span data-stu-id="4d367-123">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| <span data-ttu-id="4d367-124">Da un campo di una riga in un file INF</span><span class="sxs-lookup"><span data-stu-id="4d367-124">From a field of a line in an INF file</span></span> | [<span data-ttu-id="4d367-125">**SetupGetStringField**</span><span class="sxs-lookup"><span data-stu-id="4d367-125">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [<span data-ttu-id="4d367-126">**SetupGetIntField**</span><span class="sxs-lookup"><span data-stu-id="4d367-126">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [<span data-ttu-id="4d367-127">**SetupGetBinaryField**</span><span class="sxs-lookup"><span data-stu-id="4d367-127">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [<span data-ttu-id="4d367-128">**SetupGetMultiSzField**</span><span class="sxs-lookup"><span data-stu-id="4d367-128">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

<span data-ttu-id="4d367-129">Nell'esempio seguente viene usata la funzione [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) per recuperare la descrizione leggibile di un supporto di origine da un file inf.</span><span class="sxs-lookup"><span data-stu-id="4d367-129">The following example uses the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function to retrieve the human-readable description of a source media from an INF file.</span></span>


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



<span data-ttu-id="4d367-130">Nell'esempio, MyInf è l'handle per il file INF aperto.</span><span class="sxs-lookup"><span data-stu-id="4d367-130">In the example, MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="4d367-131">SourceId è l'identificatore per un supporto di origine specifico.</span><span class="sxs-lookup"><span data-stu-id="4d367-131">SourceId is the identifier for a specific source media.</span></span> <span data-ttu-id="4d367-132">Il valore SRCINFO \_ Description specifica che la funzione [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) deve recuperare la descrizione del supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="4d367-132">The value SRCINFO\_DESCRIPTION specifies that the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function should retrieve the source media description.</span></span> <span data-ttu-id="4d367-133">Il buffer punta a una stringa che riceverà la descrizione, MaxBufSize indica le risorse allocate al buffer e BufSize indica le risorse necessarie per archiviare il buffer.</span><span class="sxs-lookup"><span data-stu-id="4d367-133">Buffer points to a string that will receive the description, MaxBufSize indicates the resources allocated to the buffer, and BufSize indicates the resources necessary to store the buffer.</span></span>

<span data-ttu-id="4d367-134">Se BufSize è maggiore di MaxBufSize, la funzione restituirà **false** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà un errore \_ di \_ buffer insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4d367-134">If BufSize is greater than MaxBufSize, the function will return **FALSE**, and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return ERROR\_INSUFFICIENT\_BUFFER.</span></span>

 

 
