---
title: Messaggio LBSELCHSTRING (Commdlg.h)
description: Una finestra di dialogo Apri o Salva con nome invia il messaggio registrato LBSELCHSTRING alla procedura hook quando la selezione cambia in una delle caselle di riepilogo o nelle caselle combinate della finestra di dialogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Finestre di dialogo del messaggio LBSELCHSTRING
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea804e1bd5ad35b5ad5d5ee98cf77f97d54e4e93f438e6e32ad7478e10d7b9ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985401"
---
# <a name="lbselchstring-message"></a>Messaggio LBSELCHSTRING

\[A partire Windows Vista, **le**  finestre di dialogo comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo Elemento [comune](../shell/common-file-dialog.md). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]

Una **finestra di** dialogo Apri o Salva con nome invia il messaggio registrato  **LBSELCHSTRING** alla procedura hook quando la selezione cambia in una delle caselle di riepilogo o nelle caselle combinate della finestra di dialogo.


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore della casella di riepilogo o della casella combinata in cui è stata modificata la selezione.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola meno ordinata specifica il numero di elemento della stringa selezionata nella casella di riepilogo o nella casella combinata. La parola di ordine alto specifica il tipo di modifica della selezione. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                       | Significato                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt> </dl>     | L'elemento è l'unico elemento selezionato in una casella di riepilogo a selezione singola.<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD \_ LBSELADD**</dt> <dt>2</dt> </dl>              | L'elemento è uno degli elementi selezionati in una casella di riepilogo a selezione multipla.<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD \_ LBSELSUB**</dt> <dt>1</dt> </dl>              | L'elemento non è più selezionato in una casella di riepilogo a selezione multipla.<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt> </dl> | In una casella di riepilogo a selezione multipla non sono presenti elementi.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

La routine hook deve specificare la costante **LBSELCHSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore per il messaggio inviato dalla finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LBSELCHSTRINGW** (Unicode) e **LBSELCHSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_rete CDN Selchange**](cdn-selchange.md)
</dt> <dt>

[**\_rete CDN TYPECHANGE**](cdn-typechange.md)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> </dl>

