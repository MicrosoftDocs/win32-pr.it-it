---
description: Inviato da un'estensione di File Manager per recuperare il numero di file selezionati nella finestra di Gestione file attiva (finestra della directory o finestra Risultati ricerca). Il conteggio include i file con nomi di file lunghi.
title: FM_GETSELCOUNTLFN messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: ff0884e1b80e4a5a7e6c295bd449c8e1f6d069ced6c988f584108318a98c6891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094176"
---
# <a name="fm_getselcountlfn-message"></a>Messaggio \_ DI FM GETSELCOUNTLFN

Inviato da un'estensione di File Manager per recuperare il numero di file selezionati nella finestra di Gestione file attiva (finestra della directory o finestra Risultati ricerca). Il conteggio include i file con nomi di file lunghi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di file selezionati.

## <a name="remarks"></a>Commenti

Solo le estensioni che supportano nomi di file lunghi ( ad esempio, estensioni che supportano la rete) devono usare questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FM \_ GETFILESEL**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ GETFILESELLFN**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ GETSELCOUNT**](fm-getselcount.md)
</dt> </dl>

 

 




