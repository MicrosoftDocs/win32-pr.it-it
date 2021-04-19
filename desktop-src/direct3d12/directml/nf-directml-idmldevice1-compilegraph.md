---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila un grafico di operatori DirectML in un oggetto che può essere inviato alla GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 25dbc62fac9cd38d9728a295e336038441aee19f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320278"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="fbb7f-103">Metodo IDMLDevice1:: CompileGraph (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fbb7f-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="fbb7f-104">Compila un grafico di operatori DirectML in un oggetto che può essere inviato alla GPU.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="fbb7f-105">Un operatore compilato rappresenta il formato efficiente e cotto di un operatore adatto per l'esecuzione nella GPU.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="fbb7f-106">Un operatore compilato include lo stato (ad esempio shader e altri oggetti) necessario per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="fbb7f-107">Poiché un operatore compilato implementa l'interfaccia [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) , è possibile rimuoverne uno dalla memoria GPU, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="fbb7f-108">Per altre informazioni, vedere [IDMLDevice1:: Rimuovi](/windows/win32/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice1:: MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) .</span><span class="sxs-lookup"><span data-stu-id="fbb7f-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="fbb7f-109">L'operatore compilato non usa né fa riferimento agli oggetti [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) forniti all'interno della descrizione del grafo dopo la restituzione di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbb7f-110">Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="fbb7f-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fbb7f-111">Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fbb7f-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb7f-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbb7f-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="fbb7f-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbb7f-113">Parameters</span></span>

`desc`

<span data-ttu-id="fbb7f-114">Tipo: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbb7f-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="fbb7f-115">Descrizione del grafo da compilare.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-115">A description of the graph to compile.</span></span> <span data-ttu-id="fbb7f-116">Vedere [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span><span class="sxs-lookup"><span data-stu-id="fbb7f-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="fbb7f-117">Tipo: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="fbb7f-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="fbb7f-118">Tutti i flag per controllare l'esecuzione di questo operatore.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="fbb7f-119">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="fbb7f-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="fbb7f-120">Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera restituire in <i>PPV</i>.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="fbb7f-121">Questo dovrebbe essere il GUID di [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span><span class="sxs-lookup"><span data-stu-id="fbb7f-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="fbb7f-122">Tipo: <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="fbb7f-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="fbb7f-123">Puntatore a un blocco di memoria che riceve un puntatore all'operatore compilato.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="fbb7f-124">Si tratta dell'indirizzo di un puntatore a un [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), che rappresenta l'operatore compilato creato.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="fbb7f-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbb7f-125">Return value</span></span>

<span data-ttu-id="fbb7f-126">Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="fbb7f-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="fbb7f-127">Se questo metodo ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="fbb7f-128">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbb7f-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb7f-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbb7f-129">Remarks</span></span>

<span data-ttu-id="fbb7f-130">L'API Graph di DirectML operator fornisce un metodo astratto per usare DirectML in modo efficiente tra diversi componenti hardware.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="fbb7f-131">DirectML applica le ottimizzazioni a livello di tensore, ad esempio la scelta del layout tensore più efficiente in base alla scheda utilizzata.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="fbb7f-132">Applica anche le ottimizzazioni, ad esempio la rimozione di operatori join o Split.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="fbb7f-133">È consigliabile applicare ottimizzazioni di alto livello prima di creare un grafico DirectML.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="fbb7f-134">Ad esempio, fondendo gli operatori di convoluzione con BatchNorm, la riduzione costante e l'eliminazione di sottoespressioni comuni.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="fbb7f-135">Le ottimizzazioni all'interno dell'utilità di ottimizzazione dei grafici di DirectML sono progettate per completare queste ottimizzazioni indipendenti dal dispositivo, che in genere vengono gestite in modo generico dai framework di machine learning.</span><span class="sxs-lookup"><span data-stu-id="fbb7f-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb7f-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbb7f-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fbb7f-137">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="fbb7f-137">**Target Platform**</span></span> | <span data-ttu-id="fbb7f-138">Windows</span><span class="sxs-lookup"><span data-stu-id="fbb7f-138">Windows</span></span> |
| <span data-ttu-id="fbb7f-139">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="fbb7f-139">**Header**</span></span> | <span data-ttu-id="fbb7f-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="fbb7f-140">directml.h</span></span> |
| <span data-ttu-id="fbb7f-141">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="fbb7f-141">**Library**</span></span> | <span data-ttu-id="fbb7f-142">DirectML. lib</span><span class="sxs-lookup"><span data-stu-id="fbb7f-142">DirectML.lib</span></span> |
| <span data-ttu-id="fbb7f-143">**DLL**</span><span class="sxs-lookup"><span data-stu-id="fbb7f-143">**DLL**</span></span> | <span data-ttu-id="fbb7f-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="fbb7f-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="fbb7f-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbb7f-145">See also</span></span>

[<span data-ttu-id="fbb7f-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="fbb7f-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)