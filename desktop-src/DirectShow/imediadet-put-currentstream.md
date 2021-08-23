---
description: Il metodo put CurrentStream specifica il numero di flusso da usare per \_ il rilevamento multimediale.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: Metodo IMediaDet::p ut_CurrentStream (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ba8b9cfe7cf898e9645d0f1caf8ef789bb45967bfc268f08555a5bdea53c4127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952600"
---
# <a name="imediadetput_currentstream-method"></a>Metodo IMediaDet::p ut \_ CurrentStream

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `put_CurrentStream` metodo specifica il numero di flusso da usare per il rilevamento multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Numero di flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) per impostare il nome del file. Chiamare [**IMediaDet::get \_ OutputStreams**](imediadet-get-outputstreams.md) per determinare il numero di flussi contenuti nel file di origine.

Se il rilevatore di supporti è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG. Per altre informazioni, vedere [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

 

 




