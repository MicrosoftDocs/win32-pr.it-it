---
title: Metodo IWMDRMLicense CanPersist (Wmdrmsdk.h)
description: Il metodo CanPersist esegue una query per determinare se la licenza può essere mantenuta in un archivio licenze locale.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Metodo CanPersist windows Media Format
- Metodo CanPersist windows Media Format , interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense windows Media Format , metodo CanPersist
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e174f0b7d48684e40cc5796d2ae95ec1bcaca99216c493c73609323daf276b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701219"
---
# <a name="iwmdrmlicensecanpersist-method"></a>Metodo IWMDRMLicense::CanPersist

Il **metodo CanPersist** esegue una query per determinare se la licenza può essere mantenuta in un archivio licenze locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfCanPersist* \[ Cambio\]
</dt> <dd>

TRUE indica che la licenza può essere mantenuta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





