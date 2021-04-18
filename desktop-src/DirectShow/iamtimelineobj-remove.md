---
description: Il metodo Remove rimuove questo oggetto dalla sequenza temporale (inclusi gli oggetti figlio), per il reinserimento altrove.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'Metodo IAMTimelineObj:: Remove (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330824"
---
# <a name="iamtimelineobjremove-method"></a>Metodo IAMTimelineObj:: Remove

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `Remove` metodo rimuove l'oggetto dalla sequenza temporale (inclusi gli oggetti figlio), per il reinserimento altrove.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Chiamare questo metodo solo se l'applicazione inserisce immediatamente nuovamente l'oggetto nella sequenza temporale. Non è un'operazione valida chiamare questo metodo senza reinserire l'oggetto. Per rimuovere un oggetto in modo permanente, chiamare [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md).

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

 

 




