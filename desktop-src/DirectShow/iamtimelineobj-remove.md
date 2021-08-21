---
description: Il metodo Remove rimuove questo oggetto dalla sequenza temporale (inclusi gli oggetti secondari ma non gli elementi figlio), per la reinserzione altrove.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: Metodo IAMTimelineObj::Remove (Qedit.h)
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
ms.openlocfilehash: 356f7239cbdbe3972f11fcc95dd9bf44dc1b06d086a8e44c9131c0061f3ec211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155264"
---
# <a name="iamtimelineobjremove-method"></a>Metodo IAMTimelineObj::Remove

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il metodo rimuove questo oggetto dalla sequenza temporale (inclusi i sottooggetti ma non gli elementi figlio), per la `Remove` reinserzione altrove.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Chiamare questo metodo solo se l'applicazione inserirà immediatamente l'oggetto nella sequenza temporale. Si tratta di un'operazione non valida per chiamare questo metodo senza quindi reinserire l'oggetto . Per rimuovere un oggetto in modo permanente, chiamare [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




