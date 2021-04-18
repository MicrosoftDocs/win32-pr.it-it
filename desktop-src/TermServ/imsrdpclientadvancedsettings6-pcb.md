---
title: Proprietà PCB IMsRdpClientAdvancedSettings6
description: Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server. | Proprietà PCB IMsRdpClientAdvancedSettings6
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PCB
- Servizi Desktop remoto proprietà PCB, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PCB
- Servizi Desktop remoto proprietà PCB, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PCB
- Servizi Desktop remoto proprietà PCB, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PCB
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da9cfa12ec944ea8f745ec3399c2a53f6b7c6b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321187"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a><span data-ttu-id="ace08-111">IMsRdpClientAdvancedSettings6::P la proprietà CB</span><span class="sxs-lookup"><span data-stu-id="ace08-111">IMsRdpClientAdvancedSettings6::PCB property</span></span>

<span data-ttu-id="ace08-112">Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server.</span><span class="sxs-lookup"><span data-stu-id="ace08-112">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="ace08-113">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ace08-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace08-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ace08-114">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="ace08-115">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ace08-115">Property value</span></span>

<span data-ttu-id="ace08-116">Specifica l'impostazione del BLOB da usare prima della connessione.</span><span class="sxs-lookup"><span data-stu-id="ace08-116">Specifies the BLOB setting to use prior to connecting.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace08-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ace08-117">Remarks</span></span>

<span data-ttu-id="ace08-118">Questa proprietà è supportata solo dai client Connessione Desktop remoto 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="ace08-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="ace08-119">Il server utilizza l'impostazione BLOB per identificare il processo di destinazione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="ace08-119">The server uses the BLOB setting to identify the target process for the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace08-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ace08-120">Requirements</span></span>



| <span data-ttu-id="ace08-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ace08-121">Requirement</span></span> | <span data-ttu-id="ace08-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ace08-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace08-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace08-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ace08-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ace08-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="ace08-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace08-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ace08-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ace08-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="ace08-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ace08-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ace08-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace08-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ace08-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ace08-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace08-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace08-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ace08-131">IID</span><span class="sxs-lookup"><span data-stu-id="ace08-131">IID</span></span><br/>                      | <span data-ttu-id="ace08-132">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="ace08-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ace08-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ace08-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace08-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ace08-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ace08-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ace08-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ace08-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ace08-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





