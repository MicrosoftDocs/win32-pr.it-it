---
title: EM_SETELLIPSISMODE messaggio (Richedit.h)
description: Questo messaggio imposta la modalità dei puntini di sospensione corrente.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445172ea0a4ed4ef49e9a131db8d4357faaa5f7fef553169b7a8e1e795fd01c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019479"
---
# <a name="em_setellipsismode-message"></a>Messaggio EM \_ SETELLIPSISMODE

Questo messaggio imposta la modalità dei puntini di sospensione corrente. Se abilitata, vengono visualizzati i puntini di sospensione ( ) per il testo che non rientra nella finestra di visualizzazione. I puntini di sospensione vengono usati solo quando il controllo non è attivo. Se attive, le barre di scorrimento vengono usate per visualizzare il testo che non rientra nella finestra di visualizzazione.


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore DWORD che riceve uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**PUNTINI DI SOSPENSIONE \_ NESSUNO**</dt> </dl> | Non vengono usati i puntini di sospensione.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**FINE PUNTINI DI \_ SOSPENSIONE**</dt> </dl>    | Puntini di sospensione alla fine (interruzione forzata).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**PAROLA CON I PUNTINI DI \_ SOSPENSIONE**</dt> </dl> | Puntini di sospensione alla fine (interruzione di parola).<br/>   |



 

I bit per questi valori rientrano tutti in **ELLIPSIS \_ MASK.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se wparam è 0 e lparam è uno dei valori nella tabella precedente, il valore restituito è uguale a TRUE; In caso contrario, il valore restituito è uguale a FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETELLIPSISMODE**](em-getellipsismode.md)
</dt> <dt>

[**EM \_ GETELLIPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





