---
title: Metodo SetServerWeight della classe Win32_TSSessionDirectory
description: Imposta il valore del peso del server per il bilanciamento del carico di Connessione Desktop remoto broker (gestore connessione Desktop remoto).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetServerWeight
- Metodo SetServerWeight Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetServerWeight
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477716"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="c83b3-106">Metodo SetServerWeight della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="c83b3-106">SetServerWeight method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="c83b3-107">Imposta il valore del peso del server per il bilanciamento del carico di Connessione Desktop remoto broker (gestore connessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="c83b3-107">Sets the server weight value for Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="c83b3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c83b3-108">Syntax</span></span>


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a><span data-ttu-id="c83b3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c83b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c83b3-110">*ServerWeightValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c83b3-110">*ServerWeightValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83b3-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c83b3-111">Type: **uint32**</span></span>

<span data-ttu-id="c83b3-112">Valore del peso del server.</span><span class="sxs-lookup"><span data-stu-id="c83b3-112">The server weight value.</span></span> <span data-ttu-id="c83b3-113">L'intervallo valido è compreso tra 1 e 10000.</span><span class="sxs-lookup"><span data-stu-id="c83b3-113">The valid range is 1 to 10000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c83b3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c83b3-114">Remarks</span></span>

<span data-ttu-id="c83b3-115">Per impostazione predefinita, nell'interfaccia utente di Servizi Desktop remoto configurazione, il valore del peso del server è 100.</span><span class="sxs-lookup"><span data-stu-id="c83b3-115">By default in the user interface of Remote Desktop Services Configuration, the server weight value is 100.</span></span> <span data-ttu-id="c83b3-116">Il peso del server è relativo.</span><span class="sxs-lookup"><span data-stu-id="c83b3-116">The server weight is relative.</span></span> <span data-ttu-id="c83b3-117">Se pertanto si assegna un server a un valore 100 e un valore pari a 200, il server con un peso relativo di 200 riceverà il doppio del numero di sessioni.</span><span class="sxs-lookup"><span data-stu-id="c83b3-117">Therefore, if you assign one server a value of 100, and one a value of 200, the server with a relative weight of 200 will receive twice the number of sessions.</span></span>

<span data-ttu-id="c83b3-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c83b3-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c83b3-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="c83b3-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c83b3-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="c83b3-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c83b3-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c83b3-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c83b3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c83b3-122">Requirements</span></span>



| <span data-ttu-id="c83b3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c83b3-123">Requirement</span></span> | <span data-ttu-id="c83b3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c83b3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c83b3-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c83b3-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c83b3-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c83b3-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c83b3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c83b3-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c83b3-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c83b3-129">Namespace</span></span><br/>                | <span data-ttu-id="c83b3-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c83b3-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c83b3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c83b3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c83b3-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c83b3-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c83b3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c83b3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c83b3-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c83b3-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c83b3-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c83b3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c83b3-136">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="c83b3-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

