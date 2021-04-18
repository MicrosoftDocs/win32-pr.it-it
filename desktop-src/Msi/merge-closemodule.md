---
description: Il metodo CloseModule dell'oggetto merge chiude il modulo Windows Installer Merge attualmente aperto.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Metodo merge. CloseModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323986"
---
# <a name="mergeclosemodule-method"></a><span data-ttu-id="793fa-103">Merge. CloseModule, metodo</span><span class="sxs-lookup"><span data-stu-id="793fa-103">Merge.CloseModule method</span></span>

<span data-ttu-id="793fa-104">Il metodo **CloseModule** dell'oggetto [**merge**](merge-object.md) chiude il modulo Windows Installer Merge attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="793fa-104">The **CloseModule** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer merge module.</span></span>

## <a name="syntax"></a><span data-ttu-id="793fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="793fa-105">Syntax</span></span>


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a><span data-ttu-id="793fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="793fa-106">Parameters</span></span>

<span data-ttu-id="793fa-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="793fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="793fa-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="793fa-108">Return value</span></span>

<span data-ttu-id="793fa-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="793fa-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="793fa-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="793fa-110">Remarks</span></span>

<span data-ttu-id="793fa-111">La chiusura di un modulo merge non influirà sugli errori che non sono stati recuperati.</span><span class="sxs-lookup"><span data-stu-id="793fa-111">Closing a merge module will not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="793fa-112">C++</span><span class="sxs-lookup"><span data-stu-id="793fa-112">C++</span></span>

<span data-ttu-id="793fa-113">Vedere funzione [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .</span><span class="sxs-lookup"><span data-stu-id="793fa-113">See [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="793fa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="793fa-114">Requirements</span></span>



| <span data-ttu-id="793fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="793fa-115">Requirement</span></span> | <span data-ttu-id="793fa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="793fa-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="793fa-117">Versione</span><span class="sxs-lookup"><span data-stu-id="793fa-117">Version</span></span><br/> | <span data-ttu-id="793fa-118">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="793fa-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="793fa-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="793fa-119">Header</span></span><br/>  | <dl> <span data-ttu-id="793fa-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="793fa-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="793fa-121">DLL</span><span class="sxs-lookup"><span data-stu-id="793fa-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="793fa-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="793fa-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
