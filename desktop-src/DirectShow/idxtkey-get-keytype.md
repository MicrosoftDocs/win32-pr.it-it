---
description: Il metodo get \_ KeyType recupera il tipo di chiave.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: Metodo IDxtKey::get_KeyType (Qedit.h)
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
ms.openlocfilehash: cfb8930df859771f61406ebab9a1e7f60cfdf149eaf66eae23120bb7292ebf74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819475"
---
# <a name="idxtkeyget_keytype-method"></a>Metodo IDxtKey::get \_ KeyType

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `get_KeyType` metodo recupera il tipo di chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve uno dei valori di enumerazione seguenti.



| Valore             | Descrizione                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | Tasto Chroma. (Chiave sul valore RGB.                       |
| DXTKEY \_ NONRED    | Chiave non ritirata. Rende trasparenti le aree blu e verdi. |
| DXTKEY \_ LUMINANCE | Chiave di luminanza.                                        |
| DXTKEY \_ ALPHA     | Chiave per valore alfa.                                   |
| TONALITÀ DXTKEY \_       | Chiave per tonalità.                                           |



 

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

[**Interfaccia IDxtKey**](idxtkey.md)
</dt> </dl>

 

 




