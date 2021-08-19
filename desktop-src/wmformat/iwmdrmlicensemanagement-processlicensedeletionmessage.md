---
title: Metodo IWMDRMLicenseManagement ProcessLicenseDeletionMessage (Wmdrmsdk.h)
description: Il metodo ProcessLicenseDeletion elimina una licenza importata per il contenuto originariamente protetto con un altro sistema di protezione del contenuto.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Metodo ProcessLicenseDeletionMessage windows Media Format
- Metodo ProcessLicenseDeletionMessage windows Media Format , interfaccia IWMDRMLicenseManagement
- Metodo ProcessLicenseDeletionMessage dell'interfaccia IWMDRMLicenseManagement di Windows Media Format
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
ms.openlocfilehash: c369be95314ceaf3c4babce9dacd962fd3391d4f39f8988ef56f51fb3133aee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027589"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>Metodo IWMDRMLicenseManagement::P rocessLicenseDeletionMessage

Il **metodo ProcessLicenseDeletion** elimina una licenza importata per il contenuto originariamente protetto con un altro sistema di protezione del contenuto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDeletionMessage* \[ Pollici\]
</dt> <dd>

Messaggio che identifica la licenza da eliminare.

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

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





