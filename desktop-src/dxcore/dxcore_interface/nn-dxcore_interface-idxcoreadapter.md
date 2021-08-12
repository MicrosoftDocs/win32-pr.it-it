---
title: IDXCoreAdapter
description: "**L'interfaccia IDXCoreAdapter** implementa metodi per il recupero di dettagli su un elemento dell'adattatore."
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 18cdd8082701ea4f1a8b5a3cfa047decd0f77df81b17eebe49bf5a8a887663fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278788"
---
# <a name="idxcoreadapter-interface"></a>Interfaccia IDXCoreAdapter

**L'interfaccia IDXCoreAdapter** implementa metodi per il recupero di dettagli su un elemento dell'adattatore. **IDXCoreAdapter** eredita [dall'interfaccia IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown) Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

## <a name="remarks"></a>Commenti

Le proprietà di un adapter vengono stabilite al momento dell'avvio e non sono modificabili per la durata dell'adapter. Questo è in contrasto con lo stato di un adapter, che può essere sottoposto a query o impostato, e i cui valori possono cambiare nel tempo.

## <a name="see-also"></a>Vedi anche

[Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)