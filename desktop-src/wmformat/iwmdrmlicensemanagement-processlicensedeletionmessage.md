---
title: Metodo IWMDRMLicenseManagement ProcessLicenseDeletionMessage (wmdrmsdk. h)
description: Il metodo ProcessLicenseDeletion Elimina una licenza che è stata importata per il contenuto originariamente protetto con un altro sistema di protezione del contenuto.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Metodo ProcessLicenseDeletionMessage Windows Media Format
- Metodo ProcessLicenseDeletionMessage Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo ProcessLicenseDeletionMessage
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327466"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>IWMDRMLicenseManagement::P metodo rocessLicenseDeletionMessage

Il metodo **ProcessLicenseDeletion** Elimina una licenza che è stata importata per il contenuto originariamente protetto con un altro sistema di protezione del contenuto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDeletionMessage* \[ in\]
</dt> <dd>

Messaggio che identifica la licenza da eliminare.

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

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





