---
title: Metodo IWMDRMLicense CanPersist (wmdrmsdk. h)
description: Il metodo CanPersist esegue una query per determinare se la licenza può essere mantenute in un archivio licenze locale.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Metodo CanPersist Windows Media Format
- Metodo CanPersist Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo CanPersist
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
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328532"
---
# <a name="iwmdrmlicensecanpersist-method"></a>Metodo IWMDRMLicense:: CanPersist

Il metodo **CanPersist** esegue una query per determinare se la licenza può essere mantenute in un archivio licenze locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfCanPersist* \[ out\]
</dt> <dd>

TRUE indica che la licenza può essere mantenute.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





