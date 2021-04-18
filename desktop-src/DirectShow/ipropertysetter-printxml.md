---
description: Il metodo PrintXML converte i dati della proprietà in una stringa XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: Metodo IPropertySetter::P rintXML (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329628"
---
# <a name="ipropertysetterprintxml-method"></a>IPropertySetter::P metodo rintXML

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `PrintXML` metodo converte i dati della proprietà in una stringa XML.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszXML* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve la stringa XML.

</dd> <dt>

*cbXML* \[ in\]
</dt> <dd>

Dimensioni del buffer a cui punta *pszXML* in byte.

</dd> <dt>

*pcbPrinted* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve la lunghezza della stringa XML. Può essere **null**.

</dd> <dt>

*rientro* \[ in\]
</dt> <dd>

Numero di livelli di rientro per il tag più esterno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo. In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore. Se la stringa XML è più lunga del buffer, il metodo restituisce E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




