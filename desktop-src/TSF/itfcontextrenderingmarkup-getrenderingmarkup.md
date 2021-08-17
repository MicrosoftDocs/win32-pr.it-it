---
title: Metodo ITfContextRenderingMarkup GetRenderingMarkup
description: Il metodo ITfContextRenderingMarkup GetRenderingMarkup recupera un enumeratore dei markup di rendering per l'intervallo specificato.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Metodo GetRenderingMarkup Framework servizi di testo
- Metodo GetRenderingMarkup Framework servizi di testo, interfaccia ITfContextRenderingMarkup
- Interfaccia ITfContextRenderingMarkup Framework servizi di testo , metodo GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a94c8a7cce8673560cf01091b819def343213bfde578df6ce1e8850e2721723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476956"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>Metodo ITfContextRenderingMarkup::GetRenderingMarkup

Il **metodo ITfContextRenderingMarkup::GetRenderingMarkup** recupera un enumeratore dei markup di rendering per l'intervallo specificato.

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

*ec* \[ Pollici\]
</dt> <dd>

\[in \] Un cookie di modifica di sola lettura per accedere al contesto.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

\[in\]



| Valore                                                                                                                                                                                         | Significato                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**PROPRIETÀ \_ INCLUDE DI TF GRM \_ \_**</dt> </dl> | Se questo bit è 1, l'enumeratore includerà la proprietà \_ GUID PROP \_ ATTRIBUTE.<br/> |



 

</dd> <dt>

*pRangeCover* \[ Pollici\]
</dt> <dd>

\[in \] Puntatore a [un'interfaccia ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) dell'intervallo per enumerare i markup di rendering.

</dd> <dt>

*ppEnum* \[ Cambio\]
</dt> <dd>

\[out \] Puntatore per recuperare [il puntatore di interfaccia IEnumTfRenderingMarkup.](/windows/desktop/TSF/ienumtfrenderingmarkup)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                | Descrizione                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Questo metodo non è attualmente presente nei file di intestazione pubblici. Per usare questa API, è necessario compilare MIDL il [prototipo](prototypes.md).

 

 

