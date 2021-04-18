---
title: Interfaccia IMsRdpClientNonScriptable7
description: Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto
- Interfaccia IMsRdpClientNonScriptable7 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "106303652"
---
# <a name="imsrdpclientnonscriptable7-interface"></a><span data-ttu-id="ceb52-106">Interfaccia IMsRdpClientNonScriptable7</span><span class="sxs-lookup"><span data-stu-id="ceb52-106">IMsRdpClientNonScriptable7 interface</span></span>

<span data-ttu-id="ceb52-107">Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ceb52-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="ceb52-108">Deriva dall'interfaccia [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb52-108">Derives from the [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) interface.</span></span> <span data-ttu-id="ceb52-109">È possibile accedere ai metodi di questa interfaccia solo tramite vtable; non sono disponibili per l'uso nei client con script.</span><span class="sxs-lookup"><span data-stu-id="ceb52-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="ceb52-110">Un'istanza di questa interfaccia viene ottenuta chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto [**IMsTscAx**](imstscax-interface.md) , passando l' **IID \_ IMsRdpClientNonScriptable7**.</span><span class="sxs-lookup"><span data-stu-id="ceb52-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable7**.</span></span>

## <a name="members"></a><span data-ttu-id="ceb52-111">Membri</span><span class="sxs-lookup"><span data-stu-id="ceb52-111">Members</span></span>

<span data-ttu-id="ceb52-112">L'interfaccia **IMsRdpClientNonScriptable7** eredita da [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="ceb52-112">The **IMsRdpClientNonScriptable7** interface inherits from [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="ceb52-113">**IMsRdpClientNonScriptable7** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ceb52-113">**IMsRdpClientNonScriptable7** also has these types of members:</span></span>

- [<span data-ttu-id="ceb52-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="ceb52-114">Methods</span></span>](#methods)
- [<span data-ttu-id="ceb52-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ceb52-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ceb52-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="ceb52-116">Methods</span></span>

<span data-ttu-id="ceb52-117">L'interfaccia **IMsRdpClientNonScriptable7** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ceb52-117">The **IMsRdpClientNonScriptable7** interface has these methods.</span></span>


| <span data-ttu-id="ceb52-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="ceb52-118">Method</span></span>            | <span data-ttu-id="ceb52-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceb52-119">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="ceb52-120">**DisableDpiCursorScalingForProcess**</span><span class="sxs-lookup"><span data-stu-id="ceb52-120">**DisableDpiCursorScalingForProcess**</span></span>](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  <span data-ttu-id="ceb52-121">Disabilita la scalabilità locale del cursore del mouse ricevuta dal server, assicurando che la forma del cursore venga sottoposta a rendering correttamente senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="ceb52-121">Disables local scaling of the mouse cursor received from the server, ensuring that the cursor shape is rendered correctly without modification.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="ceb52-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ceb52-122">Properties</span></span>

<span data-ttu-id="ceb52-123">L'interfaccia **IMsRdpClientNonScriptable7** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ceb52-123">The **IMsRdpClientNonScriptable7** interface has these properties.</span></span>

| <span data-ttu-id="ceb52-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ceb52-124">Property</span></span>         | <span data-ttu-id="ceb52-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ceb52-125">Access type</span></span>           | <span data-ttu-id="ceb52-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceb52-126">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="ceb52-127">**CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="ceb52-127">**CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | <span data-ttu-id="ceb52-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb52-128">Read-only</span></span> |  <span data-ttu-id="ceb52-129">Ottiene la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="ceb52-129">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>   |
| [<span data-ttu-id="ceb52-130">**Appunti**</span><span class="sxs-lookup"><span data-stu-id="ceb52-130">**Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)                       | <span data-ttu-id="ceb52-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ceb52-131">Read-only</span></span> |    <span data-ttu-id="ceb52-132">Ottiene il controller degli Appunti utilizzato per sincronizzare gli Appunti locali e remoti se è abilitata la sincronizzazione manuale degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="ceb52-132">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="ceb52-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ceb52-133">Requirements</span></span>

| <span data-ttu-id="ceb52-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceb52-134">Requirement</span></span> | <span data-ttu-id="ceb52-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ceb52-135">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="ceb52-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceb52-136">Minimum supported client</span></span>| <span data-ttu-id="ceb52-137">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="ceb52-137">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="ceb52-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ceb52-138">Type library</span></span>            | <span data-ttu-id="ceb52-139">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ceb52-139">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="ceb52-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ceb52-140">DLL</span></span>                  | <span data-ttu-id="ceb52-141">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ceb52-141">MsTscAx.dll</span></span>     |
| <span data-ttu-id="ceb52-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="ceb52-142">CLSID</span></span>                    | <span data-ttu-id="ceb52-143">CLSID \_ MsRdpClient12 è definito come 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="ceb52-143">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="ceb52-144">CLSID \_ MsRdpClient12NotSafeForScripting è definito come 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="ceb52-144">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="ceb52-145">CLSID \_ MsRdpClient11 è definito come 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="ceb52-145">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="ceb52-146">CLSID \_ MsRdpClient11NotSafeForScripting è definito come 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="ceb52-146">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="ceb52-147">IID</span><span class="sxs-lookup"><span data-stu-id="ceb52-147">IID</span></span>                      | <span data-ttu-id="ceb52-148">IID \_ IMsRdpClientNonScriptable7 è definito come 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="ceb52-148">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>            |

## <a name="see-also"></a><span data-ttu-id="ceb52-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ceb52-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb52-150">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="ceb52-150">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
