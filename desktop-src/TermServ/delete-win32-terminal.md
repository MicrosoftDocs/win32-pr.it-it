---
title: Metodo Delete della classe Win32_Terminal
description: Elimina il terminale specificato.
ms.assetid: 59d8cc73-aef1-49d2-a7a2-dd3cbe5a8c52
ms.tgt_platform: multiple
keywords:
- Elimina Servizi Desktop remoto del metodo
- Metodo Delete Servizi Desktop remoto, classe Win32_Terminal
- Classe Win32_Terminal Servizi Desktop remoto, metodo Delete
topic_type:
- apiref
api_name:
- Win32_Terminal.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b7120c78eada2b047f836219d3382e5ce1e2f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301127"
---
# <a name="delete-method-of-the-win32_terminal-class"></a><span data-ttu-id="0cf8a-106">Metodo Delete della \_ classe terminale Win32</span><span class="sxs-lookup"><span data-stu-id="0cf8a-106">Delete method of the Win32\_Terminal class</span></span>

<span data-ttu-id="0cf8a-107">Il metodo **Delete** Elimina il terminale specificato.</span><span class="sxs-lookup"><span data-stu-id="0cf8a-107">The **Delete** method deletes the specified terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf8a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cf8a-108">Syntax</span></span>


```mof
uint32 Delete(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="0cf8a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cf8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf8a-110">*NewTerminalName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cf8a-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf8a-111">Nome del terminale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0cf8a-111">Name of the terminal to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf8a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cf8a-112">Return value</span></span>

<span data-ttu-id="0cf8a-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="0cf8a-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0cf8a-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0cf8a-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cf8a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cf8a-115">Remarks</span></span>

<span data-ttu-id="0cf8a-116">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0cf8a-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0cf8a-117">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0cf8a-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0cf8a-118">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0cf8a-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0cf8a-119">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0cf8a-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf8a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cf8a-120">Requirements</span></span>



| <span data-ttu-id="0cf8a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cf8a-121">Requirement</span></span> | <span data-ttu-id="0cf8a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0cf8a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf8a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cf8a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0cf8a-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cf8a-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cf8a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cf8a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0cf8a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cf8a-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cf8a-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0cf8a-127">Namespace</span></span><br/>                | <span data-ttu-id="0cf8a-128">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0cf8a-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0cf8a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="0cf8a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cf8a-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cf8a-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cf8a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0cf8a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cf8a-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cf8a-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cf8a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cf8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf8a-134">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="0cf8a-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

