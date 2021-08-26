---
description: Il metodo SetStreamNumber specifica il flusso da leggere dal file di origine associato a questo oggetto di origine.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: Metodo IAMTimelineSrc::SetStreamNumber (Qedit.h)
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
ms.openlocfilehash: ae313121831dc2855a2f07ba3c7727e87736b77a8c5f98078d2237bb9520cf6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982961"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>Metodo IAMTimelineSrc::SetStreamNumber

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

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

Numero di flusso, dal set di flussi corrispondente al tipo di supporto del gruppo padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il *parametro Val* specifica un numero di flusso dal set di flussi che corrisponde al tipo di supporto del gruppo padre, non dall'intero set di flussi nel file di origine. Si supponga, ad esempio, che un file contenga due flussi video e due flussi audio. Se l'oggetto di origine si trova all'interno di un gruppo di video, impostando *Val* su 0 viene selezionato il primo flusso video. Il chiamante è responsabile della specifica di un numero di flusso valido.

Per impostazione predefinita, il numero di flusso è zero.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




