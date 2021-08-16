---
description: Il metodo get MediaType restituisce il tipo di supporto di output corrente \_ del filtro di ridimensionamento.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: Metodo IResize::get_MediaType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d9e23c78a25f1cda141cb0c3ce55688c12bdf3aab447aca596326e01544b4e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818232"
---
# <a name="iresizeget_mediatype-method"></a>Metodo IResize::get \_ MediaType

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il metodo restituisce il tipo di supporto di output corrente `get_MediaType` del filtro di ridimensionamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pmt* \[ Cambio\]
</dt> <dd>

Puntatore a una [**\_ struttura AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata dal chiamante. Il metodo riempie questa struttura con il tipo di supporto. Il chiamante deve rilasciare il blocco di formato, se presente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se il tipo di supporto di output non è stato impostato, restituire un tipo di supporto predefinito. Il filtro deve aggiornare il tipo di supporto di output quando vengono chiamati i metodi **put \_ MediaType** o **put \_ Size.** Il tipo di supporto restituito da `get_MediaType` deve riflettere queste modifiche.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9.0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IResize**](iresize.md)
</dt> </dl>

 

 




