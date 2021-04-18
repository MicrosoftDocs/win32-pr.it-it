---
title: Rinominare il metodo della classe Win32_Terminal
description: Il metodo Rename Rinomina il terminale.
ms.assetid: 85b5c83b-8ca3-4ed0-852b-b11ba98c18a6
ms.tgt_platform: multiple
keywords:
- Rinomina Servizi Desktop remoto metodo
- Rinominare il metodo Servizi Desktop remoto, Win32_Terminal classe
- Classe Win32_Terminal Servizi Desktop remoto, Rinomina metodo
topic_type:
- apiref
api_name:
- Win32_Terminal.Rename
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0258277bd509f7f72d5e314bc20d9852fa03315a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301204"
---
# <a name="rename-method-of-the-win32_terminal-class"></a><span data-ttu-id="d56ac-106">Rinominare il metodo della \_ classe terminale Win32</span><span class="sxs-lookup"><span data-stu-id="d56ac-106">Rename method of the Win32\_Terminal class</span></span>

<span data-ttu-id="d56ac-107">Il metodo **Rename Rinomina** il terminale.</span><span class="sxs-lookup"><span data-stu-id="d56ac-107">The **Rename** method renames the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="d56ac-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d56ac-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="d56ac-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d56ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d56ac-110">*NewTerminalName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d56ac-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d56ac-111">Nuovo nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="d56ac-111">The new name of the terminal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d56ac-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d56ac-112">Return value</span></span>

<span data-ttu-id="d56ac-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d56ac-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d56ac-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d56ac-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d56ac-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d56ac-115">Remarks</span></span>

<span data-ttu-id="d56ac-116">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d56ac-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d56ac-117">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d56ac-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d56ac-118">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="d56ac-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d56ac-119">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d56ac-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d56ac-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d56ac-120">Requirements</span></span>



| <span data-ttu-id="d56ac-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d56ac-121">Requirement</span></span> | <span data-ttu-id="d56ac-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d56ac-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d56ac-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d56ac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d56ac-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d56ac-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d56ac-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d56ac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d56ac-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d56ac-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d56ac-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d56ac-127">Namespace</span></span><br/>                | <span data-ttu-id="d56ac-128">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d56ac-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d56ac-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d56ac-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d56ac-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d56ac-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d56ac-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d56ac-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d56ac-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d56ac-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d56ac-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d56ac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d56ac-134">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="d56ac-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

