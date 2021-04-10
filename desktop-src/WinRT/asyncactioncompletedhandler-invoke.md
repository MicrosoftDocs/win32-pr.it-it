---
description: Richiama il metodo che viene chiamato quando l'azione asincrona specificata viene completata.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'Metodo AsyncActionCompletedHandler:: Invoke'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129247"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a><span data-ttu-id="d07bf-103">Metodo AsyncActionCompletedHandler:: Invoke</span><span class="sxs-lookup"><span data-stu-id="d07bf-103">AsyncActionCompletedHandler::Invoke method</span></span>

<span data-ttu-id="d07bf-104">Richiama il metodo che viene chiamato quando l'azione asincrona specificata viene completata.</span><span class="sxs-lookup"><span data-stu-id="d07bf-104">Invokes the method that is called when the specified asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d07bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d07bf-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d07bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d07bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d07bf-107">*AsyncInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d07bf-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d07bf-108">Tipo: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _</span><span class="sxs-lookup"><span data-stu-id="d07bf-108">Type: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\** _</span></span>

<span data-ttu-id="d07bf-109">Azione asincrona che segnala il completamento.</span><span class="sxs-lookup"><span data-stu-id="d07bf-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d07bf-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d07bf-110">Return value</span></span>

<span data-ttu-id="d07bf-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d07bf-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d07bf-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d07bf-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d07bf-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d07bf-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d07bf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d07bf-114">Requirements</span></span>



| <span data-ttu-id="d07bf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d07bf-115">Requirement</span></span> | <span data-ttu-id="d07bf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d07bf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07bf-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d07bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d07bf-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d07bf-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="d07bf-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d07bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d07bf-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d07bf-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="d07bf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d07bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d07bf-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d07bf-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d07bf-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d07bf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d07bf-124">**AsyncActionCompletedHandler**</span><span class="sxs-lookup"><span data-stu-id="d07bf-124">**AsyncActionCompletedHandler**</span></span>](asyncactioncompletedhandler.md)
</dt> </dl>

 

