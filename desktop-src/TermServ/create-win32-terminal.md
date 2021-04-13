---
title: Metodo Create della classe Win32_Terminal
description: Crea un terminale con le impostazioni predefinite che possono essere personalizzate usando le proprietà e i metodi delle \_ classi Win32 TerminalSetting.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto crea metodo
- Create Method Servizi Desktop remoto, classe Win32_Terminal
- Classe Win32_Terminal Servizi Desktop remoto, metodo create
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475641"
---
# <a name="create-method-of-the-win32_terminal-class"></a><span data-ttu-id="d5381-106">Metodo Create della \_ classe terminale Win32</span><span class="sxs-lookup"><span data-stu-id="d5381-106">Create method of the Win32\_Terminal class</span></span>

<span data-ttu-id="d5381-107">Il metodo **create** crea un terminale con le impostazioni predefinite che possono essere personalizzate usando le proprietà e i metodi delle classi [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d5381-107">The **Create** method creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span> <span data-ttu-id="d5381-108">La funzione restituisce zero in caso di esito positivo e un errore in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="d5381-108">The function returns zero on success and an error on failure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5381-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5381-109">Syntax</span></span>


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="d5381-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5381-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5381-111">*NewTerminalName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5381-111">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5381-112">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="d5381-112">Name of the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="d5381-113">*Trasporto* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d5381-113">*Transport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5381-114">Trasporto per il terminale.</span><span class="sxs-lookup"><span data-stu-id="d5381-114">Transport for the terminal.</span></span> <span data-ttu-id="d5381-115">Si tratta di una proprietà della classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d5381-115">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d5381-116">*TerminalProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5381-116">*TerminalProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5381-117">Protocollo per il terminale.</span><span class="sxs-lookup"><span data-stu-id="d5381-117">Protocol for the terminal.</span></span> <span data-ttu-id="d5381-118">Si tratta di una proprietà della classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d5381-118">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5381-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5381-119">Return value</span></span>

<span data-ttu-id="d5381-120">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d5381-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d5381-121">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d5381-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5381-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5381-122">Remarks</span></span>

<span data-ttu-id="d5381-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d5381-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d5381-124">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d5381-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d5381-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="d5381-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d5381-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d5381-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5381-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5381-127">Requirements</span></span>



| <span data-ttu-id="d5381-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5381-128">Requirement</span></span> | <span data-ttu-id="d5381-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d5381-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5381-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5381-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d5381-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5381-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5381-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5381-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d5381-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5381-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5381-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d5381-134">Namespace</span></span><br/>                | <span data-ttu-id="d5381-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d5381-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d5381-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d5381-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5381-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5381-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5381-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d5381-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5381-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5381-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5381-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5381-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5381-141">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="d5381-141">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

