---
description: L'interfaccia IWiaDevMgr2 viene usata per creare e gestire i dispositivi di acquisizione di immagini e per eseguire la registrazione per ricevere eventi del dispositivo.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Interfaccia IWiaDevMgr2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881890"
---
# <a name="iwiadevmgr2-interface"></a><span data-ttu-id="84eaa-103">Interfaccia IWiaDevMgr2</span><span class="sxs-lookup"><span data-stu-id="84eaa-103">IWiaDevMgr2 interface</span></span>

<span data-ttu-id="84eaa-104">L'interfaccia **IWiaDevMgr2** viene usata per creare e gestire i dispositivi di acquisizione di immagini e per eseguire la registrazione per ricevere eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84eaa-104">The **IWiaDevMgr2** interface is used to create and manage image acquisition devices and to register to receive device events.</span></span>

## <a name="members"></a><span data-ttu-id="84eaa-105">Membri</span><span class="sxs-lookup"><span data-stu-id="84eaa-105">Members</span></span>

<span data-ttu-id="84eaa-106">L'interfaccia **IWiaDevMgr2** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="84eaa-106">The **IWiaDevMgr2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="84eaa-107">**IWiaDevMgr2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84eaa-107">**IWiaDevMgr2** also has these types of members:</span></span>

-   [<span data-ttu-id="84eaa-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="84eaa-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="84eaa-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="84eaa-109">Methods</span></span>

<span data-ttu-id="84eaa-110">L'interfaccia **IWiaDevMgr2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="84eaa-110">The **IWiaDevMgr2** interface has these methods.</span></span>



| <span data-ttu-id="84eaa-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="84eaa-111">Method</span></span>                                                                                    | <span data-ttu-id="84eaa-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84eaa-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84eaa-113">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="84eaa-113">**CreateDevice**</span></span>](-wia-iwiadevmgr2-createdevice.md)                                     | <span data-ttu-id="84eaa-114">Crea un albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) per un dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="84eaa-114">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="84eaa-115">**EnumDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="84eaa-115">**EnumDeviceInfo**</span></span>](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | <span data-ttu-id="84eaa-116">Crea un enumeratore di informazioni sulle proprietà per ogni dispositivo WIA 2,0 disponibile.</span><span class="sxs-lookup"><span data-stu-id="84eaa-116">Creates an enumerator of property information for each available WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="84eaa-117">**GetImageDlg**</span><span class="sxs-lookup"><span data-stu-id="84eaa-117">**GetImageDlg**</span></span>](-wia-iwiadevmgr2-getimagedlg.md)                                       | <span data-ttu-id="84eaa-118">Il metodo [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) Visualizza una o più finestre di dialogo che consentono a un utente di acquisire un'immagine da un dispositivo WIA 2,0 e scrivere l'immagine in un file specificato.</span><span class="sxs-lookup"><span data-stu-id="84eaa-118">The [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method displays one or more dialog boxes that enable a user to acquire an image from a WIA 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="84eaa-119">Questo metodo estende la funzionalità di [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) per incapsulare l'acquisizione di immagini in una singola chiamata API.</span><span class="sxs-lookup"><span data-stu-id="84eaa-119">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span> <br/> |
| [<span data-ttu-id="84eaa-120">**RegisterEventCallbackCLSID**</span><span class="sxs-lookup"><span data-stu-id="84eaa-120">**RegisterEventCallbackCLSID**</span></span>](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | <span data-ttu-id="84eaa-121">Il metodo [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) registra un'applicazione per ricevere eventi anche se l'applicazione non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84eaa-121">The [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) method registers an application to receive events even if the application is not running.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="84eaa-122">**RegisterEventCallbackInterface**</span><span class="sxs-lookup"><span data-stu-id="84eaa-122">**RegisterEventCallbackInterface**</span></span>](-wia-iwiadevmgr2-registereventcallbackinterface.md) | <span data-ttu-id="84eaa-123">Registra un'applicazione in esecuzione per la notifica degli eventi WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="84eaa-123">Registers a running application for WIA 2.0 event notification.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="84eaa-124">**RegisterEventCallbackProgram**</span><span class="sxs-lookup"><span data-stu-id="84eaa-124">**RegisterEventCallbackProgram**</span></span>](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | <span data-ttu-id="84eaa-125">Il metodo [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) registra un'applicazione per la ricezione di eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84eaa-125">The [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method registers an application to receive device events.</span></span> <span data-ttu-id="84eaa-126">Viene fornita principalmente per garantire la compatibilità con le applicazioni che non sono state scritte per WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="84eaa-126">It is primarily provided for backward compatibility with applications that were not written for WIA 2.0.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="84eaa-127">**SelectDeviceDlg**</span><span class="sxs-lookup"><span data-stu-id="84eaa-127">**SelectDeviceDlg**</span></span>](-wia-iwiadevmgr2-selectdevicedlg.md)                               | <span data-ttu-id="84eaa-128">Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="84eaa-128">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="84eaa-129">**SelectDeviceDlgID**</span><span class="sxs-lookup"><span data-stu-id="84eaa-129">**SelectDeviceDlgID**</span></span>](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | <span data-ttu-id="84eaa-130">Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="84eaa-130">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="84eaa-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="84eaa-131">Remarks</span></span>

<span data-ttu-id="84eaa-132">L'interfaccia **IWiaDevMgr2** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="84eaa-132">The **IWiaDevMgr2** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="84eaa-133">Metodi IUnknown</span><span class="sxs-lookup"><span data-stu-id="84eaa-133">IUnknown Methods</span></span>                                        | <span data-ttu-id="84eaa-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84eaa-134">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="84eaa-135">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="84eaa-135">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="84eaa-136">Restituisce puntatori alle interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="84eaa-136">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="84eaa-137">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="84eaa-137">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="84eaa-138">Incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="84eaa-138">Increments reference count.</span></span>               |
| [<span data-ttu-id="84eaa-139">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="84eaa-139">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="84eaa-140">Riduce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="84eaa-140">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="84eaa-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84eaa-141">Requirements</span></span>



| <span data-ttu-id="84eaa-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="84eaa-142">Requirement</span></span> | <span data-ttu-id="84eaa-143">Valore</span><span class="sxs-lookup"><span data-stu-id="84eaa-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84eaa-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84eaa-144">Minimum supported client</span></span><br/> | <span data-ttu-id="84eaa-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84eaa-145">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="84eaa-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84eaa-146">Minimum supported server</span></span><br/> | <span data-ttu-id="84eaa-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84eaa-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="84eaa-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84eaa-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="84eaa-149"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="84eaa-149"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="84eaa-150">IDL</span><span class="sxs-lookup"><span data-stu-id="84eaa-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84eaa-151"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84eaa-151"><dt>Wia.idl</dt></span></span> </dl> |



 

 
