---
title: Metodo EnvironmentVariables della classe Win32_TSExpandEnvironmentVariables
description: Espande le variabili di ambiente definite dal sistema. | Metodo EnvironmentVariables della classe Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnvironmentVariables
- Metodo EnvironmentVariables Servizi Desktop remoto, classe Win32_TSExpandEnvironmentVariables
- Classe Win32_TSExpandEnvironmentVariables Servizi Desktop remoto, metodo EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321265"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="3c468-107">Metodo EnvironmentVariables della \_ classe TSExpandEnvironmentVariables Win32</span><span class="sxs-lookup"><span data-stu-id="3c468-107">EnvironmentVariables method of the Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="3c468-108">Espande le variabili di ambiente definite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3c468-108">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c468-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c468-109">Syntax</span></span>


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a><span data-ttu-id="3c468-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c468-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c468-111">*OriginalString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c468-111">*OriginalString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c468-112">Stringa che contiene le variabili di ambiente da espandere.</span><span class="sxs-lookup"><span data-stu-id="3c468-112">A string that contains the environment variables to expand.</span></span>

</dd> <dt>

<span data-ttu-id="3c468-113">*ExpandedString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c468-113">*ExpandedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c468-114">Stringa con le variabili di ambiente espanse.</span><span class="sxs-lookup"><span data-stu-id="3c468-114">A string with the environment variables expanded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c468-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c468-115">Remarks</span></span>

<span data-ttu-id="3c468-116">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="3c468-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3c468-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3c468-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3c468-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="3c468-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3c468-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3c468-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3c468-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3c468-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c468-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c468-121">Requirements</span></span>



| <span data-ttu-id="3c468-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c468-122">Requirement</span></span> | <span data-ttu-id="3c468-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3c468-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c468-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c468-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c468-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3c468-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3c468-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c468-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c468-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c468-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c468-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c468-128">Namespace</span></span><br/>                | <span data-ttu-id="3c468-129">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3c468-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3c468-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3c468-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c468-131"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c468-131"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="3c468-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3c468-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c468-133"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c468-133"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c468-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c468-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c468-135">**\_TSExpandEnvironmentVariables Win32**</span><span class="sxs-lookup"><span data-stu-id="3c468-135">**Win32\_TSExpandEnvironmentVariables**</span></span>](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

