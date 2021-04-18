---
description: Il \_ metodo Get chiave Type recupera il tipo di chiave.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Metodo IDxtKey:: get_KeyType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326919"
---
# <a name="idxtkeyget_keytype-method"></a>Metodo IDxtKey:: Get \_ DataType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_KeyType` metodo recupera il tipo di chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve uno dei seguenti valori di enumerazione.



| Valore             | Descrizione                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | Tasto Chroma. (Chiave su valore RGB).                       |
| \_NONRED DXTKEY    | Chiave di Nonred. (Rende trasparenti le aree blu e verde). |
| \_luminanza DXTKEY | Chiave di luminanza.                                        |
| DXTKEY \_ alfa     | Chiave per valore alfa.                                   |
| \_tonalità DXTKEY       | Chiave per tonalità.                                           |



 

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
</dt> </dl>

 

 




