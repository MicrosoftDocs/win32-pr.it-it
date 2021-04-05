---
title: Metodo ITfContextRenderingMarkup GetRenderingMarkup
description: Il metodo ITfContextRenderingMarkup GetRenderingMarkup recupera un enumeratore dei markup di rendering per l'intervallo specificato.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Framework servizi di testo Metodo GetRenderingMarkup
- Framework dei servizi di testo del metodo GetRenderingMarkup, interfaccia ITfContextRenderingMarkup
- ITfContextRenderingMarkup Interface Text Services Framework, metodo GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728554"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>Metodo ITfContextRenderingMarkup:: GetRenderingMarkup

Il metodo **ITfContextRenderingMarkup:: GetRenderingMarkup** recupera un enumeratore dei markup di rendering per l'intervallo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EC* \[ in\]
</dt> <dd>

\[in \] un cookie di modifica di sola lettura per accedere al contesto.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

\[in\]



| Valore                                                                                                                                                                                         | Significato                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**\_proprietà di \_ inclusione TF GRM \_**</dt> </dl> | Se questo bit è 1, l'enumeratore includerà la \_ proprietà dell'attributo GUID Prop \_ .<br/> |



 

</dd> <dt>

*pRangeCover* \[ in\]
</dt> <dd>

\[in \] un puntatore a un'interfaccia [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) dell'intervallo per enumerare i markup di rendering.

</dd> <dt>

*ppEnum* \[ out\]
</dt> <dd>

\[\]un puntatore per recuperare il puntatore all'interfaccia [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                | Descrizione                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Questo metodo non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL per il [prototipo](prototypes.md).

 

 

