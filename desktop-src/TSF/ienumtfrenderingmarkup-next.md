---
title: Metodo Next di IEnumTfRenderingMarkup
description: Il metodo successivo IEnumTfRenderingMarkup ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Framework dei servizi di testo del metodo successivo
- Next Method Text Services Framework, interfaccia IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup Interface Text Services Framework, metodo Next
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046993"
---
# <a name="ienumtfrenderingmarkupnext-method"></a>IEnumTfRenderingMarkup:: Next (metodo)

Il metodo **IEnumTfRenderingMarkup:: Next** ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulCount* \[ out\]
</dt> <dd>

\[out \] specifica il numero di elementi da ottenere.

</dd> <dt>

*ppElement* \[ out\]
</dt> <dd>

\[\]puntatore out a una matrice di strutture [tf \_ RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) . La dimensione della matrice deve essere almeno di elementi *ulCount* .

</dd> <dt>

*pcFetched* \[ out\]
</dt> <dd>

\[\]puntatore out a un valore ULONG che riceve il numero di elementi effettivamente ottenuti. Questo valore può essere minore del numero di elementi richiesti. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>                                                                               |
| <dl> <dt>**S \_ false**</dt> </dl>      | Il metodo ha raggiunto la fine dell'enumerazione prima che sia possibile ottenere il numero specificato di elementi.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono validi.<br/>                                                                      |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Questo metodo non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).

 

 

