---
description: 'Il metodo SetMediaLength2 specifica la durata del file di origine. Questo metodo è equivalente a IAMTimelineSrc:: SetMediaLength, ma accetta un valore REFTIME.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'Metodo IAMTimelineSrc:: SetMediaLength2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330182"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a>Metodo IAMTimelineSrc:: SetMediaLength2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetMediaLength2` metodo specifica la durata del file di origine. Questo metodo è equivalente a [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md), ma accetta un valore [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Length* 
</dt> <dd>

Lunghezza del supporto, in secondi.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




