---
description: La funzione GetPropertyInfo restituisce un puntatore alle informazioni sulle proprietà di un protocollo specificato.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: Funzione GetPropertyInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878650"
---
# <a name="getpropertyinfo-function"></a><span data-ttu-id="cf448-103">Funzione GetPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="cf448-103">GetPropertyInfo function</span></span>

<span data-ttu-id="cf448-104">La funzione **GetPropertyInfo** restituisce un puntatore alle informazioni sulle proprietà di un protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="cf448-104">The **GetPropertyInfo** function returns a pointer to the property information of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf448-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf448-105">Syntax</span></span>


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="cf448-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf448-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf448-107">*hProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf448-107">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf448-108">Handle per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="cf448-108">Handle to a property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf448-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf448-109">Return value</span></span>

<span data-ttu-id="cf448-110">Se la funzione ha esito positivo, il valore restituito è un puntatore alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="cf448-110">If the function is successful, the return value is a pointer to the property.</span></span>

<span data-ttu-id="cf448-111">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="cf448-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf448-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf448-112">Remarks</span></span>

<span data-ttu-id="cf448-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetPropertyInfo** .</span><span class="sxs-lookup"><span data-stu-id="cf448-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf448-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf448-114">Requirements</span></span>



| <span data-ttu-id="cf448-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf448-115">Requirement</span></span> | <span data-ttu-id="cf448-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cf448-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf448-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf448-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cf448-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf448-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cf448-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf448-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cf448-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cf448-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cf448-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf448-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf448-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf448-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cf448-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="cf448-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf448-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf448-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf448-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cf448-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf448-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf448-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




