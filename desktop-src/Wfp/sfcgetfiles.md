---
description: Elenca i file protetti.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Funzione SfcGetFiles (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882621"
---
# <a name="sfcgetfiles-function"></a><span data-ttu-id="ae9f1-103">SfcGetFiles (funzione)</span><span class="sxs-lookup"><span data-stu-id="ae9f1-103">SfcGetFiles function</span></span>

<span data-ttu-id="ae9f1-104">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-104">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ae9f1-105">Il supporto per questa funzione è stato rimosso in Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-105">Support for this function was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="ae9f1-106">Usare invece le funzioni supportate elencate in [WRP Functions](wfp-functions.md) .\]</span><span class="sxs-lookup"><span data-stu-id="ae9f1-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="ae9f1-107">Elenca i file protetti.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-107">Lists protected files.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae9f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae9f1-108">Syntax</span></span>


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a><span data-ttu-id="ae9f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae9f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae9f1-110">*ProtFileData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae9f1-110">*ProtFileData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f1-111">Puntatore a una struttura [**di \_ \_ voce di file PPROTECT**](pprotect-file-entry.md) che contiene l'elenco dei file protetti.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-111">A pointer to a [**PPROTECT\_FILE\_ENTRY**](pprotect-file-entry.md) structure that contains the protected files list.</span></span>

</dd> <dt>

<span data-ttu-id="ae9f1-112">*FileCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae9f1-112">*FileCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f1-113">Puntatore a una posizione contenente un valore ULONG che rappresenta il numero di file protetti.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-113">A pointer to a location containing a ULONG value that is the number of protected files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae9f1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae9f1-114">Return value</span></span>

<span data-ttu-id="ae9f1-115">Se la funzione ha esito positivo, il valore restituito è STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-115">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span> <span data-ttu-id="ae9f1-116">Se la funzione ha esito negativo, viene restituito il codice di errore NTSTATUS appropriato.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-116">If the function fails, it returns the appropriate NTSTATUS error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae9f1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae9f1-117">Requirements</span></span>



| <span data-ttu-id="ae9f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae9f1-118">Requirement</span></span> | <span data-ttu-id="ae9f1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9f1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9f1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae9f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9f1-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ae9f1-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ae9f1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae9f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9f1-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae9f1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae9f1-124">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ae9f1-124">End of client support</span></span><br/>    | <span data-ttu-id="ae9f1-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ae9f1-125">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ae9f1-126">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ae9f1-126">End of server support</span></span><br/>    | <span data-ttu-id="ae9f1-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ae9f1-127">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ae9f1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae9f1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae9f1-129"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae9f1-129"><dt>Sfcfiles.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae9f1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ae9f1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae9f1-131"><dt>Sfcfiles.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae9f1-131"><dt>Sfcfiles.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae9f1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae9f1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9f1-133">**\_voce di file PPROTECT \_**</span><span class="sxs-lookup"><span data-stu-id="ae9f1-133">**PPROTECT\_FILE\_ENTRY**</span></span>](pprotect-file-entry.md)
</dt> </dl>

 

 




