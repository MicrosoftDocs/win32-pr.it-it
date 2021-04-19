---
description: Il metodo SetStreamNumber specifica il flusso da leggere dal file di origine associato a questo oggetto di origine.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'Metodo IAMTimelineSrc:: SetStreamNumber (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330177"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>Metodo IAMTimelineSrc:: SetStreamNumber

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetStreamNumber` metodo specifica il flusso da leggere dal file di origine associato a questo oggetto di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Val* 
</dt> <dd>

Il numero di flusso, dal set di flussi che corrispondono al tipo di supporto del gruppo padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il parametro *Val* specifica un numero di flusso dal set di flussi che corrisponde al tipo di supporto del gruppo padre, non dall'intero set di flussi nel file di origine. Si supponga, ad esempio, che un file contenga due flussi video e due flussi audio. Se l'oggetto di origine si trova all'interno di un gruppo video, impostando *Val* su 0 viene selezionato il primo flusso video. Il chiamante è responsabile della specifica di un numero di flusso valido.

Il valore predefinito per il numero di flusso è zero.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




