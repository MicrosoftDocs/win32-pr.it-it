---
description: Il metodo put \_ Luminance specifica il valore di luminance su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ LUMINANCE.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: Metodo IDxtKey::p ut_Luminance (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae51fe72220355cb6e206ea437f547a0a8ca2d77633195debeb364f17e7f136f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819384"
---
# <a name="idxtkeyput_luminance-method"></a>Metodo IDxtKey::p ut \_ Luminance

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `put_Luminance` metodo specifica il valore di luminance su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ LUMINANCE.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Valore di luminance su cui eseguire la chiave. L'intervallo valido è compreso tra 0 e 100.

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

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




