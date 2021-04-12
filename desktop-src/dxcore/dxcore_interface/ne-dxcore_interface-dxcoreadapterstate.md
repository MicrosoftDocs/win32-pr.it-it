---
title: DXCoreAdapterState
description: Definisce le costanti che specificano i tipi di Stati dell'adattatore DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338039"
---
# <a name="dxcoreadapterstate-enum"></a><span data-ttu-id="b9adb-103">Enumerazione DXCoreAdapterState</span><span class="sxs-lookup"><span data-stu-id="b9adb-103">DXCoreAdapterState enum</span></span>

<span data-ttu-id="b9adb-104">Definisce le costanti che specificano i tipi di Stati dell'adattatore DXCore.</span><span class="sxs-lookup"><span data-stu-id="b9adb-104">Defines constants that specify kinds of DXCore adapter states.</span></span> <span data-ttu-id="b9adb-105">Passare una di queste costanti al metodo [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) per recuperare l'elemento di stato dell'adapter per un tipo di stato. passare una costante al metodo [IDXCoreAdapter:: sestate](./nf-dxcore_interface-idxcoreadapter-setstate.md) per impostare le informazioni di un adapter per un elemento di stato.</span><span class="sxs-lookup"><span data-stu-id="b9adb-105">Pass one of these constants to the [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) method to set an adapter's info for a state item.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9adb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9adb-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a><span data-ttu-id="b9adb-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="b9adb-107">Constants</span></span>

### <a name="isdriverupdateinprogress"></a><span data-ttu-id="b9adb-108">IsDriverUpdateInProgress</span><span class="sxs-lookup"><span data-stu-id="b9adb-108">IsDriverUpdateInProgress</span></span>

<span data-ttu-id="b9adb-109">Specifica lo stato dell'adattatore <em>IsDriverUpdateInProgress</em> , che `true` indica quando è stato avviato un aggiornamento del driver sulla scheda ma non è stato ancora completato.</span><span class="sxs-lookup"><span data-stu-id="b9adb-109">Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed.</span></span> <span data-ttu-id="b9adb-110">Se l'aggiornamento del driver è già stato completato, l'adapter sarà stato invalidato e la chiamata a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) restituirà un valore <b>HRESULT</b> di <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span><span class="sxs-lookup"><span data-stu-id="b9adb-110">If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span></span>

<span data-ttu-id="b9adb-111">Quando si chiama [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l'elemento stato <em>IsDriverUpdateInProgress</em> è di tipo <b>uint8_t</b>, che rappresenta un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="b9adb-111">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.</span></span>

<span data-ttu-id="b9adb-112"><b>Importante</b>.</span><span class="sxs-lookup"><span data-stu-id="b9adb-112"><b>Important</b>.</span></span> <span data-ttu-id="b9adb-113">Questo elemento di stato non è supportato per [sestate](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span><span class="sxs-lookup"><span data-stu-id="b9adb-113">This state item is not supported for [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span></span>

### <a name="adaptermemorybudget"></a><span data-ttu-id="b9adb-114">AdapterMemoryBudget</span><span class="sxs-lookup"><span data-stu-id="b9adb-114">AdapterMemoryBudget</span></span>

<span data-ttu-id="b9adb-115">Specifica lo stato dell'adattatore <em>AdapterMemoryBudget</em> , che recupera o richiede il budget di memoria dell'adapter per l'adapter.</span><span class="sxs-lookup"><span data-stu-id="b9adb-115">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span>

<span data-ttu-id="b9adb-116">Quando si chiama [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), lo stato dell'adattatore <em>AdapterMemoryBudget</em> è <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> per *inputStateDetails* e il tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> per *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="b9adb-116">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9adb-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9adb-117">See also</span></span>

<span data-ttu-id="b9adb-118">[IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter:: sestate](./nf-dxcore_interface-idxcoreadapter-setstate.md), [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="b9adb-118">[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>