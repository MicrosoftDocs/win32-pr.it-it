---
title: ICM_GETSTATE messaggio (Vfw.h)
description: Il ICM GETSTATE esegue una query su un driver di compressione video per restituire la configurazione corrente in un blocco di memoria o per determinare la quantità di memoria necessaria per recuperare le \_ informazioni di configurazione.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE messaggio Windows Multimediali
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
ms.openlocfilehash: c9bf21d808752b8a3ac3ba71a8593cd6dc577b3af4f34f421682d126c73b3578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784951"
---
# <a name="icm_getstate-message"></a>\_ICM Messaggio GETSTATE

Il **ICM \_ GETSTATE** esegue una query su un driver di compressione video per restituire la configurazione corrente in un blocco di memoria o per determinare la quantità di memoria necessaria per recuperare le informazioni di configurazione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICGetState.**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Puntatore a un blocco di memoria per contenere le informazioni di configurazione correnti. È possibile specificare **NULL** per questo parametro per determinare la quantità di memoria necessaria per le informazioni di configurazione, come in [**ICGetStateSize.**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize)

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Dimensione, in byte, del blocco di memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se *pv* è **NULL,** restituisce la quantità di memoria, in byte, necessaria per le informazioni di configurazione.

Se *pv non* è **NULL,** restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

La struttura utilizzata per rappresentare le informazioni di configurazione è specifica del driver ed è definita dal driver.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





