---
title: Metodo SetStringProperty della classe Win32_RDSHCollection (CertEnroll. h)
description: Aggiorna il valore di una proprietà di stringa di un \_ oggetto Win32 RDSHCollection.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo SetStringProperty
- Metodo SetStringProperty Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, Metodo SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2606c195822432138ee67576db54f945c6834cfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301966"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="97178-106">Metodo SetStringProperty della \_ classe RDSHCollection Win32</span><span class="sxs-lookup"><span data-stu-id="97178-106">SetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="97178-107">Aggiorna il valore di una proprietà di stringa di un oggetto [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="97178-107">Updates a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="97178-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97178-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="97178-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="97178-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97178-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="97178-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97178-111">Chiave che identifica la proprietà da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="97178-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="97178-112">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="97178-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97178-113">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="97178-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97178-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97178-114">Return value</span></span>

<span data-ttu-id="97178-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="97178-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="97178-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97178-116">Requirements</span></span>



| <span data-ttu-id="97178-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="97178-117">Requirement</span></span> | <span data-ttu-id="97178-118">Valore</span><span class="sxs-lookup"><span data-stu-id="97178-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="97178-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97178-119">Minimum supported client</span></span><br/> | <span data-ttu-id="97178-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="97178-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="97178-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97178-121">Minimum supported server</span></span><br/> | <span data-ttu-id="97178-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97178-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="97178-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="97178-123">Namespace</span></span><br/>                | <span data-ttu-id="97178-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="97178-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="97178-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97178-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="97178-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="97178-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="97178-127">MOF</span><span class="sxs-lookup"><span data-stu-id="97178-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97178-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97178-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="97178-129">DLL</span><span class="sxs-lookup"><span data-stu-id="97178-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97178-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97178-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="97178-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97178-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97178-132">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="97178-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





