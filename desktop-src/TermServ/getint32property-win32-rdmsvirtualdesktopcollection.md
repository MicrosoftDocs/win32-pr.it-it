---
title: Metodo GetInt32Property della classe Win32_RDMSVirtualDesktopCollection (Microsoft. Diagnostics. appanalysis. h)
description: Recupera una proprietà Integer da un insieme di desktop virtuali.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetInt32Property
- Metodo GetInt32Property Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301114"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="83f63-106">Metodo GetInt32Property della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="83f63-106">GetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="83f63-107">Recupera una proprietà Integer da un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="83f63-107">Retrieves an integer property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f63-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83f63-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="83f63-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="83f63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83f63-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="83f63-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83f63-111">Chiave che identifica la proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="83f63-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="83f63-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="83f63-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83f63-113">Intero che riceve il valore recuperato.</span><span class="sxs-lookup"><span data-stu-id="83f63-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83f63-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83f63-114">Return value</span></span>

<span data-ttu-id="83f63-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="83f63-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="83f63-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83f63-116">Requirements</span></span>



| <span data-ttu-id="83f63-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="83f63-117">Requirement</span></span> | <span data-ttu-id="83f63-118">Valore</span><span class="sxs-lookup"><span data-stu-id="83f63-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83f63-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83f63-119">Minimum supported client</span></span><br/> | <span data-ttu-id="83f63-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="83f63-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="83f63-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83f63-121">Minimum supported server</span></span><br/> | <span data-ttu-id="83f63-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83f63-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="83f63-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83f63-123">Namespace</span></span><br/>                | <span data-ttu-id="83f63-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="83f63-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="83f63-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83f63-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="83f63-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="83f63-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="83f63-127">MOF</span><span class="sxs-lookup"><span data-stu-id="83f63-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83f63-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83f63-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="83f63-129">DLL</span><span class="sxs-lookup"><span data-stu-id="83f63-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83f63-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83f63-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="83f63-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83f63-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f63-132">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="83f63-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





