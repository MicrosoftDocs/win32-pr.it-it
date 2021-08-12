---
title: BM_SETIMAGE messaggio (Winuser.h)
description: Associa una nuova immagine (icona o bitmap) al pulsante.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE controlli Windows messaggio
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8948c73c04d3b01230a47ab91529764c9e20281e4f45803f71d82f59dedb14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674814"
---
# <a name="bm_setimage-message"></a>Messaggio BM \_ SETIMAGE

Associa una nuova immagine (icona o bitmap) al pulsante.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di immagine da associare al pulsante. Questo parametro può essere uno dei valori seguenti:

-   BITMAP \_ DELL'IMMAGINE
-   ICONA \_ IMMAGINE

</dd> <dt>

*lParam* 
</dt> <dd>

Handle (**HICON** o **HBITMAP**) all'immagine da associare al pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per l'immagine associata in precedenza al pulsante, se presente; in caso contrario, è **NULL.**

## <a name="remarks"></a>Commenti

L'aspetto del testo, di un'icona o di entrambi in un controllo pulsante dipende dagli stili [**BS \_ ICON**](button-styles.md) e [**BS \_ BITMAP**](button-styles.md) e dal fatto che il messaggio **BM \_ SETIMAGE** sia chiamato. I possibili risultati sono i seguenti:



| BS \_ ICON o BS BITMAP \_ Set? | Chiamata di BM \_ SETIMAGE? | Risultato              |
|-----------------------------|----------------------|---------------------|
| Sì                         | Sì                  | Mostra solo icona.     |
| No                          | Sì                  | Mostra l'icona e il testo. |
| Sì                         | No                   | Mostra solo testo.     |
| No                          | No                   | Mostra solo testo      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BM \_ GETIMAGE**](bm-getimage.md)
</dt> </dl>

 

 





