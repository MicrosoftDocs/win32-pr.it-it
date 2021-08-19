---
title: Metodo IWMDRMLicenseManagement StoreLicense (Wmdrmsdk.h)
description: Il metodo StoreLicense include una licenza generata all'esterno del sottosistema DRM locale nell'archivio licenze locale.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Metodo StoreLicense windows Media Format
- Metodo StoreLicense windows Media Format , interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement windows Media Format , metodo StoreLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c509fdbc89acfd2d31ad5ead7ce63cd7f3b501b304d82240475c845c013e03b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655049"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>Metodo IWMDRMLicenseManagement::StoreLicense

Il **metodo StoreLicense** include una licenza generata all'esterno del sottosistema DRM locale nell'archivio licenze locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrLicenseResponse* \[ Pollici\]
</dt> <dd>

Stringa di risposta della licenza da decodificare e aggiungere all'archivio licenze locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile usare questo metodo per aggiungere licenze XMR create all'archivio licenze locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





