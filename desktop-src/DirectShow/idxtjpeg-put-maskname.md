---
description: Il metodo put \_ MaskName specifica il nome di un file JPEG da usare come maschera di cancellazione dati.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: Metodo IDxtJpeg::p ut_MaskName (Qedit.h)
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
ms.openlocfilehash: 7a43398020c49f2a6dab1cd56fc0244c4be88e2e45e38e0f6bd63c119bbf66a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755941"
---
# <a name="idxtjpegput_maskname-method"></a>Metodo IDxtJpeg::p ut \_ MaskName

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `put_MaskName` metodo specifica il nome di un file JPEG da usare come maschera di cancellazione dati. Questa maschera verrà usata al posto di una delle maschere di cancellazione incorporate. Il file deve contenere una sfumatura monocromatica a 8 bit per pixel. La sfumatura viene usata come maschera per definire l'avanzamento della cancellazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Specifica il nome del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Per ripristinare una maschera predefinita, impostare la **proprietà MaskNum.**

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IDxtJpeg**](idxtjpeg.md)
</dt> <dt>

[**IDxtJpeg::put \_ MaskNum**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




