---
description: Converte i dati dell'attributo specificato in formato XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: SdbFormatAttribute (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877129"
---
# <a name="sdbformatattribute-function"></a><span data-ttu-id="ad847-103">SdbFormatAttribute (funzione)</span><span class="sxs-lookup"><span data-stu-id="ad847-103">SdbFormatAttribute function</span></span>

<span data-ttu-id="ad847-104">Converte i dati dell'attributo specificato in formato XML.</span><span class="sxs-lookup"><span data-stu-id="ad847-104">Converts the specified attribute data to XML format.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad847-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad847-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="ad847-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad847-107">*pAttrInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad847-107">*pAttrInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad847-108">Struttura [**ATTRINFO**](attrinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ad847-108">An [**ATTRINFO**](attrinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ad847-109">*pchBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ad847-109">*pchBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad847-110">Buffer di output.</span><span class="sxs-lookup"><span data-stu-id="ad847-110">The output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ad847-111">*dwBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad847-111">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad847-112">Dimensioni del buffer *pchBuffer* , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="ad847-112">The size of the *pchBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad847-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad847-113">Return value</span></span>

<span data-ttu-id="ad847-114">La funzione restituisce **true** in caso di esito positivo o **false** se il buffer è troppo piccolo o l'attributo non viene trovato.</span><span class="sxs-lookup"><span data-stu-id="ad847-114">The function returns **TRUE** on success or **FALSE** if the buffer is too small or the attribute is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad847-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad847-115">Requirements</span></span>



| <span data-ttu-id="ad847-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad847-116">Requirement</span></span> | <span data-ttu-id="ad847-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ad847-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad847-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad847-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ad847-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad847-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ad847-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad847-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ad847-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ad847-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ad847-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ad847-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad847-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad847-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad847-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad847-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad847-125">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="ad847-125">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




