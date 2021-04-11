---
title: Interfaccia IMsRdpWorkspace
description: Espone metodi che gestiscono le credenziali e le connessioni Connessione RemoteApp e desktop.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
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
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963842"
---
# <a name="imsrdpworkspace-interface"></a><span data-ttu-id="9cfbc-105">Interfaccia IMsRdpWorkspace</span><span class="sxs-lookup"><span data-stu-id="9cfbc-105">IMsRdpWorkspace interface</span></span>

<span data-ttu-id="9cfbc-106">Espone metodi che gestiscono le credenziali e le connessioni Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-106">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span> <span data-ttu-id="9cfbc-107">Questa interfaccia viene implementata dal controllo Servizi Desktop remoto Accesso Web.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="9cfbc-108">Questo controllo è un wrapper per il client di Connessione Desktop remoto (MsTscAx.dll) e il proxy di runtime di connessioni RemoteApp e desktop (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="9cfbc-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="9cfbc-109">Membri</span><span class="sxs-lookup"><span data-stu-id="9cfbc-109">Members</span></span>

<span data-ttu-id="9cfbc-110">L'interfaccia **IMsRdpWorkspace** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="9cfbc-110">The **IMsRdpWorkspace** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9cfbc-111">**IMsRdpWorkspace** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9cfbc-111">**IMsRdpWorkspace** also has these types of members:</span></span>

-   [<span data-ttu-id="9cfbc-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="9cfbc-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9cfbc-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="9cfbc-113">Methods</span></span>

<span data-ttu-id="9cfbc-114">L'interfaccia **IMsRdpWorkspace** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="9cfbc-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="9cfbc-115">Method</span></span>                                                                                   | <span data-ttu-id="9cfbc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cfbc-116">Description</span></span>                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cfbc-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cfbc-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span></span>             | <span data-ttu-id="9cfbc-118">Elimina le credenziali utente associate all'ID di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-118">Deletes the user credentials associated with the specified connection ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="9cfbc-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cfbc-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span></span>                       | <span data-ttu-id="9cfbc-120">Disconnette tutte le connessioni esistenti associate all'ID di connessione specificato ed Elimina le credenziali utente corrispondenti dall'archivio delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-120">Disconnects all existing connections associated with the specified connection ID and deletes the corresponding user credentials from the credential store.</span></span><br/> |
| <span data-ttu-id="9cfbc-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cfbc-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span></span> | <span data-ttu-id="9cfbc-122">Determina se esistono credenziali utente per l'ID di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-122">Determines whether user credentials exist for the specified connection ID.</span></span><br/>                                                                                 |
| <span data-ttu-id="9cfbc-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cfbc-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span></span>                   | <span data-ttu-id="9cfbc-124">Determina se Single Sign-on (SSO) è abilitato per Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-124">Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.</span></span><br/>                                                                   |
| <span data-ttu-id="9cfbc-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cfbc-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span></span>                               | <span data-ttu-id="9cfbc-126">Contrassegna l'autenticazione delle credenziali utente per l'ID connessione e successivamente Visualizza la notifica di connessione nell'area di notifica della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-126">Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.</span></span> <br/>     |
| <span data-ttu-id="9cfbc-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cfbc-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span></span>                                 | <span data-ttu-id="9cfbc-128">Associa le credenziali utente e i certificati con un ID connessione.</span><span class="sxs-lookup"><span data-stu-id="9cfbc-128">Associates user credentials and certificates with a connection ID.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="9cfbc-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cfbc-129">Requirements</span></span>



| <span data-ttu-id="9cfbc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cfbc-130">Requirement</span></span> | <span data-ttu-id="9cfbc-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9cfbc-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cfbc-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cfbc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9cfbc-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfbc-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9cfbc-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cfbc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9cfbc-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9cfbc-135">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="9cfbc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9cfbc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cfbc-137"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cfbc-137"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="9cfbc-138">IID</span><span class="sxs-lookup"><span data-stu-id="9cfbc-138">IID</span></span><br/>                      | <span data-ttu-id="9cfbc-139">IID \_ IMsRdpWorkspace è definito come 145D0621-04CF-4FC2-A766-A81A9069CDF8</span><span class="sxs-lookup"><span data-stu-id="9cfbc-139">IID\_IMsRdpWorkspace is defined as 145D0621-04CF-4FC2-A766-A81A9069CDF8</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9cfbc-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cfbc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cfbc-141">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="9cfbc-141">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

