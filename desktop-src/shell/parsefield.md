---
description: Legge una riga dal file Setup. inf ed estrae il campo specificato dalla stringa.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Funzione ParseField (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232111"
---
# <a name="parsefield-function"></a><span data-ttu-id="91351-103">ParseField (funzione)</span><span class="sxs-lookup"><span data-stu-id="91351-103">ParseField function</span></span>

<span data-ttu-id="91351-104">\[La funzione **ParseField** è attualmente prevista per l'utilizzo nella versione successiva del sistema operativo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="91351-104">\[The **ParseField** function is currently expected to be available for use in the next version of the Microsoft Windows operating system.</span></span> <span data-ttu-id="91351-105">Potrebbe essere modificato o non disponibile nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="91351-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="91351-106">Legge una riga dal file Setup. inf ed estrae il campo specificato dalla stringa.</span><span class="sxs-lookup"><span data-stu-id="91351-106">Reads a line from Setup.inf and extracts the specified field from the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="91351-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91351-107">Syntax</span></span>


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="91351-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="91351-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91351-109">*szData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91351-109">*szData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91351-110">Tipo: \**LPCTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="91351-110">Type: \**LPCTSTR\** _</span></span>

<span data-ttu-id="91351-111">Puntatore alla riga da Setup. inf.</span><span class="sxs-lookup"><span data-stu-id="91351-111">A pointer to the line from Setup.inf.</span></span>

</dd> <dt>

<span data-ttu-id="91351-112">_n \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91351-112">_n\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91351-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="91351-113">Type: **int**</span></span>

<span data-ttu-id="91351-114">**Int** che indica il campo da estrarre.</span><span class="sxs-lookup"><span data-stu-id="91351-114">**INT** that indicates which field to extract.</span></span>

<dt>



 <span data-ttu-id="91351-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="91351-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="91351-116">Indica il campo prima di un segno di uguale (=).</span><span class="sxs-lookup"><span data-stu-id="91351-116">Indicates the field before an equals sign (=).</span></span>

</dd> <dt>



 <span data-ttu-id="91351-117">(1)</span><span class="sxs-lookup"><span data-stu-id="91351-117">(1)</span></span>


</dt> <dd>

<span data-ttu-id="91351-118">Indica il primo campo.</span><span class="sxs-lookup"><span data-stu-id="91351-118">Indicates the first field.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="91351-119">*szBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91351-119">*szBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91351-120">Tipo: \**LPTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="91351-120">Type: \**LPTSTR\** _</span></span>

<span data-ttu-id="91351-121">Puntatore al buffer che riceve il campo Estratto.</span><span class="sxs-lookup"><span data-stu-id="91351-121">A pointer to the buffer that receives the extracted field.</span></span>

</dd> <dt>

<span data-ttu-id="91351-122">_iBufLen \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91351-122">_iBufLen\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91351-123">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="91351-123">Type: **int**</span></span>

<span data-ttu-id="91351-124">**Int** che riceve la dimensione del buffer che riceve il campo Estratto.</span><span class="sxs-lookup"><span data-stu-id="91351-124">**INT** that receives the size of the buffer that receives the extracted field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91351-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91351-125">Return value</span></span>

<span data-ttu-id="91351-126">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="91351-126">Type: **bool**</span></span>

<span data-ttu-id="91351-127">Restituisce **true** se la funzione ha esito positivo e **false** in caso di esito negativo.</span><span class="sxs-lookup"><span data-stu-id="91351-127">Returns **TRUE** if the function is successful and **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="91351-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="91351-128">Remarks</span></span>

<span data-ttu-id="91351-129">I campi nella stringa devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="91351-129">The fields in the string must be separated by commas.</span></span>

<span data-ttu-id="91351-130">Gli spazi iniziali e finali vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="91351-130">Leading and trailing spaces are removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="91351-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91351-131">Requirements</span></span>



| <span data-ttu-id="91351-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="91351-132">Requirement</span></span> | <span data-ttu-id="91351-133">Valore</span><span class="sxs-lookup"><span data-stu-id="91351-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91351-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91351-134">Minimum supported client</span></span><br/> | <span data-ttu-id="91351-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91351-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91351-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91351-136">Minimum supported server</span></span><br/> | <span data-ttu-id="91351-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91351-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="91351-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91351-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="91351-139"><dt>Util. h</dt></span><span class="sxs-lookup"><span data-stu-id="91351-139"><dt>Util.h</dt></span></span> </dl>                             |
| <span data-ttu-id="91351-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="91351-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="91351-141"><dt>Shell32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91351-141"><dt>Shell32.lib</dt></span></span> </dl>                        |
| <span data-ttu-id="91351-142">DLL</span><span class="sxs-lookup"><span data-stu-id="91351-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91351-143"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="91351-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




