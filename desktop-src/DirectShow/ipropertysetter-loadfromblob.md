---
description: Il metodo LoadFromBlob carica i dati delle proprietà da un formato di persistenza.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'Metodo IPropertySetter:: LoadFromBlob (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a1e58aa5802e8fcb05c2464fc1f121ee1e86f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325478"
---
# <a name="ipropertysetterloadfromblob-method"></a>Metodo IPropertySetter:: LoadFromBlob

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `LoadFromBlob` metodo carica i dati della proprietà da un formato di persistenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cSize* \[ in\]
</dt> <dd>

Dimensioni dei dati in byte.

</dd> <dt>

*PB* \[ in\]
</dt> <dd>

Puntatore a una matrice di byte che contiene i dati.

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

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




