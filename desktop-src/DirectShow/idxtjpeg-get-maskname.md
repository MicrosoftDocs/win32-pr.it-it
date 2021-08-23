---
description: Il metodo get \_ MaskName recupera il nome di un file JPEG da usare come maschera di cancellazione dati.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: Metodo IDxtJpeg::get_MaskName (Qedit.h)
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
ms.openlocfilehash: d984f426289b9017ca316567b474beaa41b39a35f0ab012ea94ffdd8db33a36b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584741"
---
# <a name="idxtjpegget_maskname-method"></a>Metodo IDxtJpeg::get \_ MaskName

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `get_MaskName` metodo recupera il nome di un file JPEG da usare come maschera di cancellazione dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve il nome del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se la transizione di cancellazione usa una delle cancellazioni SMPTE incorporate supportate, il valore di questa proprietà è una stringa vuota.

Il chiamante deve rilasciare la stringa restituita usando **la funzione SysFreeString.**

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

[**IDxtJpeg::get \_ MaskNum**](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




