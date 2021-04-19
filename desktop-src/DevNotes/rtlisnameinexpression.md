---
description: Determina se una stringa Unicode corrisponde al modello specificato.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: RtlIsNameInExpression (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304654"
---
# <a name="rtlisnameinexpression-function"></a><span data-ttu-id="e8ed0-103">RtlIsNameInExpression (funzione)</span><span class="sxs-lookup"><span data-stu-id="e8ed0-103">RtlIsNameInExpression function</span></span>

<span data-ttu-id="e8ed0-104">Determina se una stringa Unicode corrisponde al modello specificato.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-104">Determines whether a Unicode string matches the specified pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ed0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8ed0-105">Syntax</span></span>


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a><span data-ttu-id="e8ed0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8ed0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8ed0-107">*Espressione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8ed0-107">*Expression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ed0-108">Puntatore alla stringa del modello.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-108">A pointer to the pattern string.</span></span> <span data-ttu-id="e8ed0-109">Questa stringa può contenere caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-109">This string can contain wildcard characters.</span></span> <span data-ttu-id="e8ed0-110">Se il parametro *IgnoreCase* è true, la stringa deve contenere solo caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-110">If the *IgnoreCase* parameter is TRUE, the string must contain only uppercase characters.</span></span>

</dd> <dt>

<span data-ttu-id="e8ed0-111">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8ed0-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ed0-112">Puntatore alla stringa da confrontare con il modello.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-112">A pointer to the string to be compared against the pattern.</span></span> <span data-ttu-id="e8ed0-113">Questa stringa non può contenere caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-113">This string cannot contain wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="e8ed0-114">*IgnoreCase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8ed0-114">*IgnoreCase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ed0-115">**True** per la corrispondenza senza distinzione tra maiuscole e minuscole o **false** per corrispondenza con distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="e8ed0-115">**TRUE** for case-insensitive matching, or **FALSE** for case-sensitive matching.</span></span>

</dd> <dt>

<span data-ttu-id="e8ed0-116">*UpcaseTable* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e8ed0-116">*UpcaseTable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ed0-117">Puntatore facoltativo a una tabella caratteri maiuscola da usare per la corrispondenza senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-117">An optional pointer to an uppercase character table to use for case-insensitive matching.</span></span> <span data-ttu-id="e8ed0-118">Se questo parametro è NULL, viene utilizzata la tabella dei caratteri maiuscoli di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-118">If this parameter is NULL, the default system uppercase character table is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8ed0-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8ed0-119">Return value</span></span>

<span data-ttu-id="e8ed0-120">Restituisce **true** se la stringa corrisponde al modello.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-120">Returns **TRUE** if the string matches the pattern.</span></span> <span data-ttu-id="e8ed0-121">Se la stringa non corrisponde al modello, la funzione restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-121">If the string does not match the pattern, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ed0-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8ed0-122">Remarks</span></span>

<span data-ttu-id="e8ed0-123">A questa funzione non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-123">This function has no associated header file.</span></span> <span data-ttu-id="e8ed0-124">La libreria di importazione associata, Ntdll. lib, è disponibile in Microsoft Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="e8ed0-124">The associated import library, Ntdll.lib, is available in the Microsoft Windows Driver Kit (WDK).</span></span> <span data-ttu-id="e8ed0-125">È anche possibile chiamare questa funzione usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="e8ed0-125">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8ed0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8ed0-126">Requirements</span></span>



| <span data-ttu-id="e8ed0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8ed0-127">Requirement</span></span> | <span data-ttu-id="e8ed0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e8ed0-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ed0-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8ed0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ed0-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8ed0-130">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e8ed0-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8ed0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ed0-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8ed0-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e8ed0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e8ed0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8ed0-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8ed0-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
