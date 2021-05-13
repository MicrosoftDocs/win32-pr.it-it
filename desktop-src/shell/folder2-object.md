---
description: Estende l'oggetto Folder per supportare le cartelle offline.
title: Oggetto Folder2 (Shldisp.h)
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
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842062"
---
# <a name="folder2-object"></a><span data-ttu-id="336cd-103">Oggetto Folder2</span><span class="sxs-lookup"><span data-stu-id="336cd-103">Folder2 object</span></span>

<span data-ttu-id="336cd-104">Estende [**l'oggetto Folder**](folder.md) per supportare le cartelle offline.</span><span class="sxs-lookup"><span data-stu-id="336cd-104">Extends the [**Folder**](folder.md) object to support offline folders.</span></span>

## <a name="members"></a><span data-ttu-id="336cd-105">Membri</span><span class="sxs-lookup"><span data-stu-id="336cd-105">Members</span></span>

<span data-ttu-id="336cd-106">**L'oggetto Folder2** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="336cd-106">The **Folder2** object has these types of members:</span></span>

-   [<span data-ttu-id="336cd-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="336cd-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="336cd-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="336cd-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="336cd-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="336cd-109">Methods</span></span>

<span data-ttu-id="336cd-110">**L'oggetto Folder2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="336cd-110">The **Folder2** object has these methods.</span></span>



| <span data-ttu-id="336cd-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="336cd-111">Method</span></span>                                                                 | <span data-ttu-id="336cd-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="336cd-112">Description</span></span>                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="336cd-113">**DismissedWebViewBarricade**</span><span class="sxs-lookup"><span data-stu-id="336cd-113">**DismissedWebViewBarricade**</span></span>](folder2-dismissedwebviewbarricade.md) | <span data-ttu-id="336cd-114">Chiamato in risposta alla barra di visualizzazione Web ignorata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="336cd-114">Called in response to the web view barricade being dismissed by the user.</span></span><br/> |
| [<span data-ttu-id="336cd-115">**Sincronizzare**</span><span class="sxs-lookup"><span data-stu-id="336cd-115">**Synchronize**</span></span>](folder2-synchronize.md)                             | <span data-ttu-id="336cd-116">Sincronizza tutti i file offline nella cartella.</span><span class="sxs-lookup"><span data-stu-id="336cd-116">Synchronizes all offline files in the folder.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="336cd-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="336cd-117">Properties</span></span>

<span data-ttu-id="336cd-118">**L'oggetto Folder2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="336cd-118">The **Folder2** object has these properties.</span></span>



| <span data-ttu-id="336cd-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="336cd-119">Property</span></span>                                                                            | <span data-ttu-id="336cd-120">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="336cd-120">Access type</span></span>          | <span data-ttu-id="336cd-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="336cd-121">Description</span></span>                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="336cd-122">**HaveToShowWebViewBarricade**</span><span class="sxs-lookup"><span data-stu-id="336cd-122">**HaveToShowWebViewBarricade**</span></span>](folder2-havetoshowwebviewbarricade.md)<br/> | <span data-ttu-id="336cd-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="336cd-123">Read-only</span></span><br/> | <span data-ttu-id="336cd-124">Non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="336cd-124">Not currently supported.</span></span><br/>                                       |
| [<span data-ttu-id="336cd-125">**OfflineStatus**</span><span class="sxs-lookup"><span data-stu-id="336cd-125">**OfflineStatus**</span></span>](folder2-offlinestatus.md)<br/>                           | <span data-ttu-id="336cd-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="336cd-126">Read-only</span></span><br/> | <span data-ttu-id="336cd-127">Contiene lo stato offline della cartella.</span><span class="sxs-lookup"><span data-stu-id="336cd-127">Contains the offline status of the folder.</span></span><br/>                     |
| [<span data-ttu-id="336cd-128">**stesso**</span><span class="sxs-lookup"><span data-stu-id="336cd-128">**Self**</span></span>](folder2-self.md)<br/>                                             | <span data-ttu-id="336cd-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="336cd-129">Read-only</span></span><br/> | <span data-ttu-id="336cd-130">Contiene l'oggetto [**FolderItem della**](folderitem.md) cartella.</span><span class="sxs-lookup"><span data-stu-id="336cd-130">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="336cd-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="336cd-131">Requirements</span></span>



| <span data-ttu-id="336cd-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="336cd-132">Requirement</span></span> | <span data-ttu-id="336cd-133">Valore</span><span class="sxs-lookup"><span data-stu-id="336cd-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="336cd-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="336cd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="336cd-135">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="336cd-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="336cd-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="336cd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="336cd-137">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="336cd-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="336cd-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="336cd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="336cd-139"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="336cd-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="336cd-140">Idl</span><span class="sxs-lookup"><span data-stu-id="336cd-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="336cd-141"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="336cd-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="336cd-142">DLL</span><span class="sxs-lookup"><span data-stu-id="336cd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="336cd-143"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="336cd-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="336cd-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="336cd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="336cd-145">**Cartella**</span><span class="sxs-lookup"><span data-stu-id="336cd-145">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




