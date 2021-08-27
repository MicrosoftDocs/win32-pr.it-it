---
description: Il metodo get \_ BorderWidth recupera la larghezza del bordo a tinta unita lungo i bordi del modello di cancellazione.
ms.assetid: 85c62524-5936-475e-a73b-7a3c926bb5f0
title: Metodo IDxtJpeg::get_BorderWidth (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32f2632c62cadd717232e2febc9ed7e834b7ea11c38fa49522e05b2383cb845d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131061"
---
# <a name="idxtjpegget_borderwidth-method"></a>Metodo IDxtJpeg::get \_ BorderWidth

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo recupera la larghezza del bordo a `get_BorderWidth` tinta unita lungo i bordi del modello di cancellazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_BorderWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve la larghezza del bordo, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

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

[**Interfaccia IDxtJpeg**](idxtjpeg.md)
</dt> </dl>

 

 




