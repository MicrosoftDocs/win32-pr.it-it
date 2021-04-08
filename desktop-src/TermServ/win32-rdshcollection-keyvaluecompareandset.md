---
title: Metodo KeyValueCompareAndSet della classe Win32_RDSHCollection
description: Confronta la chiave specificata nella raccolta con un comparand; Se corrispondono, la chiave viene impostata su un nuovo valore. Se la chiave non esiste, il metodo inserirà la chiave nella raccolta.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo KeyValueCompareAndSet
- Metodo KeyValueCompareAndSet Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, metodo KeyValueCompareAndSet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873622"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="cd6fb-107">Metodo KeyValueCompareAndSet della \_ classe RDSHCollection Win32</span><span class="sxs-lookup"><span data-stu-id="cd6fb-107">KeyValueCompareAndSet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="cd6fb-108">Confronta la chiave specificata nella raccolta con un comparand; Se corrispondono, la chiave viene impostata su un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="cd6fb-108">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="cd6fb-109">Se la chiave non esiste, il metodo inserirà la chiave nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="cd6fb-109">If the key does not exist, the method will insert the key into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6fb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd6fb-110">Syntax</span></span>


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a><span data-ttu-id="cd6fb-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd6fb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd6fb-112">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cd6fb-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6fb-113">Chiave da confrontare.</span><span class="sxs-lookup"><span data-stu-id="cd6fb-113">The key to compare.</span></span>

</dd> <dt>

<span data-ttu-id="cd6fb-114">*NewValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd6fb-114">*NewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6fb-115">Nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="cd6fb-115">The new value.</span></span>

</dd> <dt>

<span data-ttu-id="cd6fb-116">*Comparand* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd6fb-116">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6fb-117">Stringa da confrontare con la chiave.</span><span class="sxs-lookup"><span data-stu-id="cd6fb-117">The string to compare the key to.</span></span>

</dd> <dt>

<span data-ttu-id="cd6fb-118">*InitialValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd6fb-118">*InitialValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6fb-119">In caso di esito positivo o negativo, contiene il valore iniziale della chiave.</span><span class="sxs-lookup"><span data-stu-id="cd6fb-119">On success or failure, contains the initial value of the key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd6fb-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd6fb-120">Remarks</span></span>

<span data-ttu-id="cd6fb-121">Si noti che questo metodo può recuperare il valore della chiave e, di conseguenza, incapsula la funzionalità di [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span><span class="sxs-lookup"><span data-stu-id="cd6fb-121">Note that this method can retrieve the value of the key, and as such encapsulates the functionality of [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6fb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd6fb-122">Requirements</span></span>



| <span data-ttu-id="cd6fb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd6fb-123">Requirement</span></span> | <span data-ttu-id="cd6fb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cd6fb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6fb-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd6fb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd6fb-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cd6fb-126">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cd6fb-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd6fb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd6fb-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cd6fb-128">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="cd6fb-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd6fb-129">Namespace</span></span><br/>                | <span data-ttu-id="cd6fb-130">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="cd6fb-130">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cd6fb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cd6fb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd6fb-132"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd6fb-132"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd6fb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cd6fb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd6fb-134"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd6fb-134"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cd6fb-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd6fb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6fb-136">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="cd6fb-136">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





