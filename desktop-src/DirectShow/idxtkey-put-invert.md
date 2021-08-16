---
description: Il metodo put \_ Invert specifica se l'operazione chiave è invertita. Questa proprietà si applica a tutti i tipi di chiave, ad eccezione di DXTKEY \_ ALPHA.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: Metodo IDxtKey::p ut_Invert (Qedit.h)
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
ms.openlocfilehash: ed1ed445e7a6f5f1f07eff74ac739934f2c9ca1358affe3e0cd699b7a101f0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819438"
---
# <a name="idxtkeyput_invert-method"></a>Metodo IDxtKey::p ut \_ Invert

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `put_Invert` metodo specifica se l'operazione chiave è invertita. Questa proprietà si applica a tutti i tipi di chiave, ad eccezione di DXTKEY \_ ALPHA.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Specifica un valore booleano. Se **TRUE,** i pixel nell'immagine in e sovrasospetti vengono invertiti rispetto all'operazione predefinita. Se **FALSE,** i pixel nell'immagine sovrassinge vengono resi trasparenti nel modo predefinito.

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
</dt> <dt>

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




