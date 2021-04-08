---
title: Proprietà TaskService. HighestVersion
description: Per gli script, indica la versione più recente di Utilità di pianificazione supportata da un computer.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Utilità di pianificazione proprietà HighestVersion
- Utilità di pianificazione proprietà HighestVersion, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, proprietà HighestVersion
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743735"
---
# <a name="taskservicehighestversion-property"></a><span data-ttu-id="928ab-106">Proprietà TaskService. HighestVersion</span><span class="sxs-lookup"><span data-stu-id="928ab-106">TaskService.HighestVersion property</span></span>

<span data-ttu-id="928ab-107">Per gli script, indica la versione più recente di Utilità di pianificazione supportata da un computer.</span><span class="sxs-lookup"><span data-stu-id="928ab-107">For scripting, indicates the highest version of Task Scheduler that a computer supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="928ab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="928ab-108">Syntax</span></span>


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a><span data-ttu-id="928ab-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="928ab-109">Property value</span></span>

<span data-ttu-id="928ab-110">La versione più recente di Utilità di pianificazione supportata da un computer.</span><span class="sxs-lookup"><span data-stu-id="928ab-110">The highest version of Task Scheduler that a computer supports.</span></span> <span data-ttu-id="928ab-111">La versione più recente è un valore suddiviso in MajorVersion/MinorVersion sul limite a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="928ab-111">The highest version is a value that is split into MajorVersion/MinorVersion on the 16-bit boundary.</span></span> <span data-ttu-id="928ab-112">Il servizio Utilità di pianificazione restituisce 1 per la versione principale e 2 per la versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="928ab-112">The Task Scheduler service returns 1 for the major version and 2 for the minor version.</span></span> <span data-ttu-id="928ab-113">Usare la funzione [CLng](/previous-versions//ck4c5842(v=vs.85)) per ottenere il valore intero della proprietà.</span><span class="sxs-lookup"><span data-stu-id="928ab-113">Use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the integer value of the property.</span></span>

## <a name="examples"></a><span data-ttu-id="928ab-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="928ab-114">Examples</span></span>

<span data-ttu-id="928ab-115">Nel codice seguente viene illustrato come utilizzare la funzione [CLng](/previous-versions//ck4c5842(v=vs.85)) per ottenere il valore della proprietà **HighestVersion** .</span><span class="sxs-lookup"><span data-stu-id="928ab-115">The following code shows how to use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the value of the **HighestVersion** property.</span></span>


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a><span data-ttu-id="928ab-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="928ab-116">Requirements</span></span>



| <span data-ttu-id="928ab-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="928ab-117">Requirement</span></span> | <span data-ttu-id="928ab-118">Valore</span><span class="sxs-lookup"><span data-stu-id="928ab-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="928ab-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="928ab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="928ab-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="928ab-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="928ab-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="928ab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="928ab-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="928ab-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="928ab-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="928ab-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="928ab-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="928ab-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="928ab-125">DLL</span><span class="sxs-lookup"><span data-stu-id="928ab-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="928ab-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="928ab-126"><dt>Taskschd.dll</dt></span></span> </dl> |



 

