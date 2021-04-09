---
description: Callback che notifica all'host le informazioni sul framebuffer restituite dalla richiesta associata.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFrameBufferCallback:: ResultCallback'
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
ms.openlocfilehash: 5433c7bbf5fe67455b60fd754eecb2c2877c5d6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124617"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>Metodo IFrameBufferCallback:: ResultCallback

Callback che notifica all'host le informazioni sul framebuffer restituite dalla richiesta associata.

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

*NumeroFrame*   
Numero di frame.

*Larghezza*   
Larghezza del frame.

*altezza*   
Altezza del frame.

*renderTargetPtr*   
Destinazione di rendering da cui provengono i risultati. Si tratta sempre di uno slot specificato dalla richiesta del buffer del frame oppure, in caso contrario, della prima Bount di RTV per l'origine di output.

*frameDuraction*   
Non usato.

*dimensioni*   
Dimensioni in byte del buffer di output.

*\_buffer count5*   
Contenuto della destinazione di rendering nel formato R8G8B8A8 \_ UNORM.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IFrameBufferCallback**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
