---
description: Il metodo put \_ KeyType specifica il tipo di chiave.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: Metodo IDxtKey::p ut_KeyType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e75a99f3920d129416521f99557835d5e1e9827260b85ef25e20b951ff7b2831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998616"
---
# <a name="idxtkeyput_keytype-method"></a>Metodo IDxtKey::p ut \_ KeyType

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `put_KeyType` metodo specifica il tipo di chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Specifica il tipo di chiave. Questo parametro deve essere uno dei valori di enumerazione seguenti.



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

 

 




