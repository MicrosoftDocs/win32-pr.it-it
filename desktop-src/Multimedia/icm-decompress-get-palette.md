---
title: Messaggio di ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: Il \_ messaggio della tavolozza Decomprimi MCI \_ \_ richiede che il driver di decompressione video fornisca la tabella dei colori della struttura di output BITMAPINFOHEADER. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302268"
---
# <a name="icm_decompress_get_palette-message"></a>\_Messaggio della \_ tavolozza Decompress Get di ICM \_

Il messaggio della **\_ \_ \_ tavolozza Decomprimi MCI** richiede che il driver di decompressione video fornisca la tabella dei colori della struttura di output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntatore a una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) contenente il formato di input.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntatore a una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) per contenere la tabella dei colori. Lo spazio riservato per la tabella dei colori è sempre di almeno 256 colori. È possibile specificare zero per questo parametro per restituire solo le dimensioni della tabella dei colori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Se *lpbiOutput* è diverso da zero, il driver imposta il membro **biClrUsed** di [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) sul numero di colori nella tabella dei colori. Il driver riempie il membro **bmiColors** di [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con i colori effettivi.

Il driver deve supportare questo messaggio solo se usa una tavolozza diversa da quella specificata nel formato di input.

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

 

