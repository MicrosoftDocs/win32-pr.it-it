---
description: Il \_ metodo Get InputSize restituisce le dimensioni di input correnti del filtro Resizer.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Metodo IResize:: get_InputSize (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332570"
---
# <a name="iresizeget_inputsize-method"></a>Metodo IResize:: Get \_ InputSize

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_InputSize` metodo restituisce le dimensioni di input correnti del filtro Resizer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
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

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se il pin di input del filtro non è connesso, restituire un codice di errore. In caso contrario, restituire la larghezza e l'altezza del video, come specificato dal tipo di supporto del PIN di input.

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

 

 




