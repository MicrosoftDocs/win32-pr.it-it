---
title: Metodo Clone IEnumTfRenderingMarkup
description: Il metodo IEnumTfRenderingMarkup Clone crea una copia dell'oggetto enumeratore.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Metodo Clone Framework servizi di testo
- Metodo Clone Framework servizi di testo, interfaccia IEnumTfRenderingMarkup
- Interfaccia IEnumTfRenderingMarkup Framework servizi di testo , metodo Clone
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d7909e75b44baf5a9efd33d86d01b1c86571c93a181decd6d3b0dd1019a3c38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118878745"
---
# <a name="ienumtfrenderingmarkupclone-method"></a>Metodo IEnumTfRenderingMarkup::Clone

Il **metodo IEnumTfRenderingMarkup::Clone** crea una copia dell'oggetto enumeratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ Cambio\]
</dt> <dd>

\[out \] Puntatore a [un'interfaccia IEnumTfRenderingMarkup.](/windows/desktop/TSF/ienumtfrenderingmarkup)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Si è verificato un errore non specificato.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o più parametri non sono validi.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Questo metodo non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL il [prototipo](prototypes.md).

 

 

