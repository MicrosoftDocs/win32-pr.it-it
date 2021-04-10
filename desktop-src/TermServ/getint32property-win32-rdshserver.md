---
title: Metodo GetInt32Property della classe Win32_RDSHServer (Microsoft. Diagnostics. appanalysis. h)
description: Recupera un valore di proprietà Integer di un \_ oggetto Win32 RDSHServer.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetInt32Property
- Metodo GetInt32Property Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, metodo GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a2427cfa19a84a8b8988cceacf3e0b836a031f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964431"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="88c2c-106">Metodo GetInt32Property della \_ classe RDSHServer Win32</span><span class="sxs-lookup"><span data-stu-id="88c2c-106">GetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="88c2c-107">Recupera un valore di proprietà Integer di un oggetto [**Win32 \_ RDSHServer**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="88c2c-107">Retrieves an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c2c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88c2c-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="88c2c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="88c2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88c2c-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="88c2c-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88c2c-111">Chiave che identifica la proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="88c2c-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="88c2c-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="88c2c-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88c2c-113">Riceve il valore della proprietà recuperata.</span><span class="sxs-lookup"><span data-stu-id="88c2c-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88c2c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88c2c-114">Return value</span></span>

<span data-ttu-id="88c2c-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="88c2c-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="88c2c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88c2c-116">Requirements</span></span>



| <span data-ttu-id="88c2c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="88c2c-117">Requirement</span></span> | <span data-ttu-id="88c2c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="88c2c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c2c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88c2c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="88c2c-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="88c2c-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="88c2c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88c2c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="88c2c-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88c2c-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="88c2c-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88c2c-123">Namespace</span></span><br/>                | <span data-ttu-id="88c2c-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="88c2c-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="88c2c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88c2c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="88c2c-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c2c-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="88c2c-127">MOF</span><span class="sxs-lookup"><span data-stu-id="88c2c-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88c2c-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88c2c-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="88c2c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="88c2c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88c2c-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88c2c-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="88c2c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88c2c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c2c-132">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="88c2c-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





