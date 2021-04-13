---
title: Metodo PingSessionDirectory della classe Win32_TSSessionDirectory
description: Verifica se è disponibile il server Gestore connessione Desktop remoto (Connessione Desktop remoto Broker).
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo PingSessionDirectory
- Metodo PingSessionDirectory Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo PingSessionDirectory
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4022a0c34094a19651522c3f8153038c6d9df503
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518040"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="6fe50-106">Metodo PingSessionDirectory della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="6fe50-106">PingSessionDirectory method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="6fe50-107">Verifica se è disponibile il server Gestore connessione Desktop remoto (Connessione Desktop remoto Broker).</span><span class="sxs-lookup"><span data-stu-id="6fe50-107">Checks whether the Remote Desktop Connection Broker (RD Connection Broker) server is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe50-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fe50-108">Syntax</span></span>


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="6fe50-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fe50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe50-110">*Nomeserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fe50-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe50-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6fe50-111">Type: **string**</span></span>

<span data-ttu-id="6fe50-112">Nome del server Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="6fe50-112">Name of the RD Connection Broker server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe50-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fe50-113">Return value</span></span>

<span data-ttu-id="6fe50-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fe50-114">Type: **uint32**</span></span>

<span data-ttu-id="6fe50-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="6fe50-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6fe50-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6fe50-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fe50-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fe50-117">Remarks</span></span>

<span data-ttu-id="6fe50-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6fe50-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6fe50-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="6fe50-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6fe50-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6fe50-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6fe50-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6fe50-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe50-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fe50-122">Requirements</span></span>



| <span data-ttu-id="6fe50-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fe50-123">Requirement</span></span> | <span data-ttu-id="6fe50-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6fe50-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe50-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fe50-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe50-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6fe50-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6fe50-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fe50-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe50-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fe50-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6fe50-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6fe50-129">Namespace</span></span><br/>                | <span data-ttu-id="6fe50-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6fe50-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6fe50-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6fe50-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fe50-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fe50-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fe50-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6fe50-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fe50-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fe50-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe50-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fe50-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe50-136">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="6fe50-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

