---
description: Visualizza una finestra di dialogo contenente le informazioni sul firmatario per un messaggio firmato.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: Funzione CryptUIDlgViewSignerInfo
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878954"
---
# <a name="cryptuidlgviewsignerinfo-function"></a><span data-ttu-id="395a3-103">Funzione CryptUIDlgViewSignerInfo</span><span class="sxs-lookup"><span data-stu-id="395a3-103">CryptUIDlgViewSignerInfo function</span></span>

<span data-ttu-id="395a3-104">\[La funzione **CryptUIDlgViewSignerInfo** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="395a3-104">\[The **CryptUIDlgViewSignerInfo** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="395a3-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="395a3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="395a3-106">\]</span><span class="sxs-lookup"><span data-stu-id="395a3-106">\]</span></span>

<span data-ttu-id="395a3-107">La funzione **CryptUIDlgViewSignerInfo** Visualizza una finestra di dialogo contenente le informazioni sul firmatario per un messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="395a3-107">The **CryptUIDlgViewSignerInfo** function displays a dialog box that contains the signer information for a signed message.</span></span>

> [!Note]  
> <span data-ttu-id="395a3-108">Questa funzione non è dichiarata in un file di intestazione pubblicato.</span><span class="sxs-lookup"><span data-stu-id="395a3-108">This function is not declared in a published header file.</span></span> <span data-ttu-id="395a3-109">Per usare questa struttura, dichiararla nel formato esatto indicato.</span><span class="sxs-lookup"><span data-stu-id="395a3-109">To use this structure, declare it in the exact format shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="395a3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="395a3-110">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="395a3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="395a3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="395a3-112">*pcvsi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="395a3-112">*pcvsi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="395a3-113">Puntatore a una struttura [**CRYPTUI \_ VIEWSIGNERINFO \_ struct**](cryptui-viewsignerinfo-struct.md) che contiene le informazioni sul firmatario da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="395a3-113">A pointer to a [**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**](cryptui-viewsignerinfo-struct.md) structure that contains the signer information to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="395a3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="395a3-114">Return value</span></span>

<span data-ttu-id="395a3-115">Questa funzione restituisce un valore diverso da zero in caso di esito positivo e zero in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="395a3-115">This function returns a nonzero value on success and zero on failure.</span></span> <span data-ttu-id="395a3-116">Per informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="395a3-116">For extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="395a3-117">I codici di errore possibili restituiti da [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) includono ma non sono limitati a quanto segue.</span><span class="sxs-lookup"><span data-stu-id="395a3-117">Possible error codes returned from [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) include, but are not limited to, the following.</span></span>



| <span data-ttu-id="395a3-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="395a3-118">Return code</span></span>                                                                                   | <span data-ttu-id="395a3-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="395a3-119">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="395a3-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="395a3-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="395a3-121">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="395a3-121">One or more arguments are not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="395a3-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="395a3-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="395a3-123">Si è verificato un errore di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="395a3-123">A memory allocation failure occurred.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="395a3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="395a3-124">Requirements</span></span>



| <span data-ttu-id="395a3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="395a3-125">Requirement</span></span> | <span data-ttu-id="395a3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="395a3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="395a3-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="395a3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="395a3-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="395a3-128">Windows XP \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="395a3-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="395a3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="395a3-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="395a3-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="395a3-131">Fine del supporto</span><span class="sxs-lookup"><span data-stu-id="395a3-131">End of support</span></span><br/> | <span data-ttu-id="395a3-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="395a3-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="395a3-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="395a3-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="395a3-134"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="395a3-134"><dt>Cryptui.lib</dt></span></span> </dl>      |
| <span data-ttu-id="395a3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="395a3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="395a3-136"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="395a3-136"><dt>Cryptui.dll</dt></span></span> </dl>      |
| <span data-ttu-id="395a3-137">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="395a3-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="395a3-138">**CryptUIDlgViewSignerInfoW** (Unicode) e **CryptUIDlgViewSignerInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="395a3-138">**CryptUIDlgViewSignerInfoW** (Unicode) and **CryptUIDlgViewSignerInfoA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="395a3-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="395a3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="395a3-140">**\_struct CRYPTUI VIEWSIGNERINFO \_**</span><span class="sxs-lookup"><span data-stu-id="395a3-140">**CRYPTUI\_VIEWSIGNERINFO\_STRUCT**</span></span>](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
