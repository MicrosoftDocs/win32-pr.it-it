---
title: Metodo SetInt32Property della classe Win32_RDSHServer
description: Aggiorna un valore della proprietà Integer di un \_ oggetto Win32 RDSHServer.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetInt32Property
- Metodo SetInt32Property Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, metodo SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741298"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="8ae7a-106">Metodo SetInt32Property della \_ classe RDSHServer Win32</span><span class="sxs-lookup"><span data-stu-id="8ae7a-106">SetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="8ae7a-107">Aggiorna un valore della proprietà Integer di un oggetto [**Win32 \_ RDSHServer**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="8ae7a-107">Updates an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae7a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ae7a-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="8ae7a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ae7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae7a-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8ae7a-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae7a-111">Chiave che identifica la proprietà da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="8ae7a-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="8ae7a-112">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8ae7a-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae7a-113">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8ae7a-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae7a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ae7a-114">Return value</span></span>

<span data-ttu-id="8ae7a-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="8ae7a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae7a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ae7a-116">Requirements</span></span>



| <span data-ttu-id="8ae7a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ae7a-117">Requirement</span></span> | <span data-ttu-id="8ae7a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8ae7a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae7a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ae7a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae7a-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8ae7a-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8ae7a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ae7a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae7a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ae7a-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8ae7a-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8ae7a-123">Namespace</span></span><br/>                | <span data-ttu-id="8ae7a-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="8ae7a-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8ae7a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="8ae7a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ae7a-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ae7a-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ae7a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8ae7a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ae7a-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ae7a-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8ae7a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ae7a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae7a-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="8ae7a-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





