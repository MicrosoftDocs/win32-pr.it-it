---
title: Messaggio di ICM_DECOMPRESS_QUERY (VFW. h)
description: Il \_ messaggio di query decomprimere ICM \_ esegue una query su un driver di decompressione video per determinare se supporta un formato di input specifico o se può decomprimere un formato di input specifico in un formato di output specifico.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- ICM_DECOMPRESS_QUERY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302267"
---
# <a name="icm_decompress_query-message"></a>\_Messaggio di query di decompressione ICM \_

Il messaggio di **\_ \_ query decomprimere ICM** esegue una query su un driver di decompressione video per determinare se supporta un formato di input specifico o se può decomprimere un formato di input specifico in un formato di output specifico. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) .


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di output. È possibile specificare zero per questo parametro per indicare che il formato di output è accettabile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se la decompressione specificata è supportata o ICERR \_ BADFORMAT in caso contrario.

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

 

