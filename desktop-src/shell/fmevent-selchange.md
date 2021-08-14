---
description: Inviato a una DLL di estensione quando l'utente seleziona un nome file nella finestra della directory di File Manager o nella finestra Risultati ricerca.
title: FMEVENT_SELCHANGE messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: befc217eeb24453d7db726cf68d233fa57e5a7971fd148406cf90810b52b070d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459038"
---
# <a name="fmevent_selchange-message"></a>Messaggio FMEVENT \_ SELCHANGE

Inviato a una DLL di estensione quando l'utente seleziona un nome file nella finestra della directory di File Manager o nella finestra Risultati ricerca.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una DLL di estensione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Le modifiche nella parte dell'albero della finestra della directory non generano questo messaggio.

Poiché l'utente può modificare la selezione più volte, la DLL di estensione deve restituire prontamente dopo l'elaborazione del messaggio per evitare di rallentare il processo di selezione per l'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




