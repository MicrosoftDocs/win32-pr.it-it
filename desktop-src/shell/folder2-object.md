---
description: Estende l'oggetto Folder per supportare le cartelle offline.
title: Oggetto Cartella2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: 8db899fc52cc3511d1af82013fc6c4c87544f1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979674"
---
# <a name="folder2-object"></a><span data-ttu-id="ab9ca-103">Oggetto Cartella2</span><span class="sxs-lookup"><span data-stu-id="ab9ca-103">Folder2 object</span></span>

<span data-ttu-id="ab9ca-104">Estende l'oggetto [**Folder**](folder.md) per supportare le cartelle offline.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-104">Extends the [**Folder**](folder.md) object to support offline folders.</span></span>

## <a name="members"></a><span data-ttu-id="ab9ca-105">Membri</span><span class="sxs-lookup"><span data-stu-id="ab9ca-105">Members</span></span>

<span data-ttu-id="ab9ca-106">L'oggetto **Cartella2** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ab9ca-106">The **Folder2** object has these types of members:</span></span>

-   [<span data-ttu-id="ab9ca-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="ab9ca-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="ab9ca-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab9ca-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ab9ca-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ab9ca-109">Methods</span></span>

<span data-ttu-id="ab9ca-110">L'oggetto **Cartella2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-110">The **Folder2** object has these methods.</span></span>



| <span data-ttu-id="ab9ca-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="ab9ca-111">Method</span></span>                                                                 | <span data-ttu-id="ab9ca-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab9ca-112">Description</span></span>                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab9ca-113">**DismissedWebViewBarricade**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-113">**DismissedWebViewBarricade**</span></span>](folder2-dismissedwebviewbarricade.md) | <span data-ttu-id="ab9ca-114">Chiamato in risposta alla barricata della visualizzazione Web che viene rilasciata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-114">Called in response to the web view barricade being dismissed by the user.</span></span><br/> |
| [<span data-ttu-id="ab9ca-115">**Sincronizzare**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-115">**Synchronize**</span></span>](folder2-synchronize.md)                             | <span data-ttu-id="ab9ca-116">Sincronizza tutti i file offline nella cartella.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-116">Synchronizes all offline files in the folder.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="ab9ca-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab9ca-117">Properties</span></span>

<span data-ttu-id="ab9ca-118">L'oggetto **Cartella2** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-118">The **Folder2** object has these properties.</span></span>



| <span data-ttu-id="ab9ca-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab9ca-119">Property</span></span>                                                                            | <span data-ttu-id="ab9ca-120">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ab9ca-120">Access type</span></span>          | <span data-ttu-id="ab9ca-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab9ca-121">Description</span></span>                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="ab9ca-122">**HaveToShowWebViewBarricade**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-122">**HaveToShowWebViewBarricade**</span></span>](folder2-havetoshowwebviewbarricade.md)<br/> | <span data-ttu-id="ab9ca-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab9ca-123">Read-only</span></span><br/> | <span data-ttu-id="ab9ca-124">Non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-124">Not currently supported.</span></span><br/>                                       |
| [<span data-ttu-id="ab9ca-125">**OfflineStatus**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-125">**OfflineStatus**</span></span>](folder2-offlinestatus.md)<br/>                           | <span data-ttu-id="ab9ca-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab9ca-126">Read-only</span></span><br/> | <span data-ttu-id="ab9ca-127">Contiene lo stato offline della cartella.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-127">Contains the offline status of the folder.</span></span><br/>                     |
| [<span data-ttu-id="ab9ca-128">**Auto**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-128">**Self**</span></span>](folder2-self.md)<br/>                                             | <span data-ttu-id="ab9ca-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab9ca-129">Read-only</span></span><br/> | <span data-ttu-id="ab9ca-130">Contiene l'oggetto [**FolderItem**](folderitem.md) della cartella.</span><span class="sxs-lookup"><span data-stu-id="ab9ca-130">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ab9ca-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab9ca-131">Requirements</span></span>



| <span data-ttu-id="ab9ca-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab9ca-132">Requirement</span></span> | <span data-ttu-id="ab9ca-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ab9ca-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9ca-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab9ca-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ab9ca-135">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab9ca-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab9ca-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ab9ca-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab9ca-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ab9ca-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab9ca-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab9ca-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ca-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ab9ca-140">IDL</span><span class="sxs-lookup"><span data-stu-id="ab9ca-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab9ca-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ca-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ab9ca-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ab9ca-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab9ca-143"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ca-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab9ca-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab9ca-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab9ca-145">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="ab9ca-145">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




