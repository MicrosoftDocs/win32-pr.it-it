---
title: Interfaccia ITSRemoteProgram
description: Include metodi per impostare e recuperare la modalità RemoteApp e i parametri di avvio per un programma RemoteApp, ad esempio il percorso del file eseguibile e la directory di lavoro.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Interfaccia ITSRemoteProgram Servizi Desktop remoto
- Interfaccia ITSRemoteProgram Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048505"
---
# <a name="itsremoteprogram-interface"></a><span data-ttu-id="a6856-105">Interfaccia ITSRemoteProgram</span><span class="sxs-lookup"><span data-stu-id="a6856-105">ITSRemoteProgram interface</span></span>

<span data-ttu-id="a6856-106">Include metodi per impostare e recuperare la modalità RemoteApp e i parametri di avvio per un programma RemoteApp, ad esempio il percorso del file eseguibile e la directory di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a6856-106">Includes methods to set and retrieve the RemoteApp mode and the start-up parameters for a RemoteApp program, such as the path of the executable file and the working directory.</span></span>

## <a name="members"></a><span data-ttu-id="a6856-107">Membri</span><span class="sxs-lookup"><span data-stu-id="a6856-107">Members</span></span>

<span data-ttu-id="a6856-108">L'interfaccia **ITSRemoteProgram** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a6856-108">The **ITSRemoteProgram** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a6856-109">**ITSRemoteProgram** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a6856-109">**ITSRemoteProgram** also has these types of members:</span></span>

-   [<span data-ttu-id="a6856-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6856-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a6856-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6856-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a6856-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6856-112">Methods</span></span>

<span data-ttu-id="a6856-113">L'interfaccia **ITSRemoteProgram** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a6856-113">The **ITSRemoteProgram** interface has these methods.</span></span>



| <span data-ttu-id="a6856-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="a6856-114">Method</span></span>                                                            | <span data-ttu-id="a6856-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6856-115">Description</span></span>                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="a6856-116">**ServerStartProgram**</span><span class="sxs-lookup"><span data-stu-id="a6856-116">**ServerStartProgram**</span></span>](itsremoteprogram-serverstartprogram.md) | <span data-ttu-id="a6856-117">Specifica un programma RemoteApp da avviare nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="a6856-117">Specifies a RemoteApp program to start in the remote session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a6856-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6856-118">Properties</span></span>

<span data-ttu-id="a6856-119">L'interfaccia **ITSRemoteProgram** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a6856-119">The **ITSRemoteProgram** interface has these properties.</span></span>



| <span data-ttu-id="a6856-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6856-120">Property</span></span>                                                                   | <span data-ttu-id="a6856-121">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a6856-121">Access type</span></span>           | <span data-ttu-id="a6856-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6856-122">Description</span></span>                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [<span data-ttu-id="a6856-123">**RemoteProgramMode**</span><span class="sxs-lookup"><span data-stu-id="a6856-123">**RemoteProgramMode**</span></span>](itsremoteprogram-remoteprogrammode.md)<br/> | <span data-ttu-id="a6856-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a6856-124">Read/write</span></span><br/> | <span data-ttu-id="a6856-125">Modalità RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="a6856-125">The RemoteApp mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a6856-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6856-126">Requirements</span></span>



| <span data-ttu-id="a6856-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6856-127">Requirement</span></span> | <span data-ttu-id="a6856-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a6856-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6856-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6856-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a6856-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6856-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a6856-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6856-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a6856-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6856-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a6856-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a6856-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="a6856-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6856-134"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6856-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a6856-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6856-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6856-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6856-137">IID</span><span class="sxs-lookup"><span data-stu-id="a6856-137">IID</span></span><br/>                      | <span data-ttu-id="a6856-138">IID \_ ITSRemoteProgram è definito come FDD029F9-467a-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="a6856-138">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="a6856-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6856-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6856-140">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a6856-140">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="a6856-141">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="a6856-141">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

