---
title: Messaggio di ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: Il \_ messaggio della \_ tavolozza del set di decomprimementi ICM \_ specifica una tavolozza per un driver di decompressione video da usare se viene decompresso in un formato che usa una tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302266"
---
# <a name="icm_decompress_set_palette-message"></a>\_Messaggio della \_ tavolozza del set di DEcompressione ICM \_

Il messaggio della **\_ \_ \_ tavolozza del set di decomprimementi ICM** specifica una tavolozza per un driver di decompressione video da usare se viene decompresso in un formato che usa una tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*
</dt> <dd>

Puntatore a una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) la cui tabella dei colori contiene i colori che devono essere utilizzati, se possibile. È possibile specificare zero per usare il set predefinito di colori di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se il driver di decompressione può decomprimere con precisione le immagini nella tavolozza suggerita utilizzando il set di colori così come sono disposti nella tavolozza. Restituisce ICERR \_ in caso contrario non supportato.

## <a name="remarks"></a>Commenti

Questo messaggio non dovrebbe influire sulla decompressione già in corso. al contrario, i colori passati con questo messaggio devono essere restituiti in risposta [**al \_ \_ \_ formato MCI Decompress Get**](icm-decompress-get-format.md) e ai messaggi [**MCI \_ Decompress \_ get \_ palette**](icm-decompress-get-palette.md) . I colori vengono restituiti al driver di decompressione in un successivo messaggio di [**\_ \_ inizio**](icm-decompress-begin.md) decompressione di ICM.

Questo messaggio viene utilizzato principalmente quando un driver decomprime le immagini sullo schermo e un'altra applicazione che utilizza una tavolozza è in primo piano, forzando il driver di decompressione ad adattarsi a un set di colori esterno.

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

 

