---
description: Il \_ metodo Get Size restituisce le dimensioni di output e la modalità di estensione correnti.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'Metodo IResize:: get_Size (qedit. h)'
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
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332568"
---
# <a name="iresizeget_size-method"></a>Metodo IResize:: Get \_ size

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_Size` metodo restituisce le dimensioni di output e la modalità di estensione correnti.

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

*piHeight* \[ out\]
</dt> <dd>

Riceve l'altezza del video in pixel.

</dd> <dt>

*piWidth* \[ out\]
</dt> <dd>

Riceve la larghezza del video in pixel.

</dd> <dt>

*PFLAG* \[ out\]
</dt> <dd>

Riceve un flag che specifica la modalità di estensione. Per i valori possibili, vedere [**ridimensionare i flag**](resize-flags.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se il tipo di output non è stato impostato, il filtro deve restituire valori predefiniti. Questi valori possono essere scelti arbitrariamente in fase di progettazione.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9,0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IResize**](iresize.md)
</dt> </dl>

 

 




