---
title: Messaggio di ICM_GETSTATE (VFW. h)
description: Il \_ messaggio ICM GetState esegue una query su un driver di compressione video per restituire la configurazione corrente in un blocco di memoria o per determinare la quantità di memoria necessaria per recuperare le informazioni di configurazione.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121683"
---
# <a name="icm_getstate-message"></a>\_Messaggio ICM GETstate

Il messaggio **ICM \_ GetState** esegue una query su un driver di compressione video per restituire la configurazione corrente in un blocco di memoria o per determinare la quantità di memoria necessaria per recuperare le informazioni di configurazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*PV*
</dt> <dd>

Puntatore a un blocco di memoria per contenere le informazioni di configurazione correnti. È possibile specificare **null** per questo parametro per determinare la quantità di memoria richiesta per le informazioni di configurazione, come in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Dimensione, in byte, del blocco di memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se *PV* è **null**, restituisce la quantità di memoria, in byte, necessaria per le informazioni di configurazione.

Se *PV* non è **null**, restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

La struttura utilizzata per rappresentare le informazioni di configurazione è specifica del driver e viene definita dal driver.

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

 

 





