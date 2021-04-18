---
description: Il \_ metodo RGB put specifica il colore RGB su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: 'IDxtKey: metodo:p ut_RGB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329631"
---
# <a name="idxtkeyput_rgb-method"></a>IDxtKey: \_ metodo RGB ut:p

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_RGB` metodo specifica il colore RGB su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ in\]
</dt> <dd>

Specifica il colore come numero esadecimale con formato 0xRRGGBB, dove RR è il valore rosso, GG è il valore verde e BB è il valore blu.

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

[**IDxtKey: tipo di:p di \_ tipo UT**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




