---
description: Callback che notifica all'host le informazioni di framebuffer restituite dalla richiesta associata.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IFrameBufferCallback::ResultCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 69f577ec182144a59a7c879a56e8222911ec3fa56b979b5d7a6e7d1e68982ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484957"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Metodo IFrameBufferCallback::ResultCallback

Callback che notifica all'host le informazioni di framebuffer restituite dalla richiesta associata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a>Parametri

*frameNumber*   
Numero di frame.

*Larghezza*   
Larghezza del frame.

*Altezza*   
Altezza del frame.

*renderTargetPtr*   
Destinazione di rendering da cui provengono i risultati. Si tratta sempre di uno slot specificato dalla richiesta del buffer dei frame o, in caso contrario, di una chiamata di disegno, il primo elemento RTV all'origine di output.

*frameDuraction*   
Non usato.

*Dimensione*   
Dimensioni del buffer di output in byte.

*buffer \_ count5*   
Contenuto della destinazione di rendering in formato R8G8B8A8 \_ UNORM.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IFrameBufferCallback**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
