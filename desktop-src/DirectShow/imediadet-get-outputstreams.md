---
description: Il \_ metodo Get OutputStreams Recupera il numero di flussi audio e video contenuti nell'origine multimediale. Tutti gli altri tipi di flusso, ad esempio i flussi di dati, vengono ignorati.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'Metodo IMediaDet:: get_OutputStreams (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331504"
---
# <a name="imediadetget_outputstreams-method"></a>Metodo IMediaDet:: Get \_ OutputStreams

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_OutputStreams` metodo recupera il numero di flussi audio e video contenuti nell'origine multimediale. Tutti gli altri tipi di flusso, ad esempio i flussi di dati, vengono ignorati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve il numero di flussi di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) per impostare il nome del file. Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG. Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

 

 




