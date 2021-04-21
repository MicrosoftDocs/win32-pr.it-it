---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Rappresenta un dispositivo DirectML, utilizzato per creare operatori, tabelle di associazione, registratori di comandi e altri oggetti.
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
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803734"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="ea240-103">Interfaccia IDMLDevice1 (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ea240-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="ea240-104">Rappresenta un dispositivo DirectML, utilizzato per creare operatori, tabelle di associazione, registratori di comandi e altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="ea240-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="ea240-105">**L'interfaccia IDMLDevice1** eredita da [IDMLDevice.](/windows/win32/api/directml/nn-directml-idmldevice)</span><span class="sxs-lookup"><span data-stu-id="ea240-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="ea240-106">Un dispositivo DirectML è sempre associato esattamente a un dispositivo Direct3D 12 sottostante.</span><span class="sxs-lookup"><span data-stu-id="ea240-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="ea240-107">Tutti gli oggetti creati dal dispositivo DirectML mantengono un riferimento sicuro al dispositivo padre.</span><span class="sxs-lookup"><span data-stu-id="ea240-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="ea240-108">A differenza del dispositivo Direct3D 12, il dispositivo DML non è un singleton.</span><span class="sxs-lookup"><span data-stu-id="ea240-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="ea240-109">È quindi possibile creare più dispositivi DirectML sullo stesso dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="ea240-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="ea240-110">Tuttavia, questa operazione non è consigliata perché il dispositivo DirectML non ha uno stato modificabile, quindi la creazione di più dispositivi DML sullo stesso dispositivo Direct3D 12 non ha alcun vantaggio.</span><span class="sxs-lookup"><span data-stu-id="ea240-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="ea240-111">Questo oggetto è thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ea240-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea240-112">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive).</span><span class="sxs-lookup"><span data-stu-id="ea240-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ea240-113">Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ea240-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="ea240-114">Disponibilità</span><span class="sxs-lookup"><span data-stu-id="ea240-114">Availability</span></span>
<span data-ttu-id="ea240-115">Questa API è stata introdotta nella versione di `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="ea240-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ea240-116">Vincoli tensore</span><span class="sxs-lookup"><span data-stu-id="ea240-116">Tensor constraints</span></span>
<span data-ttu-id="ea240-117">**Piattaforma di destinazione:** Windows</span><span class="sxs-lookup"><span data-stu-id="ea240-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="ea240-118">Ereditarietà</span><span class="sxs-lookup"><span data-stu-id="ea240-118">Inheritance</span></span>


<span data-ttu-id="ea240-119">L'interfaccia IDMLDevice1 eredita dall'interfaccia IDMLDevice.</span><span class="sxs-lookup"><span data-stu-id="ea240-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="ea240-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="ea240-120">Methods</span></span>

<p><span data-ttu-id="ea240-121"><b>L'interfaccia IDMLDevice1</b> include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ea240-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="ea240-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="ea240-122">Method</span></span> | <span data-ttu-id="ea240-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea240-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="ea240-124">IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="ea240-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="ea240-125">Compila un grafico degli operatori DirectML in un oggetto che può essere inviato alla GPU.</span><span class="sxs-lookup"><span data-stu-id="ea240-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="ea240-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea240-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ea240-127">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="ea240-127">**Target Platform**</span></span> | <span data-ttu-id="ea240-128">Windows</span><span class="sxs-lookup"><span data-stu-id="ea240-128">Windows</span></span> |
| <span data-ttu-id="ea240-129">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="ea240-129">**Header**</span></span> | <span data-ttu-id="ea240-130">directml.h</span><span class="sxs-lookup"><span data-stu-id="ea240-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ea240-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea240-131">See also</span></span>

[<span data-ttu-id="ea240-132">Interfaccia IDMLDevice</span><span class="sxs-lookup"><span data-stu-id="ea240-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)