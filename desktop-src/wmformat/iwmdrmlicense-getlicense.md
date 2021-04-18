---
title: Metodo GetLicense IWMDRMLicense (wmdrmsdk. h)
description: Il metodo GetLicense recupera la licenza come dati XML o XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Metodo GetLicense formato Windows Media
- Metodo GetLicense formato Windows Media, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328528"
---
# <a name="iwmdrmlicensegetlicense-method"></a>Metodo IWMDRMLicense:: GetLicense

Il metodo **GetLicense** recupera la licenza come dati XML o XMR.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppbLicense* \[ out\]
</dt> <dd>

Riceve la licenza.

</dd> <dt>

*pcbLicense* \[ out\]
</dt> <dd>

Riceve le dimensioni della licenza.

</dd> <dt>

*pdwLicenseType* \[ out\]
</dt> <dd>

Riceve il tipo della licenza restituita. Questo valore è impostato su una delle costanti nella tabella seguente.



| Costante                  | Descrizione                            |
|---------------------------|----------------------------------------|
| \_XML di \_ tipo di licenza WMDRM \_ | La licenza recuperata è formattata come XML. |
| \_tipo di licenza WMDRM \_ \_ XMR | La licenza recuperata è formattata come XMR. |



 

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
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





