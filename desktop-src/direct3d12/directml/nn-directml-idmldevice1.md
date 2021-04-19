---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Rappresenta un dispositivo DirectML, utilizzato per creare operatori, associazioni di tabelle, registratori di comandi e altri oggetti.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: a23d6ec4299a2aa3ca7e9f6873167412d094af8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320304"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="e29b9-103">Interfaccia IDMLDevice1 (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e29b9-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="e29b9-104">Rappresenta un dispositivo DirectML, utilizzato per creare operatori, associazioni di tabelle, registratori di comandi e altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="e29b9-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="e29b9-105">L'interfaccia **IDMLDevice1** eredita da [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="e29b9-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="e29b9-106">Un dispositivo DirectML è sempre associato esattamente a un dispositivo Direct3D 12 sottostante.</span><span class="sxs-lookup"><span data-stu-id="e29b9-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="e29b9-107">Tutti gli oggetti creati dal dispositivo DirectML gestiscono un riferimento sicuro al dispositivo padre.</span><span class="sxs-lookup"><span data-stu-id="e29b9-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="e29b9-108">A differenza del dispositivo Direct3D 12, il dispositivo DML non è un singleton.</span><span class="sxs-lookup"><span data-stu-id="e29b9-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="e29b9-109">È quindi possibile creare più dispositivi DirectML tramite lo stesso dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e29b9-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="e29b9-110">Tuttavia, questa operazione non è consigliata perché il dispositivo DirectML non ha uno stato modificabile, quindi è possibile creare più dispositivi DML tramite lo stesso dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e29b9-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="e29b9-111">Questo oggetto è thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e29b9-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e29b9-112">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="e29b9-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e29b9-113">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e29b9-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="e29b9-114">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="e29b9-114">Availability</span></span>
<span data-ttu-id="e29b9-115">Questa API è stata introdotta nella versione DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="e29b9-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e29b9-116">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="e29b9-116">Tensor constraints</span></span>
<span data-ttu-id="e29b9-117">**Piattaforma di destinazione**: Windows</span><span class="sxs-lookup"><span data-stu-id="e29b9-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="e29b9-118">Ereditarietà</span><span class="sxs-lookup"><span data-stu-id="e29b9-118">Inheritance</span></span>


<span data-ttu-id="e29b9-119">L'interfaccia IDMLDevice1 eredita dall'interfaccia IDMLDevice.</span><span class="sxs-lookup"><span data-stu-id="e29b9-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="e29b9-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="e29b9-120">Methods</span></span>

<p><span data-ttu-id="e29b9-121">L'interfaccia <b>IDMLDevice1</b> dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e29b9-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="e29b9-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="e29b9-122">Method</span></span> | <span data-ttu-id="e29b9-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e29b9-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="e29b9-124">IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="e29b9-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="e29b9-125">Compila un grafico di operatori DirectML in un oggetto che può essere inviato alla GPU.</span><span class="sxs-lookup"><span data-stu-id="e29b9-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="e29b9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e29b9-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e29b9-127">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="e29b9-127">**Target Platform**</span></span> | <span data-ttu-id="e29b9-128">Windows</span><span class="sxs-lookup"><span data-stu-id="e29b9-128">Windows</span></span> |
| <span data-ttu-id="e29b9-129">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e29b9-129">**Header**</span></span> | <span data-ttu-id="e29b9-130">directml. h</span><span class="sxs-lookup"><span data-stu-id="e29b9-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e29b9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e29b9-131">See also</span></span>

[<span data-ttu-id="e29b9-132">Interfaccia IDMLDevice</span><span class="sxs-lookup"><span data-stu-id="e29b9-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)