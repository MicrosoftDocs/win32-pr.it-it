---
title: Funzione WsDumpMemory (WebServicesDebug. h)
description: Questa funzione consente di eseguire il dump di tutte le allocazioni di memoria alla console.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Servizi Web per la funzione WsDumpMemory per Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964694"
---
# <a name="wsdumpmemory-function"></a><span data-ttu-id="915b9-104">WsDumpMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="915b9-104">WsDumpMemory function</span></span>

<span data-ttu-id="915b9-105">Questa funzione consente di eseguire il dump di tutte le allocazioni di memoria alla console.</span><span class="sxs-lookup"><span data-stu-id="915b9-105">This function dumps all memory allocations to the console.</span></span>

> [!Note]  
> <span data-ttu-id="915b9-106">Questa funzione è solo per il DEBUG.</span><span class="sxs-lookup"><span data-stu-id="915b9-106">This function is for DEBUG ONLY.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="915b9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="915b9-107">Syntax</span></span>


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="915b9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="915b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="915b9-109">*errore* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="915b9-109">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="915b9-110">Puntatore a un oggetto [WS \_ Error](ws-error.md) in cui è necessario archiviare informazioni aggiuntive sull'errore se la funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="915b9-110">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="915b9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="915b9-111">Return value</span></span>

<span data-ttu-id="915b9-112">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="915b9-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="915b9-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="915b9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="915b9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="915b9-114">Requirements</span></span>



| <span data-ttu-id="915b9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="915b9-115">Requirement</span></span> | <span data-ttu-id="915b9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="915b9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="915b9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="915b9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="915b9-118">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="915b9-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                             |
| <span data-ttu-id="915b9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="915b9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="915b9-120">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="915b9-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="915b9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="915b9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="915b9-122"><dt>WebServicesDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="915b9-122"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





