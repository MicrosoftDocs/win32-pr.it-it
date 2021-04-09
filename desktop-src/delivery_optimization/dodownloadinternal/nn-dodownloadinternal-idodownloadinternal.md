---
title: Interfaccia IDODownloadInternal
description: Utilizzato per ottenere o impostare le proprietà di download estese.
keywords:
- Interfaccia IDODownloadInternal
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118126"
---
# <a name="idodownloadinternal-interface"></a><span data-ttu-id="6cd03-104">Interfaccia IDODownloadInternal</span><span class="sxs-lookup"><span data-stu-id="6cd03-104">IDODownloadInternal interface</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cd03-105">L'interfaccia **IDODownloadInternal** è deprecata.</span><span class="sxs-lookup"><span data-stu-id="6cd03-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="6cd03-106">Usare invece l'interfaccia [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="6cd03-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="6cd03-107">L'interfaccia **IDODownloadInternal** viene utilizzata per ottenere o impostare le proprietà di download estese.</span><span class="sxs-lookup"><span data-stu-id="6cd03-107">The **IDODownloadInternal** interface is used to get or set extended download properties.</span></span>

## <a name="methods"></a><span data-ttu-id="6cd03-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="6cd03-108">Methods</span></span>

<span data-ttu-id="6cd03-109">L'interfaccia **IDODownloadInternal** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6cd03-109">The **IDODownloadInternal** interface has these methods.</span></span>

| <span data-ttu-id="6cd03-110">Metodo</span><span class="sxs-lookup"><span data-stu-id="6cd03-110">Method</span></span> | <span data-ttu-id="6cd03-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cd03-111">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="6cd03-112">IDODownloadInternal::GetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="6cd03-112">IDODownloadInternal::GetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | <span data-ttu-id="6cd03-113">Recupera un puntatore a un **Variant** che contiene un valore di proprietà di download esteso specifico.</span><span class="sxs-lookup"><span data-stu-id="6cd03-113">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span> |
| [<span data-ttu-id="6cd03-114">IDODownloadInternal::SetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="6cd03-114">IDODownloadInternal::SetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | <span data-ttu-id="6cd03-115">Imposta una proprietà di download estesa.</span><span class="sxs-lookup"><span data-stu-id="6cd03-115">Sets an extended download property.</span></span> <span data-ttu-id="6cd03-116">Il metodo accetta un puntatore a una **variante** che contiene un valore della proprietà specifico da applicare al download.</span><span class="sxs-lookup"><span data-stu-id="6cd03-116">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="6cd03-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cd03-117">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6cd03-118">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="6cd03-118">**Minimum supported client**</span></span> | <span data-ttu-id="6cd03-119">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="6cd03-119">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6cd03-120">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="6cd03-120">**Minimum supported server**</span></span> | <span data-ttu-id="6cd03-121">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="6cd03-121">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6cd03-122">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="6cd03-122">**Header**</span></span> | <span data-ttu-id="6cd03-123">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="6cd03-123">DODownloadInternal.h</span></span> |