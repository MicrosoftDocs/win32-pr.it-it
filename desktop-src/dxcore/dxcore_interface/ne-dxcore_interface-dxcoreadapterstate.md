---
title: DXCoreAdapterState
description: Definisce costanti che specificano tipi di stati dell'adapter DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6878aaccb61fd164fcf834561fcf70f13d2609de595687b6ef6301778c87f81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367081"
---
# <a name="dxcoreadapterstate-enum"></a>Enumerazione DXCoreAdapterState

Definisce costanti che specificano tipi di stati dell'adapter DXCore. Passare una di queste costanti al metodo [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) per recuperare l'elemento dello stato dell'adapter per un tipo di stato. Passare una costante al metodo [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) per impostare le informazioni di un adattatore per un elemento di stato.

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

Specifica lo stato <em>dell'adapter IsDriverUpdateInProgress,</em> che quando indica che un aggiornamento del driver è stato avviato nella scheda ma non `true` è ancora stato completato. Se l'aggiornamento del driver è già stato completato, l'adapter sarà stato invalidato e la chiamata [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) restituirà <b>un HRESULT</b> di <b>DXGI_ERROR_DEVICE_REMOVED</b>.

Quando si [chiama QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l'elemento di stato <em>IsDriverUpdateInProgress</em> ha uint8_t <b>,</b>che rappresenta un valore booleano.

<b>Importante</b>. Questo elemento di stato non è supportato per [SetState.](./nf-dxcore_interface-idxcoreadapter-setstate.md)

### <a name="adaptermemorybudget"></a>AdapterMemoryBudget

Specifica lo stato <em>dell'adapter AdapterMemoryBudget,</em> che recupera o richiede il budget di memoria dell'adapter.

Quando si chiama [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), lo stato dell'adapter <em>AdapterMemoryBudget</em> è di tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> per *inputStateDetails* e tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> per *outputBuffer*.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)