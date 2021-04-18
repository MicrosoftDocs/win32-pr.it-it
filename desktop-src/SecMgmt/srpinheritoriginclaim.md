---
description: Questa funzione accetta l'attributo Origin se presente dal token Origin e li imposta su un duplicato del token che eredita e restituisce il token duplicato.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306421"
---
# <a name="srpinheritoriginclaim-function"></a><span data-ttu-id="b3125-103">srpInheritOriginClaim (funzione)</span><span class="sxs-lookup"><span data-stu-id="b3125-103">srpInheritOriginClaim function</span></span>

<span data-ttu-id="b3125-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b3125-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b3125-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b3125-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b3125-106">Questa funzione accetta l'attributo Origin se presente dal token Origin e li imposta su un duplicato del token che eredita e restituisce il token duplicato.</span><span class="sxs-lookup"><span data-stu-id="b3125-106">This function takes the origin attribute if present from the origin token and sets them on a duplicate of the inheriting token, and returns the duplicate token.</span></span> <span data-ttu-id="b3125-107">Il chiamante può quindi rappresentare il token restituito.</span><span class="sxs-lookup"><span data-stu-id="b3125-107">The caller can then impersonate the returned token.</span></span> <span data-ttu-id="b3125-108">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="b3125-108">This function has no associated import library.</span></span> <span data-ttu-id="b3125-109">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a srpapi.dll.</span><span class="sxs-lookup"><span data-stu-id="b3125-109">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to srpapi.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3125-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3125-110">Syntax</span></span>


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a><span data-ttu-id="b3125-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3125-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3125-112">*OriginToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3125-112">*OriginToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3125-113">Handle per il token duplicato e che riceve l'attributo Origin ereditato.</span><span class="sxs-lookup"><span data-stu-id="b3125-113">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="b3125-114">Questo handle deve essere aperto con il \_ diritto di accesso duplicato del token.</span><span class="sxs-lookup"><span data-stu-id="b3125-114">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span>

</dd> <dt>

<span data-ttu-id="b3125-115">*InheritingToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3125-115">*InheritingToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3125-116">Handle per il token duplicato e che riceve l'attributo Origin ereditato.</span><span class="sxs-lookup"><span data-stu-id="b3125-116">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="b3125-117">Questo handle deve essere aperto con il \_ diritto di accesso duplicato del token.</span><span class="sxs-lookup"><span data-stu-id="b3125-117">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span> 

</dd> <dt>

<span data-ttu-id="b3125-118">*ResultToken*</span><span class="sxs-lookup"><span data-stu-id="b3125-118">*ResultToken*</span></span> 
</dt> <dd>

<span data-ttu-id="b3125-119">Se l'operazione riesce, riceve il token duplicato.</span><span class="sxs-lookup"><span data-stu-id="b3125-119">On success, receives the duplicated token.</span></span> <span data-ttu-id="b3125-120">Il chiamante può rappresentarlo per eseguire operazioni con l'attributo Origin ereditato.</span><span class="sxs-lookup"><span data-stu-id="b3125-120">The caller can impersonate it to perform operations with the inherited origin attribute.</span></span> <span data-ttu-id="b3125-121">Il chiamante acquisisce la proprietà di questo handle e deve chiuderlo.</span><span class="sxs-lookup"><span data-stu-id="b3125-121">The caller takes ownership of this handle and must close it.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3125-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3125-122">Return value</span></span>

<span data-ttu-id="b3125-123">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b3125-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3125-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3125-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3125-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3125-125">Requirements</span></span>



| <span data-ttu-id="b3125-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3125-126">Requirement</span></span> | <span data-ttu-id="b3125-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b3125-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3125-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3125-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b3125-129">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b3125-129">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b3125-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3125-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b3125-131">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="b3125-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3125-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b3125-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3125-133"><dt>Srpapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3125-133"><dt>Srpapi.dll</dt></span></span> </dl> |



 

