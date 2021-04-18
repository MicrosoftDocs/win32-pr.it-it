---
description: Il \_ metodo Get Invert recupera un valore booleano che indica se l'operazione del tasto è invertita. Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ alfa.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Metodo IDxtKey:: get_Invert (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326921"
---
# <a name="idxtkeyget_invert-method"></a>Metodo IDxtKey:: Get \_ Invert

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_Invert` metodo recupera un valore booleano che indica se l'operazione del tasto è invertita. Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ alfa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve uno dei valori seguenti.



| Valore     | Descrizione                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | I pixel nell'immagine sovrastante vengono invertiti rispetto all'operazione predefinita. |
| **FALSE** | I pixel nell'immagine di sovrastanti vengono resi trasparenti nel modo predefinito.         |



 

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

[**Tipo di IDxtKey:: Get \_**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




