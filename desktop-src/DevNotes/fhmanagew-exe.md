---
description: Il programma FhManagew.exe Elimina le versioni dei file che superano la validità specificata dal dispositivo di destinazione della cronologia file attualmente assegnato.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483244"
---
# <a name="fhmanagewexe"></a><span data-ttu-id="4de7a-103">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="4de7a-103">FhManagew.exe</span></span>

<span data-ttu-id="4de7a-104">Il programma FhManagew.exe Elimina le versioni dei file che superano la validità specificata dal dispositivo di destinazione della cronologia file attualmente assegnato.</span><span class="sxs-lookup"><span data-stu-id="4de7a-104">The FhManagew.exe program deletes file versions that exceed a specified age from the currently assigned File History target device.</span></span>

<span data-ttu-id="4de7a-105">Questo programma è disponibile in Windows 8 e Windows Server 2012 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4de7a-105">This program is available in Windows 8 and Windows Server 2012 and later.</span></span>

<span data-ttu-id="4de7a-106">Per eseguire questo programma, andare al menu **Start** , fare clic su **Esegui** e digitare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="4de7a-106">To execute this program, go to the **Start** menu, click **Run**, and type the following command.</span></span>

<span data-ttu-id="4de7a-107">*Tempo* **di puliziaFhManagew.exe**</span><span class="sxs-lookup"><span data-stu-id="4de7a-107">**FhManagew.exe -cleanup** *age*</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4de7a-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="4de7a-108">Parameter</span></span></th>
<th><span data-ttu-id="4de7a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4de7a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4de7a-110"><span id="age"></span><span id="AGE"></span><em>età</em></span><span class="sxs-lookup"><span data-stu-id="4de7a-110"><span id="age"></span><span id="AGE"></span><em>age</em></span></span><br/></td>
<td><span data-ttu-id="4de7a-111">Questo parametro specifica la durata minima, in giorni, delle versioni dei file che possono essere eliminate.</span><span class="sxs-lookup"><span data-stu-id="4de7a-111">This parameter specifies the minimum age, in days, of file versions that can be deleted.</span></span> <span data-ttu-id="4de7a-112">Una versione del file viene eliminata se si verificano entrambe le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4de7a-112">A file version is deleted if both of the following conditions are true:</span></span><br/>
<ul>
<li><span data-ttu-id="4de7a-113">La versione del file è precedente alla data di validità specificata.</span><span class="sxs-lookup"><span data-stu-id="4de7a-113">The file version is older than the specified age.</span></span></li>
<li><span data-ttu-id="4de7a-114">Il file non è più incluso nell'ambito di protezione oppure è presente una versione più recente dello stesso file nel dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4de7a-114">The file is no longer included in the protection scope, or there is a newer version of the same file on the target device.</span></span></li>
</ul>
<span data-ttu-id="4de7a-115">Se il parametro <em>Age</em> è impostato su zero, tutte le versioni dei file vengono eliminate, ad eccezione della versione più recente di ogni file attualmente presente nell'ambito di protezione.</span><span class="sxs-lookup"><span data-stu-id="4de7a-115">If the <em>age</em> parameter is set to zero, all file versions are deleted, except for the newest version of each file that is currently present in the protection scope.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4de7a-116">Per disattivare tutti gli output di questo programma, usare l'opzione della riga di comando **-quiet** come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4de7a-116">To suppress all output from this program, use the **-quiet** command-line option as follows.</span></span>

<span data-ttu-id="4de7a-117">**FhManagew.exe-pulizia** *età* **-non interattiva**</span><span class="sxs-lookup"><span data-stu-id="4de7a-117">**FhManagew.exe -cleanup** *age* **-quiet**</span></span>

## <a name="examples"></a><span data-ttu-id="4de7a-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="4de7a-118">Examples</span></span>



| <span data-ttu-id="4de7a-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="4de7a-119">Example</span></span>                                                                                                                                                                                                      | <span data-ttu-id="4de7a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4de7a-120">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4de7a-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**PuliziaFhManagew.exe 30**</span><span class="sxs-lookup"><span data-stu-id="4de7a-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**</span></span><br/>                                 | <span data-ttu-id="4de7a-122">Elimina tutte le versioni di file che hanno più di un mese.</span><span class="sxs-lookup"><span data-stu-id="4de7a-122">Delete all file versions that are older than one month.</span></span><br/>                        |
| <span data-ttu-id="4de7a-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-Cleanup 365-quiet**</span><span class="sxs-lookup"><span data-stu-id="4de7a-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**</span></span><br/> | <span data-ttu-id="4de7a-124">Eliminare tutte le versioni dei file precedenti a un anno ed eliminare tutti gli output.</span><span class="sxs-lookup"><span data-stu-id="4de7a-124">Delete all file versions that are older than one year and suppress all output.</span></span><br/> |



 

 

 




