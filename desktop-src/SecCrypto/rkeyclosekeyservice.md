---
description: La funzione RKeyCloseKeyService non è supportata.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Funzione RKeyCloseKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879266"
---
# <a name="rkeyclosekeyservice-function"></a><span data-ttu-id="0169a-103">RKeyCloseKeyService (funzione)</span><span class="sxs-lookup"><span data-stu-id="0169a-103">RKeyCloseKeyService function</span></span>

<span data-ttu-id="0169a-104">La funzione **RKeyCloseKeyService** non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0169a-104">The **RKeyCloseKeyService** function is not supported.</span></span>

<span data-ttu-id="0169a-105">**Windows Server 2003:** La funzione **RKeyCloseKeyService** chiude un handle di servizio chiave aperto da una chiamata precedente alla funzione [**RKeyOpenKeyService**](rkeyopenkeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0169a-105">**Windows Server 2003:** The **RKeyCloseKeyService** function closes a key service handle opened by a previous call to the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) function.</span></span> <span data-ttu-id="0169a-106">Si noti che questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0169a-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="0169a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0169a-107">Syntax</span></span>


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="0169a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0169a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0169a-109">*hKeySvcCli* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0169a-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0169a-110">Handle [**di \_ handle KEYSVCC**](keysvcc-handle.md) precedentemente aperto da [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="0169a-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="0169a-111">Questo valore non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0169a-111">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0169a-112">*mantenuta* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0169a-112">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0169a-113">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0169a-113">Reserved.</span></span> <span data-ttu-id="0169a-114">Impostare questo valore su **null**.</span><span class="sxs-lookup"><span data-stu-id="0169a-114">Set this value to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0169a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0169a-115">Return value</span></span>

<span data-ttu-id="0169a-116">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0169a-116">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="0169a-117">Se la funzione ha esito negativo, il valore restituito è un **ULONG** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="0169a-117">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0169a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0169a-118">Requirements</span></span>



| <span data-ttu-id="0169a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0169a-119">Requirement</span></span> | <span data-ttu-id="0169a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0169a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0169a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0169a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0169a-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0169a-122">None supported</span></span><br/>                                                             |
| <span data-ttu-id="0169a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0169a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0169a-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0169a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0169a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0169a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0169a-126"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="0169a-126"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0169a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0169a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0169a-128">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="0169a-128">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> <dt>

[<span data-ttu-id="0169a-129">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="0169a-129">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




