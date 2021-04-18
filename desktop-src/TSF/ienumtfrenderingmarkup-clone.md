---
title: Metodo Clone IEnumTfRenderingMarkup
description: Il metodo Clone IEnumTfRenderingMarkup crea una copia dell'oggetto enumeratore.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Framework dei servizi di testo del metodo Clone
- Framework dei servizi di testo del metodo Clone, interfaccia IEnumTfRenderingMarkup
- Framework dei servizi di testo dell'interfaccia IEnumTfRenderingMarkup, metodo Clone
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299962"
---
# <a name="ienumtfrenderingmarkupclone-method"></a>Metodo IEnumTfRenderingMarkup:: Clone

Il metodo **IEnumTfRenderingMarkup:: Clone** crea una copia dell'oggetto enumeratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

\[\]un puntatore a un'interfaccia [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>          |
| <dl> <dt>**E \_ non riescono**</dt> </dl>       | Si è verificato un errore non specificato.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono validi.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Questo metodo non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).

 

 

