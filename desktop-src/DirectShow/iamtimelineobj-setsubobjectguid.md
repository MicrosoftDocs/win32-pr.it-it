---
description: Il metodo SetSubObjectGUID specifica il GUID dell'oggetto SubObject associato a questo oggetto.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'Metodo IAMTimelineObj:: SetSubObjectGUID (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330803"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a>Metodo IAMTimelineObj:: SetSubObjectGUID

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetSubObjectGUID` metodo specifica il GUID dell'oggetto SubObject associato a questo oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

GUID dell'oggetto SubObject.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il motore di rendering crea un'istanza dell'oggetto sottooggetto in base alle esigenze.

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




