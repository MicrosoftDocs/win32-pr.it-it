---
description: Il metodo GetSubObject recupera l'oggetto SubObject associato a questo oggetto.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'Metodo IAMTimelineObj:: GetSubObject (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328154"
---
# <a name="iamtimelineobjgetsubobject-method"></a>Metodo IAMTimelineObj:: GetSubObject

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetSubObject` metodo recupera l'oggetto SubObject associato a questo oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve un puntatore all'interfaccia **IUnknown** dell'oggetto. Se l'oggetto non dispone di un oggetto SubObject, il valore viene impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Ogni oggetto sequenza temporale può avere un puntatore a un oggetto SubObject associato.

Se il valore restituito in *pval* non è **null**, l'interfaccia **IUnknown** presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




