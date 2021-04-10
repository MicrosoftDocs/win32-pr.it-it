---
description: Recupera i dati dell'attributo per il file specificato.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125625"
---
# <a name="sdbgetfileattributes-function"></a><span data-ttu-id="5a99e-103">SdbGetFileAttributes (funzione)</span><span class="sxs-lookup"><span data-stu-id="5a99e-103">SdbGetFileAttributes function</span></span>

<span data-ttu-id="5a99e-104">Recupera i dati dell'attributo per il file specificato.</span><span class="sxs-lookup"><span data-stu-id="5a99e-104">Retrieves the attribute data for the specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a99e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a99e-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a><span data-ttu-id="5a99e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a99e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a99e-107">*lpwszFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a99e-107">*lpwszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a99e-108">Percorso del file.</span><span class="sxs-lookup"><span data-stu-id="5a99e-108">The path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="5a99e-109">*ppAttrInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a99e-109">*ppAttrInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a99e-110">Matrice di strutture [**ATTRINFO**](attrinfo.md) che contengono i dati dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="5a99e-110">An array of [**ATTRINFO**](attrinfo.md) structures that contain the attribute data.</span></span>

</dd> <dt>

<span data-ttu-id="5a99e-111">*lpdwAttrCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a99e-111">*lpdwAttrCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a99e-112">Numero di attributi.</span><span class="sxs-lookup"><span data-stu-id="5a99e-112">The number of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a99e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a99e-113">Return value</span></span>

<span data-ttu-id="5a99e-114">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="5a99e-114">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a99e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a99e-115">Remarks</span></span>

<span data-ttu-id="5a99e-116">Una volta completati i dati, è possibile liberarli usando la funzione [**SdbFreeFileAttributes**](sdbfreefileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5a99e-116">When you have finished with the data, free it using the [**SdbFreeFileAttributes**](sdbfreefileattributes.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a99e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a99e-117">Requirements</span></span>



| <span data-ttu-id="5a99e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a99e-118">Requirement</span></span> | <span data-ttu-id="5a99e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5a99e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a99e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a99e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a99e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a99e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5a99e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a99e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a99e-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a99e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5a99e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5a99e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a99e-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a99e-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a99e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a99e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a99e-127">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="5a99e-127">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="5a99e-128">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="5a99e-128">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> </dl>

 

 




