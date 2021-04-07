---
title: Metodo Skip IEnumTfRenderingMarkup
description: Il metodo IEnumTfRenderingMarkup Skip ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Ignora Framework servizi di testo del metodo
- Skip Method Text Services Framework, interfaccia IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup Interface Text Services Framework, Skip (metodo)
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718172"
---
# <a name="ienumtfrenderingmarkupskip-method"></a>Metodo IEnumTfRenderingMarkup:: Skip

Il metodo **IEnumTfRenderingMarkup:: Skip** ottiene, dalla posizione corrente, il numero specificato di elementi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulCount* \[ in\]
</dt> <dd>

\[in \] specifica il numero di elementi da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                   | Descrizione                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Il metodo è stato eseguito correttamente.<br/>                                                                              |
| <dl> <dt>**S \_ false**</dt> </dl> | Il metodo ha raggiunto la fine dell'enumerazione prima che il numero di elementi specificato possa essere ignorato.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Questo metodo non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).

 

 

 





