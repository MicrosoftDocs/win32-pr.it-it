---
description: Espone metodi che consentono le pagine HTML ospitate in un'estensione della procedura guidata per comunicare con la procedura guidata.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Oggetto WebWizardHost (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967430"
---
# <a name="webwizardhost-object"></a><span data-ttu-id="22a9d-103">Oggetto WebWizardHost</span><span class="sxs-lookup"><span data-stu-id="22a9d-103">WebWizardHost object</span></span>

<span data-ttu-id="22a9d-104">Espone metodi che consentono le pagine HTML ospitate in un'estensione della procedura guidata per comunicare con la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="22a9d-104">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span>

## <a name="members"></a><span data-ttu-id="22a9d-105">Membri</span><span class="sxs-lookup"><span data-stu-id="22a9d-105">Members</span></span>

<span data-ttu-id="22a9d-106">L'oggetto **WebWizardHost** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="22a9d-106">The **WebWizardHost** object has these types of members:</span></span>

-   [<span data-ttu-id="22a9d-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="22a9d-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="22a9d-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22a9d-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22a9d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="22a9d-109">Methods</span></span>

<span data-ttu-id="22a9d-110">L'oggetto **WebWizardHost** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="22a9d-110">The **WebWizardHost** object has these methods.</span></span>



| <span data-ttu-id="22a9d-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="22a9d-111">Method</span></span>                                                      | <span data-ttu-id="22a9d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22a9d-112">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22a9d-113">**Annulla**</span><span class="sxs-lookup"><span data-stu-id="22a9d-113">**Cancel**</span></span>](iwebwizardhost-cancel.md)                     | <span data-ttu-id="22a9d-114">Simula un clic del pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="22a9d-114">Simulates a **Cancel** button click.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="22a9d-115">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="22a9d-115">**FinalBack**</span></span>](iwebwizardhost-finalback.md)               | <span data-ttu-id="22a9d-116">Passa alla pagina lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.</span><span class="sxs-lookup"><span data-stu-id="22a9d-116">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span><br/>                                                                    |
| [<span data-ttu-id="22a9d-117">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="22a9d-117">**FinalNext**</span></span>](iwebwizardhost-finalnext.md)               | <span data-ttu-id="22a9d-118">Passa alla pagina della procedura guidata lato client che segue la pagina che ospita le pagine HTML sul lato server oppure termina la procedura guidata se non sono presenti altre pagine lato client.</span><span class="sxs-lookup"><span data-stu-id="22a9d-118">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span><br/> |
| [<span data-ttu-id="22a9d-119">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="22a9d-119">**SetHeaderText**</span></span>](iwebwizardhost-setheadertext.md)       | <span data-ttu-id="22a9d-120">Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="22a9d-120">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="22a9d-121">In generale, il client visualizzerà l'intestazione sopra il codice HTML e sotto la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="22a9d-121">In general, the client will display the header above the HTML and below the title bar.</span></span><br/>                    |
| [<span data-ttu-id="22a9d-122">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="22a9d-122">**SetWizardButtons**</span></span>](iwebwizardhost-setwizardbuttons.md) | <span data-ttu-id="22a9d-123">Aggiorna i pulsanti **indietro**, **Avanti** e **fine** nel frame della procedura guidata del client.</span><span class="sxs-lookup"><span data-stu-id="22a9d-123">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="22a9d-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22a9d-124">Properties</span></span>

<span data-ttu-id="22a9d-125">L'oggetto **WebWizardHost** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="22a9d-125">The **WebWizardHost** object has these properties.</span></span>



| <span data-ttu-id="22a9d-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="22a9d-126">Property</span></span>                                               | <span data-ttu-id="22a9d-127">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="22a9d-127">Access type</span></span>           | <span data-ttu-id="22a9d-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22a9d-128">Description</span></span>                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="22a9d-129">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="22a9d-129">**Caption**</span></span>](iwebwizardhost-caption.md)<br/>   | <span data-ttu-id="22a9d-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="22a9d-130">Read/write</span></span><br/> | <span data-ttu-id="22a9d-131">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="22a9d-131">Not implemented.</span></span><br/>                              |
| [<span data-ttu-id="22a9d-132">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="22a9d-132">**Property**</span></span>](iwebwizardhost-property.md)<br/> | <span data-ttu-id="22a9d-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="22a9d-133">Read/write</span></span><br/> | <span data-ttu-id="22a9d-134">Imposta o Recupera il valore corrente di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="22a9d-134">Sets or retrieves a property's current value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="22a9d-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22a9d-135">Requirements</span></span>



| <span data-ttu-id="22a9d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="22a9d-136">Requirement</span></span> | <span data-ttu-id="22a9d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="22a9d-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22a9d-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22a9d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="22a9d-139">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="22a9d-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="22a9d-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22a9d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="22a9d-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22a9d-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="22a9d-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22a9d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="22a9d-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="22a9d-143"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="22a9d-144">IDL</span><span class="sxs-lookup"><span data-stu-id="22a9d-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="22a9d-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="22a9d-145"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="22a9d-146">IID</span><span class="sxs-lookup"><span data-stu-id="22a9d-146">IID</span></span><br/>                      | <span data-ttu-id="22a9d-147">\_WEBWIZARDHOST CLSID</span><span class="sxs-lookup"><span data-stu-id="22a9d-147">CLSID\_WebWizardHost</span></span><br/>                                                        |



 

 




