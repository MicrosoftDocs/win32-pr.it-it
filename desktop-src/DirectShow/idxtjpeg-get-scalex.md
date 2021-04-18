---
description: Il \_ metodo Get ScaleX Recupera il valore in base al quale la cancellazione viene allungata orizzontalmente.
ms.assetid: 74c3f60b-68d9-4a8e-a6e5-767ce281a9fb
title: 'Metodo IDxtJpeg:: get_ScaleX (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0532e3c068c0ea9641d1fffbcc3d1327290bae02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328151"
---
# <a name="idxtjpegget_scalex-method"></a>Metodo IDxtJpeg:: Get \_ ScaleX

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_ScaleX` metodo recupera il valore in base al quale la cancellazione viene allungata orizzontalmente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ScaleX(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve il valore in base al quale la cancellazione viene allungata orizzontalmente, come percentuale della definizione di cancellazione originale. Ad esempio, il valore 1,0 indica l'assenza di un'estensione e 2,0 indica l'estensione del 200%.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

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

[**Interfaccia IDxtJpeg**](idxtjpeg.md)
</dt> </dl>

 

 




