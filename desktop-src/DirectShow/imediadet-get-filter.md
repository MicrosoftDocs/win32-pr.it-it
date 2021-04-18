---
description: Il \_ metodo Get Filter recupera un puntatore al filtro di origine attualmente utilizzato dal rilevamento multimediale.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Metodo IMediaDet:: get_Filter (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331507"
---
# <a name="imediadetget_filter-method"></a>Metodo IMediaDet:: Get \_ Filter

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_Filter` metodo recupera un puntatore al filtro di origine attualmente utilizzato dal rilevamento multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppVal* \[ out, retval\]
</dt> <dd>

Riceve un puntatore all'interfaccia **IUnknown** del filtro. Se non è in uso alcun filtro di origine, il valore viene impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Quando il metodo restituisce un risultato, se *\* ppVal* non è **null**, l'interfaccia **IUnknown** presenta un conteggio dei riferimenti in attesa. Rilasciare l'interfaccia al termine dell'utilizzo.

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

[**Interfaccia IMediaDet**](imediadet.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




