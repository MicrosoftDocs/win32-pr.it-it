---
title: Messaggio di ICM_COMPRESS (VFW. h)
description: Il messaggio MCI Compress invia una \_ notifica a un driver di compressione video per comprimere un frame di dati in un buffer definito dall'applicazione.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302272"
---
# <a name="icm_compress-message"></a>\_Messaggio di compressione ICM

Il messaggio **MCI \_ Compress** invia una notifica a un driver di compressione video per comprimere un frame di dati in un buffer definito dall'applicazione.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*ICC*
</dt> <dd>

Puntatore a una struttura [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) . I membri seguenti di questa struttura specificano i parametri di compressione: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** e **dwQuality**. Il driver deve anche usare il membro **biSizeImage** della struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) associata a **lpbiOutput** di **ICCOMPRESS** per restituire le dimensioni del frame compresso.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Dimensioni, in byte, di [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

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

 

