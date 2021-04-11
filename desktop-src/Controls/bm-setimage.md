---
title: Messaggio BM_SETIMAGE (winuser. h)
description: Associa una nuova immagine (icona o bitmap) a un pulsante.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- Controlli di Windows Message BM_SETIMAGE
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
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119239"
---
# <a name="bm_setimage-message"></a>Messaggio di immagine di BM \_

Associa una nuova immagine (icona o bitmap) a un pulsante.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di immagine da associare al pulsante. Questo parametro può essere uno dei valori seguenti:

-   \_bitmap immagine
-   \_icona immagine

</dd> <dt>

*lParam* 
</dt> <dd>

Handle (**HICON** o **HBITMAP**) per l'immagine da associare al pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per l'immagine precedentemente associata al pulsante, se disponibile. in caso contrario, è **null**.

## <a name="remarks"></a>Commenti

L'aspetto del testo, di un'icona o di entrambi su un controllo Button dipende dall' [**\_ icona BS**](button-styles.md) e dagli stili di [**\_ bitmap BS**](button-styles.md) e dal fatto che il messaggio **BM \_ diImage** venga chiamato. I risultati possibili sono i seguenti:



| \_Icona BS o \_ set di bitmap BS? | \_Nome dell'immagine BM | Risultato              |
|-----------------------------|----------------------|---------------------|
| Sì                         | Sì                  | Mostra solo l'icona.     |
| No                          | Sì                  | Mostra icona e testo. |
| Sì                         | No                   | Mostra solo testo.     |
| No                          | No                   | Mostra solo testo      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BM \_ GETimage**](bm-getimage.md)
</dt> </dl>

 

 





