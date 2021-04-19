---
description: Il \_ metodo Put maskName specifica il nome di un file JPEG da usare come maschera di cancellazione.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'IDxtJpeg: metodo:p ut_MaskName (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329251"
---
# <a name="idxtjpegput_maskname-method"></a>IDxtJpeg::p UT \_ maskName metodo

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_MaskName` metodo specifica il nome di un file JPEG da usare come maschera di cancellazione. Questa maschera verrà utilizzata al posto di una delle maschere di cancellazione predefinite. Il file deve contenere una sfumatura monocromatica a 8 bit per pixel. La sfumatura viene utilizzata come maschera per definire la progressione della cancellazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ in\]
</dt> <dd>

Specifica il nome del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Per ripristinare una maschera predefinita, impostare la proprietà **MaskNum** .

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

[**IDxtJpeg::p UT \_ MaskNum**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




