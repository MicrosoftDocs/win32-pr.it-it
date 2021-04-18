---
title: Messaggio di ICM_SETSTATE (VFW. h)
description: Il \_ messaggio MCI sestate notifica a un driver di compressione video di impostare lo stato del compressore. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE messaggi multimediali di Windows
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
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302778"
---
# <a name="icm_setstate-message"></a>\_Messaggio di SESTATO ICM

Il messaggio **MCI \_ sestate** notifica a un driver di compressione video di impostare lo stato del compressore. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*PV*
</dt> <dd>

Puntatore a un blocco di memoria contenente i dati di configurazione. È possibile specificare **null** per questo parametro per ripristinare lo stato predefinito del compressore.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Dimensione, in byte, del blocco di memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di byte utilizzati dal compressore se ha esito positivo o zero in caso contrario.

## <a name="remarks"></a>Commenti

Le informazioni usate da questo messaggio sono private e specifiche di un compressore specificato. Le applicazioni client devono utilizzare questo messaggio solo per ripristinare le informazioni ottenute in precedenza con il messaggio [**ICM \_ GetState**](icm-getstate.md) e utilizzare il messaggio di configurazione [**ICM \_**](icm-configure.md) per modificare la configurazione di un driver di compressione video.

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

 

 





