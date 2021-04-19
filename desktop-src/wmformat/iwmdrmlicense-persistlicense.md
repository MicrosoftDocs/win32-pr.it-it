---
title: Metodo IWMDRMLicense PersistLicense (wmdrmsdk. h)
description: Il metodo PersistLicense salva la licenza corrente dall'archivio temporaneo nell'archivio licenze locale permanente.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Metodo PersistLicense Windows Media Format
- Metodo PersistLicense Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo PersistLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327697"
---
# <a name="iwmdrmlicensepersistlicense-method"></a>IWMDRMLicense::P metodo ersistLicense

Il metodo **PersistLicense** salva la licenza corrente dall'archivio temporaneo nell'archivio licenze locale permanente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se la licenza corrente non è presente nell'archivio temporaneo, questo metodo avrà esito negativo.

È possibile chiamare [**CanPersist**](iwmdrmlicense-canpersist.md) per eseguire una query per verificare se la licenza è consentita per essere resa permanente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





