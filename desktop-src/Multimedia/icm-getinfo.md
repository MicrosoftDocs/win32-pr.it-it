---
title: Messaggio di ICM_GETINFO (VFW. h)
description: Il \_ messaggio ICM GetInfo esegue una query su un driver di compressione video per restituirne una descrizione in una struttura ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO messaggi multimediali di Windows
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
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301759"
---
# <a name="icm_getinfo-message"></a>\_Messaggio ICM GETinfo

Il messaggio **ICM \_ GetInfo** esegue una query su un driver di compressione video per restituirne una descrizione in una struttura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

Puntatore a una struttura **ICINFO** per contenere informazioni.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Dimensioni, in byte, di **ICINFO**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la dimensione, in byte, di [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) o zero se si verifica un errore.

## <a name="remarks"></a>Commenti

In genere, le applicazioni inviano questo messaggio per visualizzare un elenco dei commediatori installati.

Il driver deve riempire tutti i membri della struttura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) ad eccezione di **szDriver**.

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

 

 





