---
title: Classe Win32_TSVirtualDesktopServerSettings
description: Contiene informazioni di configurazione per un server di Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVirtualDesktopServerSettings Servizi Desktop remoto
- Classe Win32_TSVirtualDesktopServerSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743266"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a><span data-ttu-id="593ee-105">Win32 \_ TSVirtualDesktopServerSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="593ee-105">Win32\_TSVirtualDesktopServerSettings class</span></span>

<span data-ttu-id="593ee-106">Contiene informazioni di configurazione per un server di Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="593ee-106">Contains configuration information for a Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

<span data-ttu-id="593ee-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="593ee-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="593ee-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="593ee-108">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a><span data-ttu-id="593ee-109">Members</span><span class="sxs-lookup"><span data-stu-id="593ee-109">Members</span></span>

<span data-ttu-id="593ee-110">La classe **Win32 \_ TSVirtualDesktopServerSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="593ee-110">The **Win32\_TSVirtualDesktopServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="593ee-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="593ee-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="593ee-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="593ee-112">Properties</span></span>

<span data-ttu-id="593ee-113">La classe **Win32 \_ TSVirtualDesktopServerSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="593ee-113">The **Win32\_TSVirtualDesktopServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="593ee-114">**Concorrenza**</span><span class="sxs-lookup"><span data-stu-id="593ee-114">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="593ee-115">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="593ee-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="593ee-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="593ee-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="593ee-117">Il numero massimo consentito di richieste di provisioning simultanee per questo server desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="593ee-117">The maximum allowed concurrent provisioning requests for this Virtual Desktop Server.</span></span>

</dd> <dt>

<span data-ttu-id="593ee-118">**PolicySourceSessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="593ee-118">**PolicySourceSessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="593ee-119">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="593ee-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="593ee-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="593ee-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="593ee-121">Se impostato su 0, indica che la proprietà **SessionBrokerName** è configurata dal server. Se impostato su 1, indica che la proprietà **SessionBrokerName** è configurata da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="593ee-121">If set to 0, indicates that the **SessionBrokerName** property is configured by the server; if set to 1, indicates the **SessionBrokerName** property is configured by a group policy.</span></span>

</dd> <dt>

<span data-ttu-id="593ee-122">**SessionBrokerName**</span><span class="sxs-lookup"><span data-stu-id="593ee-122">**SessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="593ee-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="593ee-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="593ee-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="593ee-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="593ee-125">Nome distinto completo del broker di sessione per il server host di virtualizzazione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="593ee-125">The fully qualified distinguished name of the session broker for the RD Virtualization Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="593ee-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="593ee-126">Requirements</span></span>



| <span data-ttu-id="593ee-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="593ee-127">Requirement</span></span> | <span data-ttu-id="593ee-128">Valore</span><span class="sxs-lookup"><span data-stu-id="593ee-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="593ee-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="593ee-129">Minimum supported client</span></span><br/> | <span data-ttu-id="593ee-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="593ee-130">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="593ee-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="593ee-131">Minimum supported server</span></span><br/> | <span data-ttu-id="593ee-132">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="593ee-132">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="593ee-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="593ee-133">Namespace</span></span><br/>                | <span data-ttu-id="593ee-134">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="593ee-134">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="593ee-135">MOF</span><span class="sxs-lookup"><span data-stu-id="593ee-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="593ee-136"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="593ee-136"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="593ee-137">DLL</span><span class="sxs-lookup"><span data-stu-id="593ee-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="593ee-138"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="593ee-138"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





