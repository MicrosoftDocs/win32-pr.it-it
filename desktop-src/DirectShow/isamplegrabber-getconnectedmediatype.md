---
description: Il metodo GetConnectedMediaType recupera il tipo di supporto per la connessione sul pin di input di Sample Grabber.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: Metodo ISampleGrabber::GetConnectedMediaType (Qedit.h)
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
ms.openlocfilehash: 03dc0c9763bdea75569f9447becb749bf284ae2ad7d77427f6dfc2f0aac58382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818060"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>Metodo ISampleGrabber::GetConnectedMediaType

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetConnectedMediaType` metodo recupera il tipo di supporto per la connessione sul pin di input di Sample Grabber.

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

Puntatore a una [**\_ struttura AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata dal chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                                           | Descrizione                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>             | Argomento del puntatore **NULL.**<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il filtro non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo copia il tipo di supporto nella struttura **AM \_ MEDIA \_ TYPE** specificata da *pType.* Il chiamante deve liberare il blocco di formato del tipo di supporto. È possibile usare **la funzione CoTaskMemFree** o [**la funzione FreeMediaType**](freemediatype.md) nella libreria di classi base.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaccia ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




