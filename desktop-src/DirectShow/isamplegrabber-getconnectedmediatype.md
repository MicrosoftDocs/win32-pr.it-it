---
description: Il metodo GetConnectedMediaType Recupera il tipo di supporto per la connessione sul pin di input del grabber di esempio.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'Metodo ISampleGrabber:: GetConnectedMediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325297"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>Metodo ISampleGrabber:: GetConnectedMediaType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetConnectedMediaType` metodo recupera il tipo di supporto per la connessione sul pin di input del grabber di esempio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pType* 
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata dal chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                           | Descrizione                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_puntatore E**</dt> </dl>             | Argomento puntatore **null** .<br/>   |
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                     |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il filtro non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo copia il tipo di supporto nella struttura del **\_ \_ tipo di supporto am** specificata da *pType*. Il chiamante deve liberare il blocco di formato del tipo di supporto. È possibile usare la funzione **CoTaskMemFree** o la funzione [**FreeMediaType**](freemediatype.md) nella libreria di classi di base.

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

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaccia ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




