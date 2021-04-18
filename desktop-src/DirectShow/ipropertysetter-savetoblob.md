---
description: Il metodo SaveToBlob Salva i dati della proprietà in un formato di persistenza.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'Metodo IPropertySetter:: SaveToBlob (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329623"
---
# <a name="ipropertysettersavetoblob-method"></a>Metodo IPropertySetter:: SaveToBlob

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SaveToBlob` metodo salva i dati della proprietà in un formato di persistenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcSize* \[ out\]
</dt> <dd>

Riceve le dimensioni dei dati in byte.

</dd> <dt>

*PPB* \[ out\]
</dt> <dd>

Riceve un puntatore a una matrice di byte che riceve i dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo alloca memoria per la matrice di byte. Il chiamante deve liberarlo, usando la funzione **CoTaskMemFree** .

Tutti i nomi e i valori delle proprietà vengono troncati con una lunghezza di 40 caratteri. Per questo motivo, XML è il formato di persistenza preferito. Vedere [**interfaccia IXml2Dex**](ixml2dex.md).

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

 

 




