---
title: Metodo GetStringProperty della classe Win32_RDSHServer
description: Recupera un valore della proprietà di stringa di un \_ oggetto Win32 RDSHServer.
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo GetStringProperty
- Metodo GetStringProperty Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, Metodo GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619a034e0a2f89270d21bf0c4fc297b4248cef59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479115"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="f5368-106">Metodo GetStringProperty della \_ classe RDSHServer Win32</span><span class="sxs-lookup"><span data-stu-id="f5368-106">GetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="f5368-107">Recupera un valore della proprietà di stringa di un oggetto [**Win32 \_ RDSHServer**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="f5368-107">Retrieves a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5368-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5368-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="f5368-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5368-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5368-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f5368-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5368-111">Chiave che identifica la proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f5368-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f5368-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f5368-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5368-113">Riceve il valore della proprietà recuperata.</span><span class="sxs-lookup"><span data-stu-id="f5368-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5368-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5368-114">Return value</span></span>

<span data-ttu-id="f5368-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="f5368-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5368-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5368-116">Requirements</span></span>



| <span data-ttu-id="f5368-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5368-117">Requirement</span></span> | <span data-ttu-id="f5368-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f5368-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5368-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5368-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5368-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f5368-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f5368-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5368-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5368-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5368-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f5368-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5368-123">Namespace</span></span><br/>                | <span data-ttu-id="f5368-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="f5368-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f5368-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f5368-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5368-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5368-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5368-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f5368-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5368-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5368-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f5368-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5368-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5368-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="f5368-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





