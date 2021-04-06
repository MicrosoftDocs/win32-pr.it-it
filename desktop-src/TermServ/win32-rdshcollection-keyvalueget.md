---
title: Metodo KeyValueGet della classe Win32_RDSHCollection
description: Recupera il valore associato alla chiave specificata nella raccolta.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo KeyValueGet
- Metodo KeyValueGet Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, metodo KeyValueGet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873621"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="38f3e-106">Metodo KeyValueGet della \_ classe RDSHCollection Win32</span><span class="sxs-lookup"><span data-stu-id="38f3e-106">KeyValueGet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="38f3e-107">Recupera il valore associato alla chiave specificata nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="38f3e-107">Retrieves the value associated with the specified key in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f3e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38f3e-108">Syntax</span></span>


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="38f3e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="38f3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f3e-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="38f3e-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f3e-111">Chiave che identifica il valore che si desidera recuperare.</span><span class="sxs-lookup"><span data-stu-id="38f3e-111">The key that identifies the value you wish to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="38f3e-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="38f3e-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f3e-113">Se l'operazione riesce, restituisce il valore associato alla chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="38f3e-113">On success, returns the value associated with the specified key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38f3e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38f3e-114">Requirements</span></span>



| <span data-ttu-id="38f3e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f3e-115">Requirement</span></span> | <span data-ttu-id="38f3e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="38f3e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f3e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38f3e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="38f3e-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="38f3e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="38f3e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38f3e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="38f3e-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="38f3e-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="38f3e-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38f3e-121">Namespace</span></span><br/>                | <span data-ttu-id="38f3e-122">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="38f3e-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="38f3e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="38f3e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38f3e-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38f3e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="38f3e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="38f3e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38f3e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38f3e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="38f3e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38f3e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f3e-128">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="38f3e-128">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





