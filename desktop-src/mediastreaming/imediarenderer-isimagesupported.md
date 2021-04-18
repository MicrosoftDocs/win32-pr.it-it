---
title: Metodo IMediaRenderer IsImageSupported
description: Recupera un valore che indica se ricevitore è in grado di visualizzare le immagini.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- API di streaming multimediale del metodo IsImageSupported
- API di streaming multimediale del metodo IsImageSupported, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, metodo IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299225"
---
# <a name="imediarendererisimagesupported-method"></a>Metodo IMediaRenderer:: IsImageSupported

Recupera un valore che indica se ricevitore è in grado di visualizzare le immagini.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Valore booleano che è **true** se ricevitore è in grado di visualizzare le immagini e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





