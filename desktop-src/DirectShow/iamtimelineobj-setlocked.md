---
description: Il metodo selocked imposta lo stato di modifica dell'oggetto su bloccato o sbloccato.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'Metodo IAMTimelineObj:: selocked (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330818"
---
# <a name="iamtimelineobjsetlocked-method"></a>Metodo IAMTimelineObj:: selocked

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetLocked` metodo imposta lo stato di modifica dell'oggetto su bloccato o sbloccato.

Uno stato bloccato indica che l'oggetto non deve essere modificato. uno stato sbloccato indica che l'oggetto può essere modificato. La sequenza temporale non impone il blocco. L'impostazione bloccata esiste solo per praticità dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* 
</dt> <dd>

Valore booleano che specifica lo stato di modifica dell'oggetto. Se **true**, l'oggetto è bloccato e non deve essere modificato. Se **false**, l'oggetto è sbloccato e può essere modificato.

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




