---
title: SB_GETTEXTLENGTH messaggio (Commctrl.h)
description: Recupera la lunghezza, in caratteri, del testo dalla parte specificata di una finestra di stato.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH di controllo Windows messaggio
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c203862b2a17352924f3df07560034c9f52784c84676d924d78524b05be1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084961"
---
# <a name="sb_gettextlength-message"></a>Messaggio SB \_ GETTEXTLENGTH

Recupera la lunghezza, in caratteri, del testo dalla parte specificata di una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della parte da cui recuperare il testo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit costituito da due valori a 16 bit. La parola bassa specifica la lunghezza, in caratteri, del testo. La parola alta specifica il tipo di operazione usata per disegnare il testo. Il tipo può essere uno dei valori seguenti:



| Codice restituito                                                                                    | Descrizione                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Il testo viene disegnato con un bordo inferiore al piano della finestra.<br/>          |
| <dl> <dt>**SBT \_ NOBORDERS**</dt> </dl>  | Il testo viene disegnato senza bordi.<br/>                                                     |
| <dl> <dt>**SBT \_ OWNERDRAW**</dt> </dl>  | Il testo viene disegnato dalla finestra padre.<br/>                                                |
| <dl> <dt>**SBT \_ POPOUT**</dt> </dl>     | Il testo viene disegnato con un bordo superiore al piano della finestra.<br/>         |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | Il testo verrà visualizzato nella direzione opposta al testo nella finestra padre.<br/> |



 

## <a name="remarks"></a>Commenti

Le finestre normali visualizzano il testo da sinistra a destra. Windows possibile eseguire *il mirroring per* visualizzare lingue come l'ebraico o l'arabo che leggono da destra a sinistra (RTL). Se l'opzione SBT RTLREADING è impostata, il testo della finestra di stato specificato verrà letto nella direzione opposta rispetto al testo \_ nella finestra padre.

Questo messaggio restituisce una lunghezza massima della stringa di 65.535 caratteri. Se la stringa di testo effettiva è più lunga, il [**messaggio SB \_ GETTEXT**](sb-gettext.md) la tronca.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ GETTEXTLENGTHW** (Unicode) e **SB \_ GETTEXTLENGTHA** (ANSI)<br/>         |



 

 





