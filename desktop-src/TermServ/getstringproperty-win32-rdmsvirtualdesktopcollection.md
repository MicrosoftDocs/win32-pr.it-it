---
title: Metodo GetStringProperty della classe Win32_RDMSVirtualDesktopCollection
description: Recupera una proprietà di stringa da un insieme di desktop virtuali.
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo GetStringProperty
- Metodo GetStringProperty Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, Metodo GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242d973d7ec8d320ed589933567b337a035f0e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301113"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="16e84-106">Metodo GetStringProperty della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="16e84-106">GetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="16e84-107">Recupera una proprietà di stringa da un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="16e84-107">Retrieves a string property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e84-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16e84-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="16e84-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="16e84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e84-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="16e84-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16e84-111">Chiave che identifica la proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="16e84-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="16e84-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="16e84-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16e84-113">Stringa che riceve il valore recuperato.</span><span class="sxs-lookup"><span data-stu-id="16e84-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e84-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16e84-114">Return value</span></span>

<span data-ttu-id="16e84-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="16e84-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e84-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16e84-116">Requirements</span></span>



| <span data-ttu-id="16e84-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e84-117">Requirement</span></span> | <span data-ttu-id="16e84-118">Valore</span><span class="sxs-lookup"><span data-stu-id="16e84-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="16e84-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16e84-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16e84-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="16e84-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="16e84-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16e84-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16e84-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16e84-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="16e84-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="16e84-123">Namespace</span></span><br/>                | <span data-ttu-id="16e84-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="16e84-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="16e84-125">MOF</span><span class="sxs-lookup"><span data-stu-id="16e84-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16e84-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16e84-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="16e84-127">DLL</span><span class="sxs-lookup"><span data-stu-id="16e84-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16e84-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16e84-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="16e84-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16e84-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e84-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="16e84-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





