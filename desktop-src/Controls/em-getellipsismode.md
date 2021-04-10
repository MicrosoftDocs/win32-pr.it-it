---
title: Messaggio di EM_GETELLIPSISMODE (RichEdit. h)
description: Recupera la modalità corrente dei puntini di sospensione.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- Controlli di Windows Message EM_GETELLIPSISMODE
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
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119842"
---
# <a name="em_getellipsismode-message"></a>\_Messaggio GETELLIPSISMODE em

Recupera la modalità corrente dei puntini di sospensione. Quando è abilitata, viene visualizzato un pulsante con i puntini di sospensione () per il testo che non rientra nella finestra di visualizzazione. I puntini di sospensione vengono utilizzati solo quando il controllo non è attivo. Quando è attiva, le barre di scorrimento vengono usate per rivelare il testo che non rientra nella finestra di visualizzazione.


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore DWORD che riceve uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**PUNTIni di sospensione \_ nessuno**</dt> </dl> | Non viene utilizzato alcun puntini di sospensione.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**PUNTIni di sospensione \_**</dt> </dl>    | Puntini di sospensione alla fine (interruzioni forzate).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**parola con i PUNTIni di sospensione \_**</dt> </dl> | Puntini di sospensione alla fine (Word Break).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se wParam è 0 e lParam non è NULL, il valore restituito è uguale a TRUE; in caso contrario, il valore restituito è uguale a FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETELLIPSISMODE em**](em-setellipsismode.md)
</dt> <dt>

[**\_GETELLIPSISSTATE em**](em-getellipsisstate.md)
</dt> </dl>

 

 





