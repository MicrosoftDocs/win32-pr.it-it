---
description: Estende l'oggetto IShellDispatch con un'ampia gamma di nuove funzionalità.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Oggetto IShellDispatch2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978031"
---
# <a name="ishelldispatch2-object"></a><span data-ttu-id="5a1d5-103">Oggetto IShellDispatch2</span><span class="sxs-lookup"><span data-stu-id="5a1d5-103">IShellDispatch2 object</span></span>

<span data-ttu-id="5a1d5-104">Estende l'oggetto [**IShellDispatch**](ishelldispatch.md) con un'ampia gamma di nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-104">Extends the [**IShellDispatch**](ishelldispatch.md) object with a variety of new functionality.</span></span>

> [!Note]  
> <span data-ttu-id="5a1d5-105">**IShellDispatch2** viene implementato e accessibile tramite l'oggetto [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="5a1d5-105">**IShellDispatch2** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="5a1d5-106">Membri</span><span class="sxs-lookup"><span data-stu-id="5a1d5-106">Members</span></span>

<span data-ttu-id="5a1d5-107">L'oggetto **IShellDispatch2** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5a1d5-107">The **IShellDispatch2** object has these types of members:</span></span>

-   [<span data-ttu-id="5a1d5-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="5a1d5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a1d5-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="5a1d5-109">Methods</span></span>

<span data-ttu-id="5a1d5-110">L'oggetto **IShellDispatch2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-110">The **IShellDispatch2** object has these methods.</span></span>



| <span data-ttu-id="5a1d5-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="5a1d5-111">Method</span></span>                                                               | <span data-ttu-id="5a1d5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a1d5-112">Description</span></span>                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="5a1d5-113">**CanStartStopService**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-113">**CanStartStopService**</span></span>](ishelldispatch2-canstartstopservice.md)   | <span data-ttu-id="5a1d5-114">Determina se l'utente corrente può avviare e arrestare il servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-114">Determines if the current user can start and stop the named service.</span></span><br/>    |
| [<span data-ttu-id="5a1d5-115">**FindPrinter**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-115">**FindPrinter**</span></span>](ishelldispatch2-findprinter.md)                   | <span data-ttu-id="5a1d5-116">Consente di visualizzare la finestra di dialogo **Trova stampante** .</span><span class="sxs-lookup"><span data-stu-id="5a1d5-116">Displays the **Find Printer** dialog box.</span></span><br/>                               |
| [<span data-ttu-id="5a1d5-117">**GetSystemInformation**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-117">**GetSystemInformation**</span></span>](ishelldispatch2-getsysteminformation.md) | <span data-ttu-id="5a1d5-118">Recupera le informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-118">Retrieves system information.</span></span><br/>                                           |
| [<span data-ttu-id="5a1d5-119">**IsRestricted**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-119">**IsRestricted**</span></span>](ishelldispatch2-isrestricted.md)                 | <span data-ttu-id="5a1d5-120">Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-120">Retrieves a group's restriction setting from the registry.</span></span><br/>              |
| [<span data-ttu-id="5a1d5-121">**IsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-121">**IsServiceRunning**</span></span>](ishelldispatch2-isservicerunning.md)         | <span data-ttu-id="5a1d5-122">Restituisce un valore che indica se un particolare servizio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-122">Returns a value that indicates whether a particular service is running.</span></span><br/> |
| [<span data-ttu-id="5a1d5-123">**ServiceStart**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-123">**ServiceStart**</span></span>](ishelldispatch2-servicestart.md)                 | <span data-ttu-id="5a1d5-124">Avvia un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-124">Starts a named service.</span></span><br/>                                                 |
| [<span data-ttu-id="5a1d5-125">**ServiceStop**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-125">**ServiceStop**</span></span>](ishelldispatch2-servicestop.md)                   | <span data-ttu-id="5a1d5-126">Arresta un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-126">Stops a named service.</span></span><br/>                                                  |
| [<span data-ttu-id="5a1d5-127">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-127">**ShellExecute**</span></span>](ishelldispatch2-shellexecute.md)                 | <span data-ttu-id="5a1d5-128">Esegue un'operazione specificata su un file specificato.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-128">Performs a specified operation on a specified file.</span></span><br/>                     |
| [<span data-ttu-id="5a1d5-129">**ShowBrowserBar**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-129">**ShowBrowserBar**</span></span>](ishelldispatch2-showbrowserbar.md)             | <span data-ttu-id="5a1d5-130">Visualizza una barra del browser.</span><span class="sxs-lookup"><span data-stu-id="5a1d5-130">Displays a browser bar.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5a1d5-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a1d5-131">Remarks</span></span>

<span data-ttu-id="5a1d5-132">Per informazioni sui servizi Windows, vedere la documentazione relativa ai [Servizi](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="5a1d5-132">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a1d5-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a1d5-133">Requirements</span></span>



| <span data-ttu-id="5a1d5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a1d5-134">Requirement</span></span> | <span data-ttu-id="5a1d5-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5a1d5-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1d5-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a1d5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1d5-137">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5a1d5-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a1d5-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a1d5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1d5-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a1d5-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5a1d5-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a1d5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a1d5-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a1d5-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5a1d5-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5a1d5-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a1d5-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a1d5-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5a1d5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5a1d5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a1d5-145"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="5a1d5-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a1d5-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a1d5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1d5-147">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-147">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="5a1d5-148">**Oggetto Shell**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-148">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="5a1d5-149">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="5a1d5-149">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> </dl>

 

 
