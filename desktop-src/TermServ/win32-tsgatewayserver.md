---
title: Classe Win32_TSGatewayServer
description: Usato per le operazioni specifiche del server Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayServer Servizi Desktop remoto
- Classe Win32_TSGatewayServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476384"
---
# <a name="win32_tsgatewayserver-class"></a><span data-ttu-id="32294-105">Win32 \_ TSGatewayServer (classe)</span><span class="sxs-lookup"><span data-stu-id="32294-105">Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="32294-106">Usato per le operazioni specifiche del server Desktop remoto Gateway (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="32294-106">Used for Remote Desktop Gateway (RD Gateway) server-specific operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="32294-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32294-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a><span data-ttu-id="32294-108">Members</span><span class="sxs-lookup"><span data-stu-id="32294-108">Members</span></span>

<span data-ttu-id="32294-109">La classe **Win32 \_ TSGatewayServer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="32294-109">The **Win32\_TSGatewayServer** class has these types of members:</span></span>

-   [<span data-ttu-id="32294-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="32294-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="32294-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="32294-111">Methods</span></span>

<span data-ttu-id="32294-112">La classe **Win32 \_ TSGatewayServer** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="32294-112">The **Win32\_TSGatewayServer** class has these methods.</span></span>



| <span data-ttu-id="32294-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="32294-113">Method</span></span>                                                                                   | <span data-ttu-id="32294-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32294-114">Description</span></span>                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32294-115">**CreateSelfSignedCertificate**</span><span class="sxs-lookup"><span data-stu-id="32294-115">**CreateSelfSignedCertificate**</span></span>](createselfsignedcertificate-win32-tsgatewayserver.md) | <span data-ttu-id="32294-116">Crea un certificato autofirmato con un nome oggetto specificato e restituisce l'hash del certificato come parametro "out".</span><span class="sxs-lookup"><span data-stu-id="32294-116">Creates a self-signed certificate with a given subject name and returns the certificate hash as an "out" parameter.</span></span><br/> |
| [<span data-ttu-id="32294-117">**Esportazione**</span><span class="sxs-lookup"><span data-stu-id="32294-117">**Export**</span></span>](export-win32-tsgatewayserver.md)                                           | <span data-ttu-id="32294-118">Restituisce la configurazione del server Gateway Desktop remoto come stringa XML.</span><span class="sxs-lookup"><span data-stu-id="32294-118">Returns the RD Gateway server configuration as an XML string.</span></span><br/>                                                       |
| [<span data-ttu-id="32294-119">**Importa**</span><span class="sxs-lookup"><span data-stu-id="32294-119">**Import**</span></span>](import-win32-tsgatewayserver.md)                                           | <span data-ttu-id="32294-120">Importa una determinata configurazione nel server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="32294-120">Imports a given configuration to the RD Gateway server.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="32294-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="32294-121">Remarks</span></span>

<span data-ttu-id="32294-122">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="32294-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="32294-123">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="32294-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="32294-124">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="32294-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="32294-125">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="32294-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="32294-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32294-126">Requirements</span></span>



| <span data-ttu-id="32294-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="32294-127">Requirement</span></span> | <span data-ttu-id="32294-128">Valore</span><span class="sxs-lookup"><span data-stu-id="32294-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32294-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32294-129">Minimum supported client</span></span><br/> | <span data-ttu-id="32294-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="32294-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="32294-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32294-131">Minimum supported server</span></span><br/> | <span data-ttu-id="32294-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32294-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="32294-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="32294-133">Namespace</span></span><br/>                | <span data-ttu-id="32294-134">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="32294-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="32294-135">MOF</span><span class="sxs-lookup"><span data-stu-id="32294-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32294-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32294-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="32294-137">DLL</span><span class="sxs-lookup"><span data-stu-id="32294-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32294-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32294-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



 

