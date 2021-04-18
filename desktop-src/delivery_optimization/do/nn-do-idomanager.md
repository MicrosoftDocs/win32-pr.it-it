---
title: Interfaccia IDOManager
description: Utilizzato per creare un nuovo download e per enumerare i download esistenti.
keywords:
- Interfaccia IDOManager
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300306"
---
# <a name="idomanager-interface"></a><span data-ttu-id="df3e3-104">Interfaccia IDOManager</span><span class="sxs-lookup"><span data-stu-id="df3e3-104">IDOManager interface</span></span>

<span data-ttu-id="df3e3-105">L'interfaccia **IDOManager** viene utilizzata per creare un nuovo download e per enumerare i download esistenti.</span><span class="sxs-lookup"><span data-stu-id="df3e3-105">The **IDOManager** interface is used to create a new download, and to enumerate existing downloads.</span></span>

## <a name="methods"></a><span data-ttu-id="df3e3-106">Metodi</span><span class="sxs-lookup"><span data-stu-id="df3e3-106">Methods</span></span>

<span data-ttu-id="df3e3-107">L'interfaccia **IDOManager** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="df3e3-107">The **IDOManager** interface has these methods.</span></span>

| <span data-ttu-id="df3e3-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="df3e3-108">Method</span></span> | <span data-ttu-id="df3e3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df3e3-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="df3e3-110">IDOManager::CreateDownload</span><span class="sxs-lookup"><span data-stu-id="df3e3-110">IDOManager::CreateDownload</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="df3e3-111">Crea un nuovo download.</span><span class="sxs-lookup"><span data-stu-id="df3e3-111">Creates a new download.</span></span> |
| [<span data-ttu-id="df3e3-112">IDOManager::EnumDownloads</span><span class="sxs-lookup"><span data-stu-id="df3e3-112">IDOManager::EnumDownloads</span></span>](./nf-do-idomanager-enumdownloads.md) | <span data-ttu-id="df3e3-113">Recupera un puntatore a interfaccia a un oggetto enumeratore utilizzato per enumerare i download esistenti.</span><span class="sxs-lookup"><span data-stu-id="df3e3-113">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span> |

## <a name="requirements"></a><span data-ttu-id="df3e3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df3e3-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="df3e3-115">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="df3e3-115">**Minimum supported client**</span></span> | <span data-ttu-id="df3e3-116">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="df3e3-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="df3e3-117">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="df3e3-117">**Minimum supported server**</span></span> | <span data-ttu-id="df3e3-118">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="df3e3-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="df3e3-119">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="df3e3-119">**Header**</span></span> | <span data-ttu-id="df3e3-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="df3e3-120">Do.h</span></span> |