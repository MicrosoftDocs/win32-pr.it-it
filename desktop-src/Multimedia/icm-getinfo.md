---
title: ICM_GETINFO messaggio (Vfw.h)
description: Il ICM GETINFO esegue una query su un driver di compressione video per restituire una descrizione di se \_ stesso in una struttura ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173f510642b807a0e4c4a8c5c84d6d4de2aa7ce55cc0707eccabf5421cf98a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690811"
---
# <a name="icm_getinfo-message"></a>\_ICM Messaggio GETINFO

Il **ICM \_ GETINFO** esegue una query su un driver di compressione video per restituire una descrizione di se stesso in una [**struttura ICINFO.**](/windows/desktop/api/Vfw/ns-vfw-icinfo)


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

Puntatore a una **struttura ICINFO** per contenere informazioni.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Dimensione, in byte, di **ICINFO.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la dimensione, in byte, di [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) o zero se si verifica un errore.

## <a name="remarks"></a>Commenti

In genere, le applicazioni inviano questo messaggio per visualizzare un elenco degli elementi installati.

Il driver deve compilare tutti i membri della [**struttura ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) ad eccezione **di szDriver**.

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

 

 





