---
description: Il \_ metodo Put Filter specifica un filtro di origine per il rilevamento multimediale da usare.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'IMediaDet: metodo:p ut_Filter (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327822"
---
# <a name="imediadetput_filter-method"></a>IMediaDet: metodo di \_ filtro ut:p

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_Filter` metodo specifica un filtro di origine per il rilevamento multimediale da usare.

> [!IMPORTANT]
> Non aggiungere il filtro di origine al grafico di filtro oppure usare un filtro già presente in un grafico a filtro. L'oggetto Media Detector compila automaticamente un grafico di filtro interno e l'inserimento del filtro in un altro grafico può causare risultati imprevisti.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ in\]
</dt> <dd>

Puntatore all'interfaccia **IUnknown** del filtro di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I possibili valori sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                             |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | *newVal* non punta a un filtro.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null** .<br/>           |



 

## <a name="remarks"></a>Commenti

Per la maggior parte delle applicazioni, è più semplice chiamare il metodo [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) con il nome di un file di origine.

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

 

 




