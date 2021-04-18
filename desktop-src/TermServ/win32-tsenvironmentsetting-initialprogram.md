---
title: Metodo InitialProgram della classe Win32_TSEnvironmentSetting
description: Il metodo InitialProgram imposta le proprietà del programma di avvio, ad esempio il nome, la directory di lavoro e il percorso del programma da avviare immediatamente dopo l'accesso al server host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InitialProgram
- Metodo InitialProgram Servizi Desktop remoto, classe Win32_TSEnvironmentSetting
- Classe Win32_TSEnvironmentSetting Servizi Desktop remoto, metodo InitialProgram
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301506"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="8d613-106">Metodo InitialProgram della \_ classe TSEnvironmentSetting Win32</span><span class="sxs-lookup"><span data-stu-id="8d613-106">InitialProgram method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="8d613-107">Il metodo **InitialProgram** imposta le proprietà del programma di avvio, ad esempio il nome, la directory di lavoro e il percorso del programma da avviare immediatamente dopo l'accesso al server Host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="8d613-107">The **InitialProgram** method sets startup program properties such as the name, working directory, and path of the program to start immediately after logon to the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d613-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d613-108">Syntax</span></span>


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a><span data-ttu-id="8d613-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d613-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d613-110">*InitialProgramPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d613-110">*InitialProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d613-111">Nome e percorso del programma di avvio.</span><span class="sxs-lookup"><span data-stu-id="8d613-111">The name and path of the startup program.</span></span>

</dd> <dt>

<span data-ttu-id="8d613-112">*Avvio in* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d613-112">*Startin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d613-113">Percorso della directory di lavoro del programma di avvio.</span><span class="sxs-lookup"><span data-stu-id="8d613-113">The path to the working directory of the startup program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d613-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d613-114">Return value</span></span>

<span data-ttu-id="8d613-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="8d613-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8d613-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="8d613-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8d613-117">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8d613-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d613-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d613-118">Remarks</span></span>

<span data-ttu-id="8d613-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8d613-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8d613-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8d613-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8d613-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8d613-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8d613-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8d613-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d613-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d613-123">Requirements</span></span>



| <span data-ttu-id="8d613-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d613-124">Requirement</span></span> | <span data-ttu-id="8d613-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8d613-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d613-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d613-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8d613-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d613-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d613-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d613-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8d613-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d613-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d613-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d613-130">Namespace</span></span><br/>                | <span data-ttu-id="8d613-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8d613-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8d613-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8d613-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d613-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d613-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d613-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8d613-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d613-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d613-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d613-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d613-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d613-137">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8d613-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

