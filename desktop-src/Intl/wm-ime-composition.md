---
description: Inviato a un'applicazione quando l'IME modifica lo stato di composizione come risultato di una sequenza di tasti. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Messaggio WM_IME_COMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968676"
---
# <a name="wm_ime_composition-message"></a>\_Messaggio di \_ composizione IME WM

Inviato a un'applicazione quando l'IME modifica lo stato di composizione come risultato di una sequenza di tasti. Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

Carattere DBCS che rappresenta l'ultima modifica apportata alla stringa di composizione.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che specifica la modalità di modifica della stringa o del carattere di composizione. Il parametro può essere costituito da uno o più dei valori seguenti. Per ulteriori informazioni su questi valori, vedere [valori stringa di composizione IME](ime-composition-string-values.md).

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

**comaccarezzatore cataloghi globali \_**
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

**COMPCLAUSE cataloghi globali \_**
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

**COMPREADSTR cataloghi globali \_**
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

**COMPREADATTR cataloghi globali \_**
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

**COMPREADCLAUSE cataloghi globali \_**
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

**COMPSTR cataloghi globali \_**
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

**CURSORPOS cataloghi globali \_**
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

**DELTASTART cataloghi globali \_**
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

**RESULTCLAUSE cataloghi globali \_**
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

**RESULTREADCLAUSE cataloghi globali \_**
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

**RESULTREADSTR cataloghi globali \_**
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

**RESULTSTR cataloghi globali \_**
</dt> </dl>

Il parametro *lParam* può avere anche uno o più dei valori seguenti.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <dt>**CS \_ INSERTCHAR**</dt> </dl>    | Inserire il carattere di composizione *wParam* in corrispondenza del punto di inserimento corrente. Un'applicazione deve visualizzare il carattere di composizione se elabora questo messaggio.<br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <dt>**CS \_ NOMOVECARET**</dt> </dl> | Non spostare la posizione del punto di inserimento in seguito all'elaborazione del messaggio. Se, ad esempio, un IME specifica una combinazione di CS \_ INSERTCHAR e cs \_ NOMOVECARET, l'applicazione deve inserire il carattere specificato nella posizione corrente del cursore, ma non deve spostare il punto di inserimento alla posizione successiva. Un \_ \_ messaggio di composizione IME WM successivo con cataloghi globali \_ RESULTSTR sostituirà questo carattere.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo messaggio se Visualizza caratteri di composizione. In caso contrario, deve inviare il messaggio alla finestra IME.

Se l'applicazione ha creato una finestra IME, deve passare questo messaggio alla finestra. La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  elabora questo messaggio passandolo alla finestra IME predefinita. La finestra IME elabora questo messaggio aggiornando l'aspetto in base al flag di modifica specificato. Un'applicazione può chiamare [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) per recuperare il nuovo stato di composizione.

Se non è impostato alcun valore di cataloghi globali \_ , il messaggio indica che la composizione corrente è stata annullata e che le applicazioni che traggono la stringa di composizione devono eliminare la stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h); </dt> <dt>Imm. h (Includi Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodo di input](input-method-manager.md)
</dt> <dt>

[Messaggi di gestione metodo di input](input-method-manager-messages.md)
</dt> <dt>

[**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
