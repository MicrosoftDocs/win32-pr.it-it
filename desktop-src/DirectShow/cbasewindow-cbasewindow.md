---
description: 'Costruttore CBaseWindow.CBaseWindow : metodo costruttore.'
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Costruttore CBaseWindow.CBaseWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8873ee896d910d1596138a8d116c93ae0190534bac48b6ceb19165074f07b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016749"
---
# <a name="cbasewindowcbasewindow-constructor"></a>Costruttore CBaseWindow.CBaseWindow

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bDoGetDC* 
</dt> <dd>

Valore booleano che specifica se recuperare il contesto di dispositivo.

</dd> <dt>

*bPostToDestroy* 
</dt> <dd>

Valore booleano che specifica la [**variabile membro CBaseWindow::m \_ bDoPostToDestroy.**](cbasewindow-m-bdoposttodestroy.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Dopo aver creato l'oggetto, chiamare il metodo [**CBaseWindow::P repareWindow**](cbasewindow-preparewindow.md) per creare la finestra. **PrepareWindow** è un metodo virtuale. Chiama [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), anche un metodo virtuale. Questi metodi sono separati dal costruttore in modo che le classi derivate possano eseguirne l'override, se necessario.

Se il valore del parametro *bDoGetDC* è **TRUE,** l'oggetto recupera un handle per il contesto di dispositivo della finestra e lo archivia nella variabile membro `CBaseWindow` [**CBaseWindow::m \_ hdc.**](cbasewindow-m-hdc.md) L'oggetto crea anche un controller di dominio di memoria compatibile, archiviato nella variabile membro [**CBaseWindow::m \_ MemoryDC.**](cbasewindow-m-memorydc.md) Queste azioni si verificano **nel metodo InitialiseWindow.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




