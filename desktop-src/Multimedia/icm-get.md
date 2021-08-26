---
title: ICM_GET messaggio (Vfw.h)
description: Il ICM GET recupera un valore DWORD definito dall'applicazione \_ da un driver di compressione video.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8885faf7b0605378ace3004165004384a582c9d49a0a8ce047122c108b6cb8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038731"
---
# <a name="icm_get-message"></a>\_ICM Messaggio GET

Il **ICM \_ GET** recupera un valore **DWORD** definito dall'applicazione da un driver di compressione video.


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Puntatore a un blocco di memoria da riempire con lo stato corrente. È anche possibile specificare **NULL** per determinare la quantità di memoria richiesta dalle informazioni sullo stato.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Dimensione, in byte, del blocco di memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la quantità di memoria, in byte, necessaria per archiviare le informazioni sullo stato.

## <a name="remarks"></a>Commenti

La struttura utilizzata per rappresentare le informazioni sullo stato è specifica del driver ed è definita dal driver.

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

 

 





