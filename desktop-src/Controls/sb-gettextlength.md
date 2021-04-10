---
title: Messaggio SB_GETTEXTLENGTH (COMmctrl. h)
description: Recupera la lunghezza, in caratteri, del testo dalla parte specificata di una finestra di stato.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- Controlli di Windows Message SB_GETTEXTLENGTH
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
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964640"
---
# <a name="sb_gettextlength-message"></a>\_Messaggio GETTEXTLENGTH SB

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

Restituisce un valore a 32 bit costituito da valori a 2 16 bit. La parola low specifica la lunghezza, in caratteri, del testo. La parola alta specifica il tipo di operazione utilizzata per creare il testo. Il tipo può essere uno dei valori seguenti:



| Codice restituito                                                                                    | Descrizione                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Il testo viene disegnato con un bordo da visualizzare in basso rispetto al piano della finestra.<br/>          |
| <dl> <dt>**\_NOborders SBT**</dt> </dl>  | Il testo viene disegnato senza bordi.<br/>                                                     |
| <dl> <dt>**\_OWNERDRAW SBT**</dt> </dl>  | Il testo viene disegnato dalla finestra padre.<br/>                                                |
| <dl> <dt>**\_POPOUT SBT**</dt> </dl>     | Il testo viene disegnato con un bordo da visualizzare più in alto rispetto al piano della finestra.<br/>         |
| <dl> <dt>**\_RTLREADING SBT**</dt> </dl> | Il testo verrà visualizzato nella direzione opposta al testo nella finestra padre.<br/> |



 

## <a name="remarks"></a>Commenti

Normale testo visualizzato da sinistra a destra (LTR). È possibile eseguire il *mirroring* di Windows per visualizzare lingue quali l'ebraico o l'arabo con lettura da destra a sinistra (RTL). Se \_ è impostato SBT RTLREADING, il testo della finestra di stato specificato verrà letto nella direzione opposta dal testo nella finestra padre.

Questo messaggio restituisce una lunghezza massima della stringa di 65.535 caratteri. Se la stringa di testo effettiva è più lunga, il messaggio [**SB \_ gettext**](sb-gettext.md) lo tronca.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SB \_ GETTEXTLENGTHW** (Unicode) e **SB \_ GETTEXTLENGTHA** (ANSI)<br/>         |



 

 





