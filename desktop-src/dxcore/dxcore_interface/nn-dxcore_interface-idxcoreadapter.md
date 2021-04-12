---
title: IDXCoreAdapter
description: L' ****   interfaccia IDXCoreAdapter implementa i metodi per il recupero dei dettagli relativi a un elemento adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118303"
---
# <a name="idxcoreadapter-interface"></a>Interfaccia IDXCoreAdapter

L' ****   interfaccia IDXCoreAdapter implementa i metodi per il recupero dei dettagli relativi a un elemento adapter. **IDXCoreAdapter** eredita dall'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

## <a name="remarks"></a>Commenti

Le proprietà di un adapter vengono stabilite nel momento in cui l'adapter viene avviato e non sono modificabili per la durata dell'adapter. Questo si differenzia dallo stato di un adapter, che può essere sottoposto a query o impostato, e i cui valori possono cambiare nel tempo.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)