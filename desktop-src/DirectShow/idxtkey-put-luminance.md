---
description: Il \_ Metodo luminanza put specifica il valore della luminanza su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ luminanza.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: 'IDxtKey: metodo:p ut_Luminance (qedit. h)'
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
ms.openlocfilehash: 100f2352b88e9aae2f31ce969302f4bee0905f27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330399"
---
# <a name="idxtkeyput_luminance-method"></a>IDxtKey::p \_ metodo di luminanza UT

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_Luminance` metodo specifica il valore della luminanza su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ luminanza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ in\]
</dt> <dd>

Valore di luminanza su cui eseguire la chiave. L'intervallo valido è compreso tra 0 e 100.

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

 

 




