---
description: Scrive dati binari nel database specificato.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: SdbWriteBinaryTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523322"
---
# <a name="sdbwritebinarytag-function"></a><span data-ttu-id="25fdf-103">SdbWriteBinaryTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="25fdf-103">SdbWriteBinaryTag function</span></span>

<span data-ttu-id="25fdf-104">Scrive dati binari nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="25fdf-104">Writes binary data to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fdf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25fdf-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a><span data-ttu-id="25fdf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25fdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25fdf-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25fdf-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fdf-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="25fdf-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="25fdf-109">*tTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25fdf-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fdf-110">TAG per la voce.</span><span class="sxs-lookup"><span data-stu-id="25fdf-110">The TAG for the entry.</span></span> <span data-ttu-id="25fdf-111">Questo TAG deve essere di tipo **tag \_ \_ Binary**.</span><span class="sxs-lookup"><span data-stu-id="25fdf-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="25fdf-112">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25fdf-112">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fdf-113">Buffer che contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="25fdf-113">The buffer that contains the data.</span></span> <span data-ttu-id="25fdf-114">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="25fdf-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25fdf-115">*dwSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25fdf-115">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fdf-116">Dimensioni in byte del buffer *pbuffer* .</span><span class="sxs-lookup"><span data-stu-id="25fdf-116">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25fdf-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25fdf-117">Return value</span></span>

<span data-ttu-id="25fdf-118">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="25fdf-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="25fdf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25fdf-119">Requirements</span></span>



| <span data-ttu-id="25fdf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="25fdf-120">Requirement</span></span> | <span data-ttu-id="25fdf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="25fdf-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25fdf-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25fdf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="25fdf-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25fdf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="25fdf-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25fdf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="25fdf-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25fdf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="25fdf-126">DLL</span><span class="sxs-lookup"><span data-stu-id="25fdf-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25fdf-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25fdf-127"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25fdf-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25fdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fdf-129">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="25fdf-129">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
</dt> <dt>

[<span data-ttu-id="25fdf-130">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="25fdf-130">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="25fdf-131">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="25fdf-131">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="25fdf-132">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="25fdf-132">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="25fdf-133">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="25fdf-133">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




