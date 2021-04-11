---
title: Interfacce di runtime Connessione RemoteApp e desktop
description: Supporta le interfacce che consentono lo sviluppo di client personalizzati in Connessione RemoteApp e desktop.
ms.assetid: 4580df05-5e44-40d0-8765-5d9b4e1d339e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, informazioni di riferimento sull'API di runtime Connessione RemoteApp e desktop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6b7c3c2fd3841cfe797fc559ba1aa30d3479436
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117057"
---
# <a name="remoteapp-and-desktop-connection-runtime-interfaces"></a><span data-ttu-id="69a1c-104">Interfacce di runtime Connessione RemoteApp e desktop</span><span class="sxs-lookup"><span data-stu-id="69a1c-104">RemoteApp and Desktop Connection Runtime interfaces</span></span>

<span data-ttu-id="69a1c-105">L'API di runtime Connessione RemoteApp e desktop supporta le interfacce che consentono lo sviluppo di client personalizzati in Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-105">The RemoteApp and Desktop Connection Runtime API supports interfaces that allow the development of custom clients in RemoteApp and Desktop Connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69a1c-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="69a1c-106">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="69a1c-107">**IWorkspace**</span><span class="sxs-lookup"><span data-stu-id="69a1c-107">**IWorkspace**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace)
</dt> <dd>

<span data-ttu-id="69a1c-108">Espone metodi che forniscono informazioni su una connessione in Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-108">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-109">**IWorkspace2**</span><span class="sxs-lookup"><span data-stu-id="69a1c-109">**IWorkspace2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2)
</dt> <dd>

<span data-ttu-id="69a1c-110">Espone metodi aggiuntivi che forniscono informazioni su una connessione in Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-110">Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-111">**IWorkspace3**</span><span class="sxs-lookup"><span data-stu-id="69a1c-111">**IWorkspace3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3)
</dt> <dd>

<span data-ttu-id="69a1c-112">Espone metodi che forniscono informazioni su una connessione in Connessione RemoteApp e desktop e aggiunge la possibilità di recuperare o impostare un token di attestazione.</span><span class="sxs-lookup"><span data-stu-id="69a1c-112">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-113">**IWorkspaceClientExt**</span><span class="sxs-lookup"><span data-stu-id="69a1c-113">**IWorkspaceClientExt**</span></span>](/windows/desktop/api/Workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext)
</dt> <dd>

<span data-ttu-id="69a1c-114">Espone metodi che consentono al runtime di disconnettere un client personalizzato in Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-114">Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-115">**IWorkspaceRegistration**</span><span class="sxs-lookup"><span data-stu-id="69a1c-115">**IWorkspaceRegistration**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration)
</dt> <dd>

<span data-ttu-id="69a1c-116">Espone metodi che aggiungono e rimuovono i riferimenti ai client personalizzati in Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-116">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-117">**IWorkspaceRegistration2**</span><span class="sxs-lookup"><span data-stu-id="69a1c-117">**IWorkspaceRegistration2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2)
</dt> <dd>

<span data-ttu-id="69a1c-118">Espone metodi che aggiungono e rimuovono i riferimenti ai client personalizzati in Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-118">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-119">**IWorkspaceReportMessage**</span><span class="sxs-lookup"><span data-stu-id="69a1c-119">**IWorkspaceReportMessage**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage)
</dt> <dd>

<span data-ttu-id="69a1c-120">Espone metodi che supportano la gestione dei messaggi di errore per le aree di lavoro remote.</span><span class="sxs-lookup"><span data-stu-id="69a1c-120">Exposes methods that support error message handling for remote workspaces.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-121">**IWorkspaceResTypeRegistry**</span><span class="sxs-lookup"><span data-stu-id="69a1c-121">**IWorkspaceResTypeRegistry**</span></span>](/windows/desktop/api/Workspaceax/nn-workspaceax-iworkspacerestyperegistry)
</dt> <dd>

<span data-ttu-id="69a1c-122">Espone metodi che consentono a un plug-in di gestire le estensioni di file di terze parti in Connessione RemoteApp e desktop Runtime.</span><span class="sxs-lookup"><span data-stu-id="69a1c-122">Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-123">**IWorkspaceScriptable**</span><span class="sxs-lookup"><span data-stu-id="69a1c-123">**IWorkspaceScriptable**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable)
</dt> <dd>

<span data-ttu-id="69a1c-124">Espone metodi che gestiscono le credenziali e le connessioni Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-124">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-125">**IWorkspaceScriptable2**</span><span class="sxs-lookup"><span data-stu-id="69a1c-125">**IWorkspaceScriptable2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2)
</dt> <dd>

<span data-ttu-id="69a1c-126">Espone metodi che gestiscono le credenziali e le connessioni Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-126">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="69a1c-127">**IWorkspaceScriptable3**</span><span class="sxs-lookup"><span data-stu-id="69a1c-127">**IWorkspaceScriptable3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3)
</dt> <dd>

<span data-ttu-id="69a1c-128">Espone metodi che gestiscono le credenziali e le connessioni Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="69a1c-128">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> </dl>

 

 




