---
title: Metodo SetInt32Property della classe Win32_RDSHCollection
description: Aggiorna un valore della proprietà Integer di un \_ oggetto Win32 RDSHCollection.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetInt32Property
- Metodo SetInt32Property Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, metodo SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 136bb8ccf34004f747829fb43ee8080ccd1d3132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302447"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="fea5e-106">Metodo SetInt32Property della \_ classe RDSHCollection Win32</span><span class="sxs-lookup"><span data-stu-id="fea5e-106">SetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="fea5e-107">Aggiorna un valore della proprietà Integer di un oggetto [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fea5e-107">Updates an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fea5e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fea5e-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="fea5e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fea5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea5e-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fea5e-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea5e-111">Chiave che identifica la proprietà da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="fea5e-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="fea5e-112">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fea5e-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea5e-113">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="fea5e-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea5e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fea5e-114">Return value</span></span>

<span data-ttu-id="fea5e-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="fea5e-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea5e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fea5e-116">Requirements</span></span>



| <span data-ttu-id="fea5e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fea5e-117">Requirement</span></span> | <span data-ttu-id="fea5e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fea5e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fea5e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fea5e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fea5e-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fea5e-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fea5e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fea5e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fea5e-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fea5e-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fea5e-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fea5e-123">Namespace</span></span><br/>                | <span data-ttu-id="fea5e-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="fea5e-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fea5e-125">MOF</span><span class="sxs-lookup"><span data-stu-id="fea5e-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fea5e-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fea5e-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fea5e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fea5e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fea5e-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fea5e-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fea5e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fea5e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea5e-130">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="fea5e-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





