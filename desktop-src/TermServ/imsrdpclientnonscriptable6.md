---
title: Interfaccia IMsRdpClientNonScriptable6
description: Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto. Deriva dall'interfaccia IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientNonScriptable6 Servizi Desktop remoto
- Interfaccia IMsRdpClientNonScriptable6 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104401038"
---
# <a name="imsrdpclientnonscriptable6-interface"></a><span data-ttu-id="2219d-106">Interfaccia IMsRdpClientNonScriptable6</span><span class="sxs-lookup"><span data-stu-id="2219d-106">IMsRdpClientNonScriptable6 interface</span></span>

<span data-ttu-id="2219d-107">Fornisce l'accesso alle proprietà non disponibili per lo scripting della sessione remota di un client nel controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2219d-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="2219d-108">Deriva dall'interfaccia [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) .</span><span class="sxs-lookup"><span data-stu-id="2219d-108">Derives from the [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) interface.</span></span> <span data-ttu-id="2219d-109">È possibile accedere ai metodi di questa interfaccia solo tramite vtable; non sono disponibili per l'uso nei client con script.</span><span class="sxs-lookup"><span data-stu-id="2219d-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="2219d-110">Un'istanza di questa interfaccia viene ottenuta chiamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto [**IMsTscAx**](imstscax-interface.md) , passando l' **IID \_ IMsRdpClientNonScriptable6**.</span><span class="sxs-lookup"><span data-stu-id="2219d-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable6**.</span></span>

## <a name="members"></a><span data-ttu-id="2219d-111">Membri</span><span class="sxs-lookup"><span data-stu-id="2219d-111">Members</span></span>

<span data-ttu-id="2219d-112">L'interfaccia **IMsRdpClientNonScriptable6** eredita da [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="2219d-112">The **IMsRdpClientNonScriptable6** interface inherits from [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="2219d-113">**IMsRdpClientNonScriptable6** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2219d-113">**IMsRdpClientNonScriptable6** also has these types of members:</span></span>

- [<span data-ttu-id="2219d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="2219d-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2219d-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="2219d-115">Methods</span></span>

<span data-ttu-id="2219d-116">L'interfaccia **IMsRdpClientNonScriptable6** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2219d-116">The **IMsRdpClientNonScriptable6** interface has these methods.</span></span>


| <span data-ttu-id="2219d-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="2219d-117">Method</span></span>            | <span data-ttu-id="2219d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2219d-118">Description</span></span>                   |
|:-----------------------------|:-----------------|
| [<span data-ttu-id="2219d-119">**SendLocation2D**</span><span class="sxs-lookup"><span data-stu-id="2219d-119">**SendLocation2D**</span></span>](imsrdpclientnonscriptable6-sendlocation2d.md)     |  <span data-ttu-id="2219d-120">Invia un valore di latitudine e longitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="2219d-120">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                   |
| [<span data-ttu-id="2219d-121">**SendLocation3D**</span><span class="sxs-lookup"><span data-stu-id="2219d-121">**SendLocation3D**</span></span>](imsrdpclientnonscriptable6-sendlocation3d.md)     | <span data-ttu-id="2219d-122">Invia un valore di latitudine, Longitudine e altitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="2219d-122">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                 |

## <a name="requirements"></a><span data-ttu-id="2219d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2219d-123">Requirements</span></span>

| <span data-ttu-id="2219d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2219d-124">Requirement</span></span> | <span data-ttu-id="2219d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2219d-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="2219d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2219d-126">Minimum supported client</span></span>| <span data-ttu-id="2219d-127">Windows 10, versione 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="2219d-127">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="2219d-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2219d-128">Type library</span></span>            | <span data-ttu-id="2219d-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="2219d-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="2219d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2219d-130">DLL</span></span>                  | <span data-ttu-id="2219d-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="2219d-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="2219d-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="2219d-132">CLSID</span></span>                    | <span data-ttu-id="2219d-133">CLSID \_ MsRdpClient12 è definito come 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="2219d-133">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="2219d-134">CLSID \_ MsRdpClient12NotSafeForScripting è definito come 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="2219d-134">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="2219d-135">CLSID \_ MsRdpClient11 è definito come 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="2219d-135">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="2219d-136">CLSID \_ MsRdpClient11NotSafeForScripting è definito come 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="2219d-136">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="2219d-137">IID</span><span class="sxs-lookup"><span data-stu-id="2219d-137">IID</span></span>                      | <span data-ttu-id="2219d-138">IID \_ IMsRdpClientNonScriptable6 è definito come 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="2219d-138">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="2219d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2219d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2219d-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2219d-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>
