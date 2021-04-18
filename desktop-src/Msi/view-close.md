---
description: Il metodo Close dell'oggetto View termina l'esecuzione della query e rilascia le risorse di database.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328754"
---
# <a name="viewclose-method"></a><span data-ttu-id="0c657-103">View. Close (metodo)</span><span class="sxs-lookup"><span data-stu-id="0c657-103">View.Close method</span></span>

<span data-ttu-id="0c657-104">Il metodo **Close** dell'oggetto [**View**](view-object.md) termina l'esecuzione della query e rilascia le risorse di database.</span><span class="sxs-lookup"><span data-stu-id="0c657-104">The **Close** method of the [**View**](view-object.md) object terminates query execution and releases database resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c657-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c657-105">Syntax</span></span>


```JScript
View.Close()
```



## <a name="parameters"></a><span data-ttu-id="0c657-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c657-106">Parameters</span></span>

<span data-ttu-id="0c657-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0c657-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c657-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c657-108">Return value</span></span>

<span data-ttu-id="0c657-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0c657-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c657-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c657-110">Remarks</span></span>

<span data-ttu-id="0c657-111">Questo metodo deve essere chiamato prima che il metodo [**Execute**](view-execute.md) venga chiamato nuovamente sull'oggetto [**View**](view-object.md) , a meno che tutte le righe del set di risultati non siano state ottenute con il metodo [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="0c657-111">This method must be called before the [**Execute**](view-execute.md) method is called again on the [**View**](view-object.md) object unless all rows of the result set have been obtained with the [**Fetch**](view-fetch.md) method.</span></span> <span data-ttu-id="0c657-112">Viene chiamato internamente quando la vista viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="0c657-112">It is called internally when the view is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c657-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c657-113">Requirements</span></span>



| <span data-ttu-id="0c657-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c657-114">Requirement</span></span> | <span data-ttu-id="0c657-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0c657-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c657-116">Versione</span><span class="sxs-lookup"><span data-stu-id="0c657-116">Version</span></span><br/> | <span data-ttu-id="0c657-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c657-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0c657-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0c657-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0c657-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c657-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0c657-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0c657-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c657-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c657-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0c657-122">IID</span><span class="sxs-lookup"><span data-stu-id="0c657-122">IID</span></span><br/>     | <span data-ttu-id="0c657-123">IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0c657-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




