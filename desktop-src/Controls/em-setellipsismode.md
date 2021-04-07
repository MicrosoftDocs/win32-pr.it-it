---
title: Messaggio di EM_SETELLIPSISMODE (RichEdit. h)
description: Questo messaggio consente di impostare la modalità corrente dei puntini di sospensione.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- Controlli di Windows Message EM_SETELLIPSISMODE
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
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048654"
---
# <a name="em_setellipsismode-message"></a>\_Messaggio SETELLIPSISMODE em

Questo messaggio consente di impostare la modalità corrente dei puntini di sospensione. Quando è abilitata, viene visualizzato un pulsante con i puntini di sospensione () per il testo che non rientra nella finestra di visualizzazione. I puntini di sospensione vengono utilizzati solo quando il controllo non è attivo. Quando è attiva, le barre di scorrimento vengono usate per rivelare il testo che non rientra nella finestra di visualizzazione.


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore DWORD che riceve uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**PUNTIni di sospensione \_ nessuno**</dt> </dl> | Non viene utilizzato alcun puntini di sospensione.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**PUNTIni di sospensione \_**</dt> </dl>    | Puntini di sospensione alla fine (interruzioni forzate).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**parola con i PUNTIni di sospensione \_**</dt> </dl> | Puntini di sospensione alla fine (Word Break).<br/>   |



 

Tutti i bit per questi valori si adattano **alla \_ maschera dei puntini** di sospensione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se wParam è 0 e lParam è uno dei valori nella tabella precedente, il valore restituito è uguale a TRUE; in caso contrario, il valore restituito è uguale a FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETELLIPSISMODE em**](em-getellipsismode.md)
</dt> <dt>

[**\_GETELLIPSISSTATE em**](em-getellipsisstate.md)
</dt> </dl>

 

 





