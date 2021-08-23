---
description: Il metodo get ScaleY recupera la quantità di estensione verticale della \_ cancellazione.
ms.assetid: d8b80f19-2ec5-4d66-bd13-d6f7b5144345
title: Metodo IDxtJpeg::get_ScaleY (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3da97c829c8234a5bd0e8c9b82bf9a7f3334bca78de395be2e5724d8a52f4838
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639401"
---
# <a name="idxtjpegget_scaley-method"></a>Metodo IDxtJpeg::get \_ ScaleY

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `get_ScaleY` metodo recupera la quantità in base alla quale la cancellazione viene estesa verticalmente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ScaleY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve la quantità in base alla quale la cancellazione viene estesa verticalmente, come percentuale della definizione di cancellazione originale. Ad esempio, il valore 1,0 significa nessuna estensione e 2,0 significa 200% di estensione.

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

 

 




