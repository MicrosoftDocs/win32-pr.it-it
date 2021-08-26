---
description: Il metodo get InputSize restituisce le dimensioni di \_ input correnti del filtro di ridimensionamento.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: Metodo IResize::get_InputSize (Qedit.h)
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
ms.openlocfilehash: 3b862237f8c51bdf6c22ca9acb667199fadee33b37e425efabfe25bdb8a20dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078931"
---
# <a name="iresizeget_inputsize-method"></a>Metodo IResize::get \_ InputSize

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo restituisce le dimensioni di input correnti `get_InputSize` del filtro di ridimensionamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
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

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se il pin di input del filtro non è connesso, restituire un codice di errore. In caso contrario, restituire la larghezza e l'altezza del video, come specificato dal tipo di supporto del segnaposto di input.

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

 

 




