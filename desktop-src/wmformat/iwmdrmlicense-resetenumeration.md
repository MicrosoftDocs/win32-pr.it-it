---
title: Metodo IWMDRMLicense ResetEnumeration (Wmdrmsdk.h)
description: Il metodo ResetEnumeration reimposta lo stato originale dell'elenco di licenze. La licenza attiva diventa la prima licenza nell'elenco.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Metodo ResetEnumeration windows Media Format
- Metodo ResetEnumeration windows Media Format , interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense windows Media Format , metodo ResetEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dda6de46a2ce96d1fec1abaaae56edcbc5b0d6a73e8ee13f038dba6b5577c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027689"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a>Metodo IWMDRMLicense::ResetEnumeration

Il **metodo ResetEnumeration** reimposta lo stato originale dell'elenco di licenze. La licenza attiva diventa la prima licenza nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM RIV TROPPO \_ \_ \_ PICCOLO**</dt> </dl> | È necessario un elenco di revoche di contenuto aggiornato.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





