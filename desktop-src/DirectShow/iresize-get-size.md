---
description: Il metodo get \_ Size restituisce le dimensioni di output correnti e la modalità stretch.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: Metodo IResize::get_Size (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 747ca8d7fd839321a9dbf4403c503652b932403e49bb964ae6148da2f49c5ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818212"
---
# <a name="iresizeget_size-method"></a>Metodo IResize::get \_ Size

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `get_Size` metodo restituisce le dimensioni di output correnti e la modalità stretch.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*piHeight* \[ Cambio\]
</dt> <dd>

Riceve l'altezza del video, in pixel.

</dd> <dt>

*piWidth* \[ Cambio\]
</dt> <dd>

Riceve la larghezza del video, in pixel.

</dd> <dt>

*pFlag* \[ Cambio\]
</dt> <dd>

Riceve un flag che specifica la modalità stretch. Per [**i valori possibili,**](resize-flags.md) vedere Flag di ridimensionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se il tipo di output non è stato impostato, il filtro deve restituire i valori predefiniti. Questi valori possono essere scelti arbitrariamente in fase di progettazione.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

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

 

 




