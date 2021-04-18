---
title: DXCore
description: DXCore è un'API di enumerazione degli adapter per i dispositivi DirectX.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: 80e93ac7440629a809cb01b4d1d4fa2e73b7ee91
ms.sourcegitcommit: aa021b23d7e8bba2e1df9de93a1c315a17681810
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/10/2020
ms.locfileid: "106300710"
---
# <a name="dxcore"></a><span data-ttu-id="68eb9-103">DXCore</span><span class="sxs-lookup"><span data-stu-id="68eb9-103">DXCore</span></span>

<span data-ttu-id="68eb9-104">DXCore è un'API di enumerazione degli adapter per i dispositivi grafici e di calcolo, quindi alcune delle sue funzionalità si sovrappongono a quelle di [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="68eb9-104">DXCore is an adapter enumeration API for graphics and compute devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span> <span data-ttu-id="68eb9-105">DXCore viene usato da Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="68eb9-105">DXCore is used by Direct3D 12.</span></span>

<span data-ttu-id="68eb9-106">Questo set di documentazione contiene informazioni sulla programmazione con DXCore, oltre al riferimento a DXCore.</span><span class="sxs-lookup"><span data-stu-id="68eb9-106">This documentation set contains information about programming with DXCore, as well as the DXCore reference.</span></span>

## <a name="requirements"></a><span data-ttu-id="68eb9-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68eb9-107">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="68eb9-108">**Ambienti di runtime supportati**</span><span class="sxs-lookup"><span data-stu-id="68eb9-108">**Supported runtime environments**</span></span> | <span data-ttu-id="68eb9-109">Windows/C++</span><span class="sxs-lookup"><span data-stu-id="68eb9-109">Windows/C++</span></span> |
| <span data-ttu-id="68eb9-110">**Linguaggi di programmazione consigliati**</span><span class="sxs-lookup"><span data-stu-id="68eb9-110">**Recommended programming languages**</span></span> | <span data-ttu-id="68eb9-111">C++</span><span class="sxs-lookup"><span data-stu-id="68eb9-111">C++</span></span> |
| <span data-ttu-id="68eb9-112">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="68eb9-112">**Minimum supported client**</span></span> | <span data-ttu-id="68eb9-113">Windows 10, versione 2004 (10,0; Compilazione 19041)</span><span class="sxs-lookup"><span data-stu-id="68eb9-113">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="68eb9-114">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="68eb9-114">**Header**</span></span> | <span data-ttu-id="68eb9-115">dxcore. h e dxcore_interface. h</span><span class="sxs-lookup"><span data-stu-id="68eb9-115">dxcore.h and dxcore_interface.h</span></span> |
| <span data-ttu-id="68eb9-116">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="68eb9-116">**Library**</span></span> | <span data-ttu-id="68eb9-117">dxcore. lib</span><span class="sxs-lookup"><span data-stu-id="68eb9-117">dxcore.lib</span></span> |
| <span data-ttu-id="68eb9-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="68eb9-118">**DLL**</span></span> | <span data-ttu-id="68eb9-119">dxcore.dll</span><span class="sxs-lookup"><span data-stu-id="68eb9-119">dxcore.dll</span></span> |

## <a name="in-this-section"></a><span data-ttu-id="68eb9-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="68eb9-120">In this section</span></span>

| <span data-ttu-id="68eb9-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="68eb9-121">Topic</span></span> | <span data-ttu-id="68eb9-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68eb9-122">Description</span></span> |
|-|-|
| [<span data-ttu-id="68eb9-123">Guida alla programmazione di DXCore</span><span class="sxs-lookup"><span data-stu-id="68eb9-123">DXCore programming guide</span></span>](dxcore-programming-guide.md) | <span data-ttu-id="68eb9-124">Linee guida per la programmazione con DXCore.</span><span class="sxs-lookup"><span data-stu-id="68eb9-124">Guidance for programming with DXCore.</span></span> |
| [<span data-ttu-id="68eb9-125">Riferimento DXCore</span><span class="sxs-lookup"><span data-stu-id="68eb9-125">DXCore reference</span></span>](dxcore-reference.md) | <span data-ttu-id="68eb9-126">Questa sezione descrive le API DXCore dichiarate in dxcore. h e dxcore_interface. h.</span><span class="sxs-lookup"><span data-stu-id="68eb9-126">This section covers DXCore APIs declared in dxcore.h and dxcore_interface.h.</span></span> |
