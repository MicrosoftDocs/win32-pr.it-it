---
description: Il metodo get \_ Invert recupera un valore booleano che indica se l'operazione della chiave è invertita. Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ ALPHA.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: Metodo IDxtKey::get_Invert (Qedit.h)
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
ms.openlocfilehash: c5a862e062175d3c052a5003a2ced60fe5d3cc439bff76315e046fc2153f73af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083851"
---
# <a name="idxtkeyget_invert-method"></a>Metodo IDxtKey::get \_ Invert

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `get_Invert` metodo recupera un valore booleano che indica se l'operazione di chiave è invertita. Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ ALPHA.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Riceve uno dei valori seguenti.



| Valore     | Descrizione                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | I pixel nell'immagine sovraspetta vengono invertiti rispetto all'operazione predefinita. |
| **FALSE** | I pixel nell'immagine overlying vengono resi trasparenti nel modo predefinito.         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

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

[**Interfaccia IDxtKey**](idxtkey.md)
</dt> <dt>

[**IDxtKey::get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




