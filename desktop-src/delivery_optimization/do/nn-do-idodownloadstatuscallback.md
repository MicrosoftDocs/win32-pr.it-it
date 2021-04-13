---
title: Interfaccia IDODownloadStatusCallback
description: Utilizzato per ricevere notifiche relative a un download.
keywords:
- Interfaccia IDODownloadStatusCallback
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399078"
---
# <a name="idodownloadstatuscallback-interface"></a><span data-ttu-id="10b97-104">Interfaccia IDODownloadStatusCallback</span><span class="sxs-lookup"><span data-stu-id="10b97-104">IDODownloadStatusCallback interface</span></span>

<span data-ttu-id="10b97-105">L'interfaccia **IDODownloadStatusCallback** viene utilizzata per ricevere notifiche relative a un download.</span><span class="sxs-lookup"><span data-stu-id="10b97-105">The **IDODownloadStatusCallback** interface is used to receive notifications about a download.</span></span>

## <a name="methods"></a><span data-ttu-id="10b97-106">Metodi</span><span class="sxs-lookup"><span data-stu-id="10b97-106">Methods</span></span>

<span data-ttu-id="10b97-107">L'interfaccia **IDODownloadStatusCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="10b97-107">The **IDODownloadStatusCallback** interface has these methods.</span></span>

| <span data-ttu-id="10b97-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="10b97-108">Method</span></span> | <span data-ttu-id="10b97-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10b97-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="10b97-110">IDODownloadStatusCallback::OnStatusChanged</span><span class="sxs-lookup"><span data-stu-id="10b97-110">IDODownloadStatusCallback::OnStatusChanged</span></span>](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | <span data-ttu-id="10b97-111">Chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato del download.</span><span class="sxs-lookup"><span data-stu-id="10b97-111">DO calls your implementation of this method any time a download status has changed.</span></span> |

## <a name="requirements"></a><span data-ttu-id="10b97-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10b97-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="10b97-113">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="10b97-113">**Minimum supported client**</span></span> | <span data-ttu-id="10b97-114">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="10b97-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="10b97-115">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="10b97-115">**Minimum supported server**</span></span> | <span data-ttu-id="10b97-116">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="10b97-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="10b97-117">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="10b97-117">**Header**</span></span> | <span data-ttu-id="10b97-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="10b97-118">Do.h</span></span> |