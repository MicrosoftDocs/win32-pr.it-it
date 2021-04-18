---
title: Metodo IWMDRMLicenseManagement StoreLicense (wmdrmsdk. h)
description: Il metodo StoreLicense include una licenza che è stata generata all'esterno del sottosistema DRM locale nell'archivio licenze locale.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Metodo StoreLicense Windows Media Format
- Metodo StoreLicense Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo StoreLicense
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
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325560"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>Metodo IWMDRMLicenseManagement:: StoreLicense

Il metodo **StoreLicense** include una licenza che è stata generata all'esterno del sottosistema DRM locale nell'archivio licenze locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrLicenseResponse* \[ in\]
</dt> <dd>

Stringa di risposta della licenza da decodificare e aggiungere all'archivio licenze locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile utilizzare questo metodo per aggiungere licenze XMR create all'archivio licenze locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





