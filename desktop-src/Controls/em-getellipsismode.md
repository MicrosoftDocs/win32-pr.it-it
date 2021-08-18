---
title: EM_GETELLIPSISMODE messaggio (Richedit.h)
description: Recupera la modalità dei puntini di sospensione corrente.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6706c2b6ee75852fd0b3ee7a1a9d18b25d20d242d72068ba073d1bb025ff8ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019699"
---
# <a name="em_getellipsismode-message"></a>Messaggio \_ EM GETELLIPSISMODE

Recupera la modalità dei puntini di sospensione corrente. Se abilitata, vengono visualizzati i puntini di sospensione ( ) per il testo che non rientra nella finestra di visualizzazione. I puntini di sospensione vengono usati solo quando il controllo non è attivo. Quando sono attive, le barre di scorrimento vengono usate per visualizzare il testo che non rientra nella finestra di visualizzazione.


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore DWORD che riceve uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**PUNTINI DI SOSPENSIONE \_ NESSUNO**</dt> </dl> | Non vengono usati puntini di sospensione.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**FINE DEI PUNTINI DI \_ SOSPENSIONE**</dt> </dl>    | Puntini di sospensione alla fine (interruzione forzata).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**PAROLA CON PUNTINI DI \_ SOSPENSIONE**</dt> </dl> | Puntini di sospensione alla fine (interruzione di parola).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se wparam è 0 e lparam non è NULL, il valore restituito è TRUE; in caso contrario, il valore restituito è uguale a FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETELLIPSISMODE**](em-setellipsismode.md)
</dt> <dt>

[**EM \_ GETELLIPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





