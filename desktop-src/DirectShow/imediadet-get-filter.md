---
description: Il metodo get \_ Filter recupera un puntatore al filtro di origine attualmente usato dal rilevatore di supporti.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: Metodo IMediaDet::get_Filter (Qedit.h)
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
ms.openlocfilehash: c3d4622438dbb8c8dfc54183550c274fcd4555de8b75435b85bbbebfae9c2c1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083761"
---
# <a name="imediadetget_filter-method"></a>Metodo IMediaDet::get \_ Filter

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `get_Filter` metodo recupera un puntatore al filtro di origine attualmente usato dal rilevatore di supporti.

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

Riceve un puntatore all'interfaccia **IUnknown del** filtro. Se non è in uso alcun filtro di origine, il valore viene impostato su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Quando il metodo termina, se *\* ppVal* non è **NULL,** **l'interfaccia IUnknown** ha un conteggio dei riferimenti in sospeso. Al termine dell'uso, rilasciare l'interfaccia .

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMediaDet**](imediadet.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




