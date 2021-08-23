---
title: ICM_COMPRESS messaggio (Vfw.h)
description: Il ICM COMPRESS invia una notifica a un driver di compressione video per comprimere un \_ frame di dati in un buffer definito dall'applicazione.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS di messaggi Windows multimediali
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
ms.openlocfilehash: f1230f429eb49596dd8a450b8a384e0a69856b69c51141834458c09fa41ca54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678471"
---
# <a name="icm_compress-message"></a>\_ICM Messaggio COMPRESS

Il **ICM \_ COMPRESS invia** una notifica a un driver di compressione video per comprimere un frame di dati in un buffer definito dall'applicazione.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*Icc*
</dt> <dd>

Puntatore a [**una struttura ICCOMPRESS.**](/windows/desktop/api/Vfw/ns-vfw-iccompress) I membri seguenti di questa struttura specificano i parametri di compressione: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** e **dwQuality**. Il driver deve anche usare il membro **biSizeImage** della struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) associata a **lpbiOutput** di **ICCOMPRESS** per restituire le dimensioni del frame compresso.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Dimensioni, in byte, di [**ICCOMPRESS.**](/windows/desktop/api/Vfw/ns-vfw-iccompress)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

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

 

