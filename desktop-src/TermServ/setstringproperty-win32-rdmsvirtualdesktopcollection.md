---
title: Metodo SetStringProperty della classe Win32_RDMSVirtualDesktopCollection (CertEnroll. h)
description: Aggiorna una proprietà di stringa di un insieme di desktop virtuali.
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo SetStringProperty
- Metodo SetStringProperty Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, Metodo SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fd85ef6611cd02dc80ca66816c5c4ce13f6cd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301969"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="1c950-106">Metodo SetStringProperty della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="1c950-106">SetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="1c950-107">Aggiorna una proprietà di stringa di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="1c950-107">Updates a string property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c950-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c950-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="1c950-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c950-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c950-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1c950-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c950-111">Chiave che identifica la proprietà da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1c950-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="1c950-112">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1c950-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c950-113">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c950-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c950-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c950-114">Return value</span></span>

<span data-ttu-id="1c950-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="1c950-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c950-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c950-116">Requirements</span></span>



| <span data-ttu-id="1c950-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c950-117">Requirement</span></span> | <span data-ttu-id="1c950-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1c950-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c950-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c950-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c950-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1c950-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1c950-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c950-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c950-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c950-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1c950-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c950-123">Namespace</span></span><br/>                | <span data-ttu-id="1c950-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="1c950-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1c950-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c950-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c950-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c950-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="1c950-127">MOF</span><span class="sxs-lookup"><span data-stu-id="1c950-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c950-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c950-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c950-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1c950-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c950-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c950-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1c950-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c950-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c950-132">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="1c950-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





