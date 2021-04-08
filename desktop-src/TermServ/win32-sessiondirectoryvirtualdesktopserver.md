---
title: Classe Win32_SessionDirectoryVirtualDesktopServer
description: Rappresenta un server di Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto) aggiunto a un gestore sessioni.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionDirectoryVirtualDesktopServer Servizi Desktop remoto
- Classe Win32_SessionDirectoryVirtualDesktopServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048082"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a><span data-ttu-id="5220b-105">Win32 \_ SessionDirectoryVirtualDesktopServer (classe)</span><span class="sxs-lookup"><span data-stu-id="5220b-105">Win32\_SessionDirectoryVirtualDesktopServer class</span></span>

<span data-ttu-id="5220b-106">Rappresenta un server di Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto) aggiunto a un gestore sessioni.</span><span class="sxs-lookup"><span data-stu-id="5220b-106">Represents a Remote Desktop Virtualization Host (RD Virtualization Host) server joined to a session broker.</span></span>

<span data-ttu-id="5220b-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5220b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5220b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5220b-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="5220b-109">Members</span><span class="sxs-lookup"><span data-stu-id="5220b-109">Members</span></span>

<span data-ttu-id="5220b-110">La classe **Win32 \_ SessionDirectoryVirtualDesktopServer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5220b-110">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these types of members:</span></span>

-   [<span data-ttu-id="5220b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5220b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5220b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5220b-112">Properties</span></span>

<span data-ttu-id="5220b-113">La classe **Win32 \_ SessionDirectoryVirtualDesktopServer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5220b-113">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5220b-114">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5220b-114">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5220b-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5220b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5220b-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5220b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5220b-117">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5220b-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5220b-118">Nome DNS del server host di virtualizzazione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5220b-118">The DNS name of the RD Virtualization Host server.</span></span> <span data-ttu-id="5220b-119">Il nome assume il formato "*machineName*. *Dominio*. com ".</span><span class="sxs-lookup"><span data-stu-id="5220b-119">This name takes the form "*MachineName*.*Domain*.com".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5220b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5220b-120">Requirements</span></span>



| <span data-ttu-id="5220b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5220b-121">Requirement</span></span> | <span data-ttu-id="5220b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5220b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5220b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5220b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5220b-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5220b-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5220b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5220b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5220b-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5220b-126">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="5220b-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5220b-127">Namespace</span></span><br/>                | <span data-ttu-id="5220b-128">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5220b-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="5220b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="5220b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5220b-130"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5220b-130"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5220b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5220b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5220b-132"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5220b-132"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

