---
title: Interfaccia IMsRdpPreferredRedirectionInfo
description: Fornisce una proprietà da controllare utilizzando un server di reindirizzamento.
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpPreferredRedirectionInfo Servizi Desktop remoto
- Interfaccia IMsRdpPreferredRedirectionInfo Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475617"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a><span data-ttu-id="240cc-105">Interfaccia IMsRdpPreferredRedirectionInfo</span><span class="sxs-lookup"><span data-stu-id="240cc-105">IMsRdpPreferredRedirectionInfo interface</span></span>

<span data-ttu-id="240cc-106">Fornisce una proprietà da controllare utilizzando un server di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="240cc-106">Provides a property to control using a redirection server.</span></span>

## <a name="members"></a><span data-ttu-id="240cc-107">Membri</span><span class="sxs-lookup"><span data-stu-id="240cc-107">Members</span></span>

<span data-ttu-id="240cc-108">L'interfaccia **IMsRdpPreferredRedirectionInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="240cc-108">The **IMsRdpPreferredRedirectionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="240cc-109">**IMsRdpPreferredRedirectionInfo** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="240cc-109">**IMsRdpPreferredRedirectionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="240cc-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="240cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="240cc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="240cc-111">Properties</span></span>

<span data-ttu-id="240cc-112">L'interfaccia **IMsRdpPreferredRedirectionInfo** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="240cc-112">The **IMsRdpPreferredRedirectionInfo** interface has these properties.</span></span>



| <span data-ttu-id="240cc-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="240cc-113">Property</span></span>                                                                                               | <span data-ttu-id="240cc-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="240cc-114">Access type</span></span>           | <span data-ttu-id="240cc-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="240cc-115">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="240cc-116">**UseRedirectionServerName**</span><span class="sxs-lookup"><span data-stu-id="240cc-116">**UseRedirectionServerName**</span></span>](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | <span data-ttu-id="240cc-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="240cc-117">Read/write</span></span><br/> | <span data-ttu-id="240cc-118">Ottiene e imposta un valore che indica se utilizzare il nome del server di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="240cc-118">Gets and sets whether to use the redirection server name.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="240cc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="240cc-119">Requirements</span></span>



| <span data-ttu-id="240cc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="240cc-120">Requirement</span></span> | <span data-ttu-id="240cc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="240cc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="240cc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="240cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="240cc-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="240cc-123">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="240cc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="240cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="240cc-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="240cc-125">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="240cc-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="240cc-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="240cc-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="240cc-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="240cc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="240cc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="240cc-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="240cc-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="240cc-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="240cc-130">CLSID</span></span><br/>                    | <span data-ttu-id="240cc-131">CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span><span class="sxs-lookup"><span data-stu-id="240cc-131">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="240cc-132">CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4ab4-907c-34905D770C7D</span><span class="sxs-lookup"><span data-stu-id="240cc-132">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="240cc-133">CLSID \_ MsRdpClient7 è definito come A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="240cc-133">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="240cc-134">CLSID \_ MsRdpClient7NotSafeForScripting è definito come 54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="240cc-134">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="240cc-135">CLSID \_ MsRdpClient8 è definito come 5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="240cc-135">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="240cc-136">CLSID \_ MsRdpClient8NotSafeForScripting è definito come A3BC03A0-041d-42e3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="240cc-136">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="240cc-137">CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="240cc-137">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="240cc-138">CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="240cc-138">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="240cc-139">IID</span><span class="sxs-lookup"><span data-stu-id="240cc-139">IID</span></span><br/>                      | <span data-ttu-id="240cc-140">IID \_ IMsRdpPreferredRedirectionInfo è definito come FDD029F9-9574-4def-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="240cc-140">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

