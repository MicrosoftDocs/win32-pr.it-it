---
title: ICM_DECOMPRESS_SET_PALETTE messaggio (Vfw.h)
description: Il ICM DECOMPRESS SET PALETTE specifica una tavolozza da usare per un driver di decompressione video se viene \_ \_ decompressa in un formato che usa \_ una tavolozza. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE messaggio Windows Multimediali
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
ms.openlocfilehash: 42213685b43d73ca0b71698b201f4c54358254d8be5b8f1e2063da1a60ada4f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987921"
---
# <a name="icm_decompress_set_palette-message"></a>\_ICM DECOMPRESSIONE \_ DEL MESSAGGIO SET \_ PALETTE

Il **ICM \_ DECOMPRESS \_ SET \_ PALETTE** specifica una tavolozza da usare per un driver di decompressione video se viene decompressa in un formato che usa una tavolozza. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDecompressSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette)


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*
</dt> <dd>

Puntatore a [**una struttura BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) la cui tabella dei colori contiene i colori da usare, se possibile. È possibile specificare zero per usare il set predefinito di colori di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR OK se il driver di decompressione può decomprimere con precisione le immagini nella tavolozza suggerita usando il set di colori disposti \_ nella tavolozza. Restituisce ICERR \_ UNSUPPORTED in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio non deve influire sulla decompressione già in corso. invece, i colori passati usando questo messaggio devono essere restituiti ICM in risposta ai messaggi [**\_ DECOMPRESS GET FORMAT e DECOMPRESS \_ GET \_ FORMAT**](icm-decompress-get-format.md) ICM [**\_ DECOMPRESS \_ GET \_ PALETTE.**](icm-decompress-get-palette.md) I colori vengono inviati al driver di decompressione in un messaggio [**\_ ICM DECOMPRESS \_ BEGIN.**](icm-decompress-begin.md)

Questo messaggio viene usato principalmente quando un driver decomprime le immagini sullo schermo e un'altra applicazione che usa una tavolozza è in primo piano, forzando il driver di decompressione ad adattarsi a un set di colori estraneo.

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

 

