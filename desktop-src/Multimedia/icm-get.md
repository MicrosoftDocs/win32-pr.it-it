---
title: Messaggio di ICM_GET (VFW. h)
description: Il \_ messaggio ICM Get recupera un valore DWORD definito dall'applicazione da un driver di compressione video.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET messaggi multimediali di Windows
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
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740495"
---
# <a name="icm_get-message"></a>\_Messaggio ICM Get

Il messaggio **ICM \_ Get** recupera un valore **DWORD** definito dall'applicazione da un driver di compressione video.


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*PV*
</dt> <dd>

Puntatore a un blocco di memoria da riempire con lo stato corrente. È anche possibile specificare **null** per determinare la quantità di memoria richiesta dalle informazioni sullo stato.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
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
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





