---
title: Interfaccia IEnumTfRenderingMarkup
description: L'interfaccia IEnumTfRenderingMarkup viene implementata da TSF Manager e utilizzata dalle applicazioni. Questa interfaccia può essere recuperata da ITfContextRenderingMarkup GetRenderingMarkup ed enumera le informazioni di markup per il rendering.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- Framework servizi di testo interfaccia IEnumTfRenderingMarkup
- Framework dei servizi di testo dell'interfaccia IEnumTfRenderingMarkup, descritto
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047155"
---
# <a name="ienumtfrenderingmarkup-interface"></a>Interfaccia IEnumTfRenderingMarkup

L'interfaccia **IEnumTfRenderingMarkup** viene implementata da TSF Manager e utilizzata dalle applicazioni. Questa interfaccia può essere recuperata da [ITfContextRenderingMarkup:: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) ed enumera le informazioni di markup per il rendering.



| Metodi IEnumTfRenderingMarkup            | Descrizione                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Clone](ienumtfrenderingmarkup-clone.md) | Il metodo **IEnumTfRenderingMarkup:: Clone** crea una copia dell'oggetto enumeratore.                                                                  |
| [Avanti](ienumtfrenderingmarkup-next.md)   | Il metodo **IEnumTfRenderingMarkup:: Next** ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.          |
| [Reimpostazione](ienumtfrenderingmarkup-reset.md) | Il metodo **IEnumTfRenderingMarkup:: Reset** Reimposta l'oggetto enumeratore spostando la posizione corrente all'inizio della sequenza di enumerazione. |
| [Skip](ienumtfrenderingmarkup-skip.md)   | Il metodo **IEnumTfRenderingMarkup:: Skip** ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.          |



 

## <a name="members"></a>Membri

L'interfaccia **IEnumTfRenderingMarkup** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questa interfaccia non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).

 

 

 