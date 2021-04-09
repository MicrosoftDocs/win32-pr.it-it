---
description: Scrive i dati binari dal file specificato nel database specificato.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: SdbWriteBinaryTagFromFile (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966032"
---
# <a name="sdbwritebinarytagfromfile-function"></a><span data-ttu-id="9e89f-103">SdbWriteBinaryTagFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="9e89f-103">SdbWriteBinaryTagFromFile function</span></span>

<span data-ttu-id="9e89f-104">Scrive i dati binari dal file specificato nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="9e89f-104">Writes binary data from the specified file to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e89f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e89f-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a><span data-ttu-id="9e89f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e89f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e89f-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e89f-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e89f-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="9e89f-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="9e89f-109">*tTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e89f-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e89f-110">TAG per la voce.</span><span class="sxs-lookup"><span data-stu-id="9e89f-110">The TAG for the entry.</span></span> <span data-ttu-id="9e89f-111">Questo TAG deve essere di tipo **tag \_ \_ Binary**.</span><span class="sxs-lookup"><span data-stu-id="9e89f-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="9e89f-112">*pwszPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e89f-112">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e89f-113">Percorso del file che contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="9e89f-113">The path to the file that contains the data.</span></span> <span data-ttu-id="9e89f-114">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9e89f-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e89f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e89f-115">Return value</span></span>

<span data-ttu-id="9e89f-116">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="9e89f-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e89f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e89f-117">Requirements</span></span>



| <span data-ttu-id="9e89f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e89f-118">Requirement</span></span> | <span data-ttu-id="9e89f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9e89f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e89f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e89f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e89f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e89f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e89f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e89f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e89f-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e89f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e89f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9e89f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e89f-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e89f-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e89f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e89f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e89f-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="9e89f-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> </dl>

 

 




