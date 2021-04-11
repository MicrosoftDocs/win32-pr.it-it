---
title: Metodo KeyValueDelete della classe Win32_RDSHCollection
description: Elimina dalla raccolta la chiave specificata e il valore associato.
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo KeyValueDelete
- Metodo KeyValueDelete Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, metodo KeyValueDelete
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964079"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="01b29-106">Metodo KeyValueDelete della \_ classe RDSHCollection Win32</span><span class="sxs-lookup"><span data-stu-id="01b29-106">KeyValueDelete method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="01b29-107">Elimina dalla raccolta la chiave specificata e il valore associato.</span><span class="sxs-lookup"><span data-stu-id="01b29-107">Deletes the specified key (and associated value) from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b29-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01b29-108">Syntax</span></span>


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="01b29-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="01b29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b29-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="01b29-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01b29-111">Chiave da eliminare.</span><span class="sxs-lookup"><span data-stu-id="01b29-111">The key to delete.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01b29-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01b29-112">Requirements</span></span>



| <span data-ttu-id="01b29-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b29-113">Requirement</span></span> | <span data-ttu-id="01b29-114">Valore</span><span class="sxs-lookup"><span data-stu-id="01b29-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b29-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b29-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01b29-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="01b29-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="01b29-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b29-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01b29-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="01b29-118">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="01b29-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01b29-119">Namespace</span></span><br/>                | <span data-ttu-id="01b29-120">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="01b29-120">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="01b29-121">MOF</span><span class="sxs-lookup"><span data-stu-id="01b29-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01b29-122"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01b29-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="01b29-123">DLL</span><span class="sxs-lookup"><span data-stu-id="01b29-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01b29-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01b29-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="01b29-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01b29-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b29-126">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="01b29-126">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





