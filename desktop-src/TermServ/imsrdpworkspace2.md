---
title: Interfaccia IMsRdpWorkspace2
description: Espone un metodo che associa Connessione RemoteApp e desktop credenziali a una connessione.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpWorkspace Servizi Desktop remoto
- Interfaccia IMsRdpWorkspace Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048291"
---
# <a name="imsrdpworkspace2-interface"></a><span data-ttu-id="20efc-105">Interfaccia IMsRdpWorkspace2</span><span class="sxs-lookup"><span data-stu-id="20efc-105">IMsRdpWorkspace2 interface</span></span>

<span data-ttu-id="20efc-106">Espone un metodo che associa Connessione RemoteApp e desktop credenziali a una connessione.</span><span class="sxs-lookup"><span data-stu-id="20efc-106">Exposes a method that associates RemoteApp and Desktop Connection credentials with a connection.</span></span> <span data-ttu-id="20efc-107">Questa interfaccia viene implementata dal controllo Servizi Desktop remoto Accesso Web.</span><span class="sxs-lookup"><span data-stu-id="20efc-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="20efc-108">Questo controllo è un wrapper per il client di Connessione Desktop remoto (MsTscAx.dll) e il proxy di runtime di connessioni RemoteApp e desktop (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="20efc-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="20efc-109">Membri</span><span class="sxs-lookup"><span data-stu-id="20efc-109">Members</span></span>

<span data-ttu-id="20efc-110">L'interfaccia **IMsRdpWorkspace** eredita da [**IMsRdpWorkspace**](imsrdpworkspace.md).</span><span class="sxs-lookup"><span data-stu-id="20efc-110">The **IMsRdpWorkspace** interface inherits from [**IMsRdpWorkspace**](imsrdpworkspace.md).</span></span> <span data-ttu-id="20efc-111">**IMsRdpWorkspace2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="20efc-111">**IMsRdpWorkspace2** also has these types of members:</span></span>

-   [<span data-ttu-id="20efc-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="20efc-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="20efc-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="20efc-113">Methods</span></span>

<span data-ttu-id="20efc-114">L'interfaccia **IMsRdpWorkspace** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="20efc-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="20efc-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="20efc-115">Method</span></span>                                                        | <span data-ttu-id="20efc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20efc-116">Description</span></span>                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="20efc-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20efc-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span></span> | <span data-ttu-id="20efc-118">Associa le credenziali utente e i certificati con un ID connessione.</span><span class="sxs-lookup"><span data-stu-id="20efc-118">Associates user credentials and certificates with a connection ID.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="20efc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20efc-119">Requirements</span></span>



| <span data-ttu-id="20efc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="20efc-120">Requirement</span></span> | <span data-ttu-id="20efc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="20efc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="20efc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20efc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="20efc-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="20efc-123">Windows 8</span></span><br/>                                                                          |
| <span data-ttu-id="20efc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20efc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="20efc-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20efc-125">Windows Server 2012</span></span><br/>                                                                |
| <span data-ttu-id="20efc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="20efc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20efc-127"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20efc-127"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="20efc-128">IID</span><span class="sxs-lookup"><span data-stu-id="20efc-128">IID</span></span><br/>                      | <span data-ttu-id="20efc-129">IID \_ IMsRdpWorkspace2 è definito come 145D0622-04CF-4fc3-A776-A82A9169CDF8</span><span class="sxs-lookup"><span data-stu-id="20efc-129">IID\_IMsRdpWorkspace2 is defined as 145D0622-04CF-4FC3-A776-A82A9169CDF8</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="20efc-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20efc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20efc-131">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="20efc-131">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> <dt>

[<span data-ttu-id="20efc-132">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="20efc-132">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

