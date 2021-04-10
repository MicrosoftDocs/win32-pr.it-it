---
title: Metodo SetInt32Property della classe Win32_RDMSVirtualDesktopCollection
description: Aggiorna una proprietà Integer di un insieme di desktop virtuali.
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetInt32Property
- Metodo SetInt32Property Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121214"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="e5ba7-106">Metodo SetInt32Property della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="e5ba7-106">SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="e5ba7-107">Aggiorna una proprietà Integer di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-107">Updates an integer property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ba7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5ba7-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="e5ba7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5ba7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ba7-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e5ba7-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ba7-111">Chiave che identifica la proprietà da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="e5ba7-112">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e5ba7-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ba7-113">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ba7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5ba7-114">Return value</span></span>

<span data-ttu-id="e5ba7-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ba7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5ba7-116">Requirements</span></span>



| <span data-ttu-id="e5ba7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5ba7-117">Requirement</span></span> | <span data-ttu-id="e5ba7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e5ba7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ba7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5ba7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ba7-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e5ba7-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e5ba7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5ba7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ba7-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5ba7-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e5ba7-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e5ba7-123">Namespace</span></span><br/>                | <span data-ttu-id="e5ba7-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="e5ba7-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e5ba7-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e5ba7-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5ba7-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5ba7-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5ba7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e5ba7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5ba7-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5ba7-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e5ba7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5ba7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ba7-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="e5ba7-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





