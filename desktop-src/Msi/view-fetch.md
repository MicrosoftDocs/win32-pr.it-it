---
description: Il metodo fetch dell'oggetto View recupera la riga successiva di dati della colonna se nel set di risultati sono disponibili più righe. in caso contrario, è null. Chiamare il metodo Execute prima del metodo fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. fetch (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324766"
---
# <a name="viewfetch-method"></a><span data-ttu-id="7bc32-104">View. fetch (metodo)</span><span class="sxs-lookup"><span data-stu-id="7bc32-104">View.Fetch method</span></span>

<span data-ttu-id="7bc32-105">Il metodo **Fetch** dell'oggetto [**View**](view-object.md) recupera la riga successiva di dati della colonna se nel set di risultati sono disponibili più righe. in caso contrario, è null.</span><span class="sxs-lookup"><span data-stu-id="7bc32-105">The **Fetch** method of the [**View**](view-object.md) object retrieves the next row of column data if more rows are available in the result set, otherwise it is Null.</span></span> <span data-ttu-id="7bc32-106">Chiamare il metodo [**Execute**](view-execute.md) prima del metodo **Fetch** .</span><span class="sxs-lookup"><span data-stu-id="7bc32-106">Call the [**Execute**](view-execute.md) method before the **Fetch** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc32-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bc32-107">Syntax</span></span>


```JScript
View.Fetch()
```



## <a name="parameters"></a><span data-ttu-id="7bc32-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bc32-108">Parameters</span></span>

<span data-ttu-id="7bc32-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7bc32-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bc32-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bc32-110">Return value</span></span>

<span data-ttu-id="7bc32-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7bc32-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bc32-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bc32-112">Remarks</span></span>

<span data-ttu-id="7bc32-113">È necessario utilizzare lo stesso oggetto [**record**](record-object.md) per recuperare i dati in più righe. in caso contrario, l'oggetto deve essere rilasciato uscendo dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="7bc32-113">The same [**Record**](record-object.md) object should be used to retrieve the data in multiple rows, or else the object should be released by going out of scope.</span></span> <span data-ttu-id="7bc32-114">Il record può essere testato per la fine del set di risultati utilizzando la sintassi "If FetchRecord is Nothing".</span><span class="sxs-lookup"><span data-stu-id="7bc32-114">The record can be tested for the end of the result set using the syntax "If FetchRecord Is Nothing".</span></span>

## <a name="requirements"></a><span data-ttu-id="7bc32-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bc32-115">Requirements</span></span>



| <span data-ttu-id="7bc32-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bc32-116">Requirement</span></span> | <span data-ttu-id="7bc32-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7bc32-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc32-118">Versione</span><span class="sxs-lookup"><span data-stu-id="7bc32-118">Version</span></span><br/> | <span data-ttu-id="7bc32-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7bc32-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7bc32-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7bc32-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7bc32-121">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="7bc32-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7bc32-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7bc32-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7bc32-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bc32-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7bc32-124">IID</span><span class="sxs-lookup"><span data-stu-id="7bc32-124">IID</span></span><br/>     | <span data-ttu-id="7bc32-125">IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7bc32-125">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




