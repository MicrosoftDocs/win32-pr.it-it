---
description: Il \_ metodo Get RGB Recupera il colore RGB su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Metodo IDxtKey:: get_RGB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326916"
---
# <a name="idxtkeyget_rgb-method"></a>Metodo IDxtKey:: Get \_ RGB

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_RGB` metodo recupera il colore RGB su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve il colore. Il valore restituito è un numero esadecimale con formato 0xRRGGBB, dove RR è il valore rosso, GG è il valore verde e BB è il valore blu.

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

[**Interfaccia IDxtKey**](idxtkey.md)
</dt> <dt>

[**Tipo di IDxtKey:: Get \_**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




