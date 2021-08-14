---
description: Il metodo put Filter specifica un filtro di origine da usare per \_ il rilevamento multimediale.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: Metodo IMediaDet::p ut_Filter (Qedit.h)
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
ms.openlocfilehash: a118baae251bd4456dfe0097afa091e0084e41ad96d96c9847006b8ce9c58d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398118"
---
# <a name="imediadetput_filter-method"></a>Metodo IMediaDet::p ut \_ Filter

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `put_Filter` metodo specifica un filtro di origine da usare per il rilevamento multimediale.

> [!IMPORTANT]
> Non aggiungere il filtro di origine al proprio grafico filtri o usare un filtro già presente in un grafico filtri. L'oggetto rilevamento multimediale crea automaticamente un grafico di filtro interno e l'inserimento del filtro in un altro grafico può causare risultati imprevisti.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Puntatore all'interfaccia **IUnknown** del filtro di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I possibili valori sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *newVal* non punta a un filtro.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Argomento del puntatore **NULL.**<br/>           |



 

## <a name="remarks"></a>Commenti

Per la maggior parte delle applicazioni, è più semplice chiamare il metodo [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) con il nome di un file di origine.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

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

 

 




