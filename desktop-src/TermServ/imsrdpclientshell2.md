---
title: Interfaccia IMsRdpClientShell2
description: Espone le proprietà che avviano il client di Connessione Desktop remoto da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da altri portali Web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740551"
---
# <a name="imsrdpclientshell2-interface"></a><span data-ttu-id="0eb52-105">Interfaccia IMsRdpClientShell2</span><span class="sxs-lookup"><span data-stu-id="0eb52-105">IMsRdpClientShell2 interface</span></span>

<span data-ttu-id="0eb52-106">Espone le proprietà che avviano il client di Connessione Desktop remoto da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da altri portali Web.</span><span class="sxs-lookup"><span data-stu-id="0eb52-106">Exposes properties that launch the Remote Desktop Connection client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

<span data-ttu-id="0eb52-107">Questa interfaccia viene implementata dal controllo Servizi Desktop remoto Accesso Web, che è un wrapper per il client di Connessione Desktop remoto (MsTscAx.dll) e il proxy di runtime delle connessioni RemoteApp e desktop (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="0eb52-107">This interface is implemented by the Remote Desktop Services Web Access Control, which is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="0eb52-108">Membri</span><span class="sxs-lookup"><span data-stu-id="0eb52-108">Members</span></span>

<span data-ttu-id="0eb52-109">L'interfaccia **IMsRdpClientShell2** eredita da **IMsRdpClientShell**.</span><span class="sxs-lookup"><span data-stu-id="0eb52-109">The **IMsRdpClientShell2** interface inherits from **IMsRdpClientShell**.</span></span> <span data-ttu-id="0eb52-110">**IMsRdpClientShell2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0eb52-110">**IMsRdpClientShell2** also has these types of members:</span></span>

-   [<span data-ttu-id="0eb52-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0eb52-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0eb52-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0eb52-112">Properties</span></span>

<span data-ttu-id="0eb52-113">L'interfaccia **IMsRdpClientShell2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0eb52-113">The **IMsRdpClientShell2** interface has these properties.</span></span>



| <span data-ttu-id="0eb52-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0eb52-114">Property</span></span>                                                                               | <span data-ttu-id="0eb52-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="0eb52-115">Access type</span></span>          | <span data-ttu-id="0eb52-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eb52-116">Description</span></span>                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0eb52-117">**MsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="0eb52-117">**MsRdpWorkspace**</span></span>](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | <span data-ttu-id="0eb52-118">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0eb52-118">Read-only</span></span><br/> | <span data-ttu-id="0eb52-119">Recupera un puntatore all'interfaccia [**IMsRdpWorkspace**](imsrdpworkspace.md) , che consente di gestire le credenziali e le connessioni connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="0eb52-119">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span><br/> |
| [<span data-ttu-id="0eb52-120">**SecuredSettingsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0eb52-120">**SecuredSettingsEnabled**</span></span>](imsrdpclientshell2-securedsettingsenabled.md)<br/> | <span data-ttu-id="0eb52-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="0eb52-121">Read-only</span></span><br/> | <span data-ttu-id="0eb52-122">Recupera un valore che indica se la pagina Web corrente si trova in un'area di protezione URL attendibile di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0eb52-122">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span><br/>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="0eb52-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0eb52-123">Requirements</span></span>



| <span data-ttu-id="0eb52-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eb52-124">Requirement</span></span> | <span data-ttu-id="0eb52-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0eb52-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb52-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0eb52-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb52-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0eb52-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0eb52-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0eb52-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb52-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0eb52-129">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="0eb52-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0eb52-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0eb52-131"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0eb52-131"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eb52-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0eb52-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eb52-133">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="0eb52-133">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

 





