---
title: Messaggio di ICM_DRAW_QUERY (VFW. h)
description: Il \_ \_ messaggio di query di estrazione ICM esegue una query su un driver di rendering per determinare se è possibile eseguire il rendering dei dati in un formato specifico. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477255"
---
# <a name="icm_draw_query-message"></a>Messaggio di query di \_ estrazione ICM \_

Il messaggio di **\_ \_ query di estrazione ICM** esegue una query su un driver di rendering per determinare se è possibile eseguire il rendering dei dati in un formato specifico. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se il driver è in grado di eseguire il rendering dei dati nel formato specificato o in ICERR \_ BADFORMAT in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio è diverso dal messaggio [**di \_ \_ inizio del progetto ICM**](icm-draw-begin.md) in quanto esegue una query sul driver in senso generale. **ICM \_ L' \_ inizio dell'estrazione** determina se il driver può creare i dati utilizzando il formato specificato in condizioni specifiche, ad esempio l'estensione dell'immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

