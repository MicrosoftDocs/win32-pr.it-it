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
# <a name="dxcoreadapterstate-enum"></a>Enumerazione DXCoreAdapterState

Definisce le costanti che specificano i tipi di Stati dell'adattatore DXCore. Passare una di queste costanti al metodo [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) per recuperare l'elemento di stato dell'adapter per un tipo di stato. passare una costante al metodo [IDXCoreAdapter:: sestate](./nf-dxcore_interface-idxcoreadapter-setstate.md) per impostare le informazioni di un adapter per un elemento di stato.

## <a name="syntax"></a>Sintassi

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>Costanti

### <a name="isdriverupdateinprogress"></a>IsDriverUpdateInProgress

Specifica lo stato dell'adattatore <em>IsDriverUpdateInProgress</em> , che `true` indica quando è stato avviato un aggiornamento del driver sulla scheda ma non è stato ancora completato. Se l'aggiornamento del driver è già stato completato, l'adapter sarà stato invalidato e la chiamata a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) restituirà un valore <b>HRESULT</b> di <b>DXGI_ERROR_DEVICE_REMOVED</b>.

Quando si chiama [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l'elemento stato <em>IsDriverUpdateInProgress</em> è di tipo <b>uint8_t</b>, che rappresenta un valore booleano.

<b>Importante</b>. Questo elemento di stato non è supportato per [sestate](./nf-dxcore_interface-idxcoreadapter-setstate.md).

### <a name="adaptermemorybudget"></a>AdapterMemoryBudget

Specifica lo stato dell'adattatore <em>AdapterMemoryBudget</em> , che recupera o richiede il budget di memoria dell'adapter per l'adapter.

Quando si chiama [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), lo stato dell'adattatore <em>AdapterMemoryBudget</em> è <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> per *inputStateDetails* e il tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> per *outputBuffer*.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter:: sestate](./nf-dxcore_interface-idxcoreadapter-setstate.md), [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)