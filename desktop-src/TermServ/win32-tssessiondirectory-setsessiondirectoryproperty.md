---
title: Metodo SetSessionDirectoryProperty della classe Win32_TSSessionDirectory
description: Imposta la proprietà SessionDirectoryLocation o la proprietà SessionDirectoryClusterName per la classe.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSessionDirectoryProperty
- Metodo SetSessionDirectoryProperty Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetSessionDirectoryProperty
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476192"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="050c9-106">Metodo SetSessionDirectoryProperty della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="050c9-106">SetSessionDirectoryProperty method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="050c9-107">Imposta la proprietà **SessionDirectoryLocation** o la proprietà **SessionDirectoryClusterName** per la classe.</span><span class="sxs-lookup"><span data-stu-id="050c9-107">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="050c9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="050c9-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="050c9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="050c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="050c9-110">*PropertyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="050c9-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050c9-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="050c9-111">Type: **string**</span></span>

<span data-ttu-id="050c9-112">Specifica la proprietà che il metodo sta impostando.</span><span class="sxs-lookup"><span data-stu-id="050c9-112">Specifies the property that the method is setting.</span></span>

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span data-ttu-id="050c9-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="050c9-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span></span>


</dt> <dd>

<span data-ttu-id="050c9-114">Il metodo sta impostando la proprietà **SessionDirectoryLocation** .</span><span class="sxs-lookup"><span data-stu-id="050c9-114">The method is setting the **SessionDirectoryLocation** property.</span></span>

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span data-ttu-id="050c9-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="050c9-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span></span>


</dt> <dd>

<span data-ttu-id="050c9-116">Il metodo sta impostando la proprietà **SessionDirectoryClusterName** .</span><span class="sxs-lookup"><span data-stu-id="050c9-116">The method is setting the **SessionDirectoryClusterName** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="050c9-117">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="050c9-117">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="050c9-118">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="050c9-118">Type: **string**</span></span>

<span data-ttu-id="050c9-119">Nuovo valore per la proprietà specificata dal parametro *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="050c9-119">The new value for the property specified by the *PropertyName* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="050c9-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="050c9-120">Return value</span></span>

<span data-ttu-id="050c9-121">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="050c9-121">Type: **uint32**</span></span>

<span data-ttu-id="050c9-122">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="050c9-122">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="050c9-123">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="050c9-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="050c9-124">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="050c9-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="050c9-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="050c9-125">Remarks</span></span>

<span data-ttu-id="050c9-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="050c9-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="050c9-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="050c9-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="050c9-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="050c9-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="050c9-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="050c9-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="050c9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="050c9-130">Requirements</span></span>



| <span data-ttu-id="050c9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="050c9-131">Requirement</span></span> | <span data-ttu-id="050c9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="050c9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="050c9-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="050c9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="050c9-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="050c9-134">None supported</span></span><br/>                                                               |
| <span data-ttu-id="050c9-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="050c9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="050c9-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="050c9-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="050c9-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="050c9-137">Namespace</span></span><br/>                | <span data-ttu-id="050c9-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="050c9-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="050c9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="050c9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="050c9-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="050c9-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="050c9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="050c9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="050c9-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="050c9-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="050c9-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="050c9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050c9-144">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="050c9-144">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

