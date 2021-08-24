---
title: ICM_SETSTATE messaggio (Vfw.h)
description: Il ICM messaggio SETSTATE notifica a un driver di compressione \_ video di impostare lo stato del compressore. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea6cd7aa0314520a30e293a8f029920c22b8baa58e995eed7ff9e5a96dd1b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525811"
---
# <a name="icm_setstate-message"></a>\_ICM Messaggio SETSTATE

Il **ICM \_ messaggio SETSTATE** notifica a un driver di compressione video di impostare lo stato del compressore. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICSetState.**](/windows/desktop/api/Vfw/nf-vfw-icsetstate)


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Puntatore a un blocco di memoria contenente i dati di configurazione. È possibile specificare **NULL per** questo parametro per ripristinare lo stato predefinito del compresso.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Dimensione, in byte, del blocco di memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di byte utilizzati dal flusso di lavoro in caso di esito positivo o zero in caso contrario.

## <a name="remarks"></a>Commenti

Le informazioni usate da questo messaggio sono private e specifiche di un determinato compresso. Le applicazioni client devono usare questo messaggio solo per ripristinare le informazioni ottenute in precedenza con il messaggio [**\_ ICM GETSTATE**](icm-getstate.md) e usare il messaggio [**ICM \_ CONFIGURE**](icm-configure.md) per modificare la configurazione di un driver di compressione video.

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

 

 





