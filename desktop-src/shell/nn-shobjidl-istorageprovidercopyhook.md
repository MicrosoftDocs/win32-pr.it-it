---
description: Definisce un metodo che determina se la shell sarà consentita per lo spostamento, la copia, l'eliminazione o la ridenominazione di una cartella nella radice di sincronizzazione di un provider di cloud.
title: Interfaccia IStorageProviderCopyHook
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400496"
---
# <a name="istorageprovidercopyhook-interface"></a><span data-ttu-id="3b3b4-103">Interfaccia IStorageProviderCopyHook</span><span class="sxs-lookup"><span data-stu-id="3b3b4-103">IStorageProviderCopyHook interface</span></span>

<span data-ttu-id="3b3b4-104">Espone un metodo che determina se la shell sarà consentita per lo spostamento, la copia, l'eliminazione o la ridenominazione di una cartella nella radice di sincronizzazione di un provider di cloud.</span><span class="sxs-lookup"><span data-stu-id="3b3b4-104">Exposes a method that determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="members"></a><span data-ttu-id="3b3b4-105">Membri</span><span class="sxs-lookup"><span data-stu-id="3b3b4-105">Members</span></span>

<span data-ttu-id="3b3b4-106">L'interfaccia **IStorageProviderCopyHook** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3b3b4-106">The **IStorageProviderCopyHook** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3b3b4-107">**IStorageProviderCopyHook** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3b3b4-107">**IStorageProviderCopyHook** also has these types of members:</span></span>

- [<span data-ttu-id="3b3b4-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="3b3b4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3b3b4-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="3b3b4-109">Methods</span></span>

<span data-ttu-id="3b3b4-110">L'interfaccia **IStorageProviderCopyHook** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3b3b4-110">The **IStorageProviderCopyHook** interface has these methods.</span></span>



| <span data-ttu-id="3b3b4-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="3b3b4-111">Method</span></span>                                           | <span data-ttu-id="3b3b4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b3b4-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b3b4-113">**CopyCallback**</span><span class="sxs-lookup"><span data-stu-id="3b3b4-113">**CopyCallback**</span></span>](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  <span data-ttu-id="3b3b4-114">Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider cloud.</span><span class="sxs-lookup"><span data-stu-id="3b3b4-114">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>                                                           |


## <a name="requirements"></a><span data-ttu-id="3b3b4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b3b4-115">Requirements</span></span>

| <span data-ttu-id="3b3b4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b3b4-116">Requirement</span></span> | <span data-ttu-id="3b3b4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3b3b4-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b3b4-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b3b4-118">Minimum supported client</span></span> | <span data-ttu-id="3b3b4-119">Windows 10 Insider Preview Build 19624</span><span class="sxs-lookup"><span data-stu-id="3b3b4-119">Windows 10 Insider Preview Build 19624</span></span>                                                |
| <span data-ttu-id="3b3b4-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b3b4-120">Header</span></span><br/>                   | <span data-ttu-id="3b3b4-121">ShObjIdl. h</span><span class="sxs-lookup"><span data-stu-id="3b3b4-121">shobjidl.h</span></span>   |
