---
title: Metodo Delete della classe Win32_TSAccount
description: Il metodo Delete Elimina l'utente, il gruppo o l'account computer specificato.
ms.assetid: d0bb06d6-781c-4711-a59d-9ff233dd2a4c
ms.tgt_platform: multiple
keywords:
- Elimina Servizi Desktop remoto del metodo
- Metodo Delete Servizi Desktop remoto, classe Win32_TSAccount
- Classe Win32_TSAccount Servizi Desktop remoto, metodo Delete
topic_type:
- apiref
api_name:
- Win32_TSAccount.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ab76ad1200fc872a3a105e74533460104d806
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400872"
---
# <a name="delete-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="2f14d-106">Metodo Delete della classe Win32 \_ TSAccount</span><span class="sxs-lookup"><span data-stu-id="2f14d-106">Delete method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="2f14d-107">Il metodo **Delete** Elimina l'utente, il gruppo o l'account computer specificato.</span><span class="sxs-lookup"><span data-stu-id="2f14d-107">The **Delete** method deletes the specified user, group, or computer account.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f14d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f14d-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="2f14d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f14d-109">Parameters</span></span>

<span data-ttu-id="2f14d-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2f14d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f14d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f14d-111">Return value</span></span>

<span data-ttu-id="2f14d-112">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="2f14d-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2f14d-113">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2f14d-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f14d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f14d-114">Remarks</span></span>

<span data-ttu-id="2f14d-115">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2f14d-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2f14d-116">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2f14d-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2f14d-117">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="2f14d-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2f14d-118">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2f14d-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f14d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f14d-119">Requirements</span></span>



| <span data-ttu-id="2f14d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f14d-120">Requirement</span></span> | <span data-ttu-id="2f14d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2f14d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f14d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f14d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f14d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f14d-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f14d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f14d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f14d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f14d-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f14d-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f14d-126">Namespace</span></span><br/>                | <span data-ttu-id="2f14d-127">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2f14d-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2f14d-128">MOF</span><span class="sxs-lookup"><span data-stu-id="2f14d-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f14d-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f14d-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f14d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2f14d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f14d-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f14d-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f14d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f14d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f14d-133">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="2f14d-133">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

