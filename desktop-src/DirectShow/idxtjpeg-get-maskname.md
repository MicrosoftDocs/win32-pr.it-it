---
description: Il \_ metodo Get maskName Recupera il nome di un file JPEG da usare come maschera di cancellazione.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'Metodo IDxtJpeg:: get_MaskName (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325921"
---
# <a name="idxtjpegget_maskname-method"></a>Metodo IDxtJpeg:: Get \_ maskName

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_MaskName` metodo recupera il nome di un file JPEG da utilizzare come maschera di cancellazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve il nome del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se la transizione di cancellazione usa una delle cancellazioni SMPTE predefinite supportate, il valore di questa proprietà è una stringa vuota.

Il chiamante deve rilasciare la stringa restituita, usando la funzione **SysFreeString** .

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
</dt> <dt>

[**IDxtJpeg:: Get \_ MaskNum**](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




