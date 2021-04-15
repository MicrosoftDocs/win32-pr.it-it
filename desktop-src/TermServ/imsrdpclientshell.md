---
title: Interfaccia IMsRdpClientShell
description: Impostazioni client di Connessione Desktop remoto (RDC) utilizzate per avviare il client da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da altri portali Web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientShell Servizi Desktop remoto
- Interfaccia IMsRdpClientShell Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477758"
---
# <a name="imsrdpclientshell-interface"></a><span data-ttu-id="f6509-105">Interfaccia IMsRdpClientShell</span><span class="sxs-lookup"><span data-stu-id="f6509-105">IMsRdpClientShell interface</span></span>

<span data-ttu-id="f6509-106">Impostazioni client di Connessione Desktop remoto (RDC) utilizzate per avviare il client da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da altri portali Web.</span><span class="sxs-lookup"><span data-stu-id="f6509-106">Remote Desktop Connection (RDC) client settings that are used to launch the client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

## <a name="members"></a><span data-ttu-id="f6509-107">Membri</span><span class="sxs-lookup"><span data-stu-id="f6509-107">Members</span></span>

<span data-ttu-id="f6509-108">L'interfaccia **IMsRdpClientShell** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="f6509-108">The **IMsRdpClientShell** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f6509-109">**IMsRdpClientShell** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f6509-109">**IMsRdpClientShell** also has these types of members:</span></span>

-   [<span data-ttu-id="f6509-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="f6509-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6509-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6509-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6509-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="f6509-112">Methods</span></span>

<span data-ttu-id="f6509-113">L'interfaccia **IMsRdpClientShell** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f6509-113">The **IMsRdpClientShell** interface has these methods.</span></span>



| <span data-ttu-id="f6509-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="f6509-114">Method</span></span>                                                     | <span data-ttu-id="f6509-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6509-115">Description</span></span>                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="f6509-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6509-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span></span> | <span data-ttu-id="f6509-117">Recupera una singola proprietà RDP.</span><span class="sxs-lookup"><span data-stu-id="f6509-117">Retrieves a single RDP property.</span></span><br/>                  |
| [<span data-ttu-id="f6509-118">**Launch**</span><span class="sxs-lookup"><span data-stu-id="f6509-118">**Launch**</span></span>](imsrdpclientshell-launch.md)                 | <span data-ttu-id="f6509-119">Avvia il contenuto del file remoto dal portale Web.</span><span class="sxs-lookup"><span data-stu-id="f6509-119">Launches remote file content from the web portal.</span></span><br/> |
| <span data-ttu-id="f6509-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6509-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span></span> | <span data-ttu-id="f6509-121">Imposta una singola proprietà RDP.</span><span class="sxs-lookup"><span data-stu-id="f6509-121">Sets a single RDP property.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="f6509-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6509-122">Properties</span></span>

<span data-ttu-id="f6509-123">L'interfaccia **IMsRdpClientShell** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f6509-123">The **IMsRdpClientShell** interface has these properties.</span></span>



| <span data-ttu-id="f6509-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6509-124">Property</span></span>                                                                                              | <span data-ttu-id="f6509-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="f6509-125">Access type</span></span>           | <span data-ttu-id="f6509-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6509-126">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6509-127">**IsRemoteProgramClientInstalled**</span><span class="sxs-lookup"><span data-stu-id="f6509-127">**IsRemoteProgramClientInstalled**</span></span>](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | <span data-ttu-id="f6509-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6509-128">Read-only</span></span><br/>  | <span data-ttu-id="f6509-129">Recupera un valore che indica se il client di Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f6509-129">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span><br/> |
| [<span data-ttu-id="f6509-130">**PublicMode**</span><span class="sxs-lookup"><span data-stu-id="f6509-130">**PublicMode**</span></span>](imsrdpclientshell-publicmode.md)<br/>                                         | <span data-ttu-id="f6509-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="f6509-131">Read/write</span></span><br/> | <span data-ttu-id="f6509-132">Recupera un valore che indica se è attivata la modalità pubblica.</span><span class="sxs-lookup"><span data-stu-id="f6509-132">Retrieves whether public mode is enabled.</span></span><br/>                                                      |
| [<span data-ttu-id="f6509-133">**RdpFileContents**</span><span class="sxs-lookup"><span data-stu-id="f6509-133">**RdpFileContents**</span></span>](imsrdpclientshell-rdpfilecontents.md)<br/>                               | <span data-ttu-id="f6509-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="f6509-134">Read/write</span></span><br/> | <span data-ttu-id="f6509-135">Versione del flusso del file di configurazione RDP.</span><span class="sxs-lookup"><span data-stu-id="f6509-135">Stream version of the RDP configuration file.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="f6509-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6509-136">Requirements</span></span>



| <span data-ttu-id="f6509-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6509-137">Requirement</span></span> | <span data-ttu-id="f6509-138">Valore</span><span class="sxs-lookup"><span data-stu-id="f6509-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6509-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6509-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f6509-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6509-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f6509-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6509-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f6509-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6509-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f6509-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f6509-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6509-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6509-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6509-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f6509-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6509-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6509-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6509-147">IID</span><span class="sxs-lookup"><span data-stu-id="f6509-147">IID</span></span><br/>                      | <span data-ttu-id="f6509-148">IID \_ IMsRdpClientShell è definito come d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="f6509-148">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f6509-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6509-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6509-150">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="f6509-150">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="f6509-151">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="f6509-151">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

