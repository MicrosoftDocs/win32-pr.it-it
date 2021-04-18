---
description: Il \_ metodo Put Invert specifica se l'operazione di chiave è invertita. Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ alfa.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: 'IDxtKey: metodo:p ut_Invert (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326907"
---
# <a name="idxtkeyput_invert-method"></a>IDxtKey: metodo di \_ inversione:p UT

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_Invert` metodo specifica se l'operazione chiave è invertita. Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ alfa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ in\]
</dt> <dd>

Specifica un valore booleano. Se **true**, i pixel nell'immagine di sovrastanti vengono invertiti rispetto all'operazione predefinita. Se **false**, i pixel nell'immagine di sovrastanti vengono resi trasparenti nel modo predefinito.

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
</dt> <dt>

[**IDxtKey: tipo di:p di \_ tipo UT**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




