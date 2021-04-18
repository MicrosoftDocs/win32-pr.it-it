---
description: Confronta due token di accesso e determina se sono equivalenti rispetto a una chiamata alla funzione AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Funzione NtCompareTokens (Ntseapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310772"
---
# <a name="ntcomparetokens-function"></a><span data-ttu-id="b2c6a-103">NtCompareTokens (funzione)</span><span class="sxs-lookup"><span data-stu-id="b2c6a-103">NtCompareTokens function</span></span>

<span data-ttu-id="b2c6a-104">La funzione **NtCompareTokens** Confronta due [*token di accesso*](/windows/desktop/SecGloss/a-gly) e determina se sono equivalenti rispetto a una chiamata alla funzione [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .</span><span class="sxs-lookup"><span data-stu-id="b2c6a-104">The **NtCompareTokens** function compares two [*access tokens*](/windows/desktop/SecGloss/a-gly) and determines whether they are equivalent with respect to a call to the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c6a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2c6a-105">Syntax</span></span>


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a><span data-ttu-id="b2c6a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2c6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c6a-107">*FirstTokenHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2c6a-107">*FirstTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c6a-108">Handle per il primo token di accesso da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-108">A handle to the first access token to compare.</span></span> <span data-ttu-id="b2c6a-109">Il token deve essere aperto per l'accesso alla **\_ query del token** .</span><span class="sxs-lookup"><span data-stu-id="b2c6a-109">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="b2c6a-110">*SecondTokenHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2c6a-110">*SecondTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c6a-111">Handle per il secondo token di accesso da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-111">A handle to the second access token to compare.</span></span> <span data-ttu-id="b2c6a-112">Il token deve essere aperto per l'accesso alla **\_ query del token** .</span><span class="sxs-lookup"><span data-stu-id="b2c6a-112">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="b2c6a-113">*Uguale* \[ a out\]</span><span class="sxs-lookup"><span data-stu-id="b2c6a-113">*Equal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c6a-114">Puntatore a una variabile che riceve un valore che indica se i token rappresentati dai parametri *FirstTokenHandle* e *SecondTokenHandle* sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-114">A pointer to a variable that receives a value that indicates whether the tokens represented by the *FirstTokenHandle* and *SecondTokenHandle* parameters are equivalent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c6a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2c6a-115">Return value</span></span>

<span data-ttu-id="b2c6a-116">Se la funzione ha esito positivo, la funzione restituisce lo stato \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-116">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="b2c6a-117">Se la funzione ha esito negativo, restituisce un codice di errore **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="b2c6a-117">If the function fails, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2c6a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2c6a-118">Remarks</span></span>

<span data-ttu-id="b2c6a-119">Due token di controllo di accesso sono considerati equivalenti se si verificano tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2c6a-119">Two access control tokens are considered to be equivalent if all of the following conditions are true:</span></span>

-   <span data-ttu-id="b2c6a-120">Ogni [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) presente in uno dei due token è presente anche nell'altro token.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-120">Every [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) that is present in either token is also present in the other token.</span></span>
-   <span data-ttu-id="b2c6a-121">Nessuno o entrambi i token sono limitati.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-121">Neither or both of the tokens are restricted.</span></span>
-   <span data-ttu-id="b2c6a-122">Se entrambi i token sono limitati, anche ogni SID limitato in un token viene limitato nell'altro token.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-122">If both tokens are restricted, every SID that is restricted in one token is also restricted in the other token.</span></span>
-   <span data-ttu-id="b2c6a-123">Ogni privilegio presente in uno dei due token è presente anche nell'altro token.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-123">Every privilege present in either token is also present in the other token.</span></span>

<span data-ttu-id="b2c6a-124">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b2c6a-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c6a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2c6a-125">Requirements</span></span>



| <span data-ttu-id="b2c6a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2c6a-126">Requirement</span></span> | <span data-ttu-id="b2c6a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b2c6a-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c6a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2c6a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c6a-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b2c6a-129">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2c6a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2c6a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c6a-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2c6a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b2c6a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2c6a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2c6a-133"><dt>Ntseapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2c6a-133"><dt>Ntseapi.h</dt></span></span> </dl> |
| <span data-ttu-id="b2c6a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b2c6a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2c6a-135"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2c6a-135"><dt>Ntdll.dll</dt></span></span> </dl> |



 

