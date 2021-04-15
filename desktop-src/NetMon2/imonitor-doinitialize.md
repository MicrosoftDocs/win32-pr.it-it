---
description: Il metodo DoInitialize deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere un filtro di acquisizione immediatamente prima di chiamare il metodo IRTCConnect di centrali.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Metodo IMonitorDoInitialize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525116"
---
# <a name="imonitordoinitialize-method"></a><span data-ttu-id="3661f-104">IMonitor::D Metodo oInitialize</span><span class="sxs-lookup"><span data-stu-id="3661f-104">IMonitor::DoInitialize method</span></span>

<span data-ttu-id="3661f-105">Il metodo **DoInitialize** deve essere implementato dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="3661f-105">The **DoInitialize** method must be implemented by the monitor.</span></span> <span data-ttu-id="3661f-106">MCSVC chiama questo metodo per ottenere un filtro di acquisizione immediatamente prima di chiamare il metodo [IRTC:: Connect](irtc-connect.md) di NPP.</span><span class="sxs-lookup"><span data-stu-id="3661f-106">The MCSVC calls this method to obtain a capture filter immediately before calling the NPP's [IRTC::Connect](irtc-connect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3661f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3661f-107">Syntax</span></span>


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a><span data-ttu-id="3661f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3661f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3661f-109">*pUnkMonitorCtrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3661f-109">*pUnkMonitorCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3661f-110">Puntatore [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) passato da MCSVC.</span><span class="sxs-lookup"><span data-stu-id="3661f-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer passed in by the MCSVC.</span></span> <span data-ttu-id="3661f-111">Per ottenere un'interfaccia di controllo di monitoraggio supportata, il monitoraggio deve chiamare [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'indicatore di misura.</span><span class="sxs-lookup"><span data-stu-id="3661f-111">To obtain a supported monitor control interface, the monitor must call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer.</span></span>

</dd> <dt>

<span data-ttu-id="3661f-112">*hNPPBlob* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="3661f-112">*hNPPBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3661f-113">In input, un handle per un BLOB di NPP.</span><span class="sxs-lookup"><span data-stu-id="3661f-113">On input, a handle to an NPP BLOB.</span></span>

<span data-ttu-id="3661f-114">Nell'output, un BLOB di NPP che contiene un filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3661f-114">On output, an NPP BLOB that contains a capture filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3661f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3661f-115">Return value</span></span>

<span data-ttu-id="3661f-116">Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR).</span><span class="sxs-lookup"><span data-stu-id="3661f-116">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="3661f-117">Se il metodo ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="3661f-117">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="3661f-118">In errore, MCSVC non creerà il monitoraggio o chiamerà [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3661f-118">On error, the MCSVC will not create the monitor or call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="3661f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3661f-119">Remarks</span></span>

<span data-ttu-id="3661f-120">MCSVC chiama il metodo **DoInitialize** per eseguire l'inizializzazione del monitoraggio richiesta.</span><span class="sxs-lookup"><span data-stu-id="3661f-120">The MCSVC calls the **DoInitialize** method to perform any required monitor initialization.</span></span>

## <a name="requirements"></a><span data-ttu-id="3661f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3661f-121">Requirements</span></span>



| <span data-ttu-id="3661f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3661f-122">Requirement</span></span> | <span data-ttu-id="3661f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3661f-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3661f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3661f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3661f-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3661f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3661f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3661f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3661f-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3661f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3661f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3661f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3661f-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3661f-129"><dt>Netmon.h</dt></span></span> </dl> |



 

