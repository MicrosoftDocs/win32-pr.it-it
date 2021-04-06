---
title: Metodo GetStringProperty della classe Win32_RDSHCollection
description: Recupera un valore della proprietà di stringa di un \_ oggetto Win32 RDSHCollection.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo GetStringProperty
- Metodo GetStringProperty Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, Metodo GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963909"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="26693-106">Metodo GetStringProperty della \_ classe RDSHCollection Win32</span><span class="sxs-lookup"><span data-stu-id="26693-106">GetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="26693-107">Recupera un valore della proprietà di stringa di un oggetto [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="26693-107">Retrieves a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26693-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26693-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="26693-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="26693-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26693-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="26693-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26693-111">Chiave che identifica la proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="26693-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="26693-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="26693-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26693-113">Riceve il valore della proprietà recuperata.</span><span class="sxs-lookup"><span data-stu-id="26693-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26693-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26693-114">Return value</span></span>

<span data-ttu-id="26693-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="26693-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26693-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26693-116">Requirements</span></span>



| <span data-ttu-id="26693-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="26693-117">Requirement</span></span> | <span data-ttu-id="26693-118">Valore</span><span class="sxs-lookup"><span data-stu-id="26693-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="26693-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26693-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26693-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="26693-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="26693-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26693-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26693-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26693-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="26693-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26693-123">Namespace</span></span><br/>                | <span data-ttu-id="26693-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="26693-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="26693-125">MOF</span><span class="sxs-lookup"><span data-stu-id="26693-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26693-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26693-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="26693-127">DLL</span><span class="sxs-lookup"><span data-stu-id="26693-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26693-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26693-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="26693-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26693-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26693-130">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="26693-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





