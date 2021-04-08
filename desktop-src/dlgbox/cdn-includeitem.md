---
title: Codice di notifica CDN_INCLUDEITEM (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome per determinare se nella finestra di dialogo deve essere visualizzato un elemento nell'elenco di elementi di una cartella della shell.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- Finestre di dialogo CDN_INCLUDEITEM codice di notifica
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cbe830c644657425eb087dd64884da17a9a0c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742847"
---
# <a name="cdn_includeitem-notification-code"></a>Codice di notifica INCLUDEITEM della rete CDN \_

\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]

Inviato da una finestra di dialogo **Apri** o **Salva con nome** per determinare se nella finestra di dialogo deve essere visualizzato un elemento nell'elenco di elementi di una cartella della shell. Quando l'utente apre una cartella, la finestra di dialogo Invia una notifica **\_ INCLUDEITEM** della rete CDN per ogni elemento nella cartella. La finestra di dialogo Invia questa notifica solo se è stato impostato il flag **OFN \_ ENABLEINCLUDENOTIFY** quando è stata creata la finestra di dialogo.

La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) .

La struttura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ INCLUDEITEM** della rete CDN.

Il membro **PSF** della struttura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) è un puntatore a un'interfaccia per la cartella i cui elementi vengono enumerati. Il membro **PIDL** è un puntatore a un elenco di identificatori di elemento che identifica l'elemento relativo alla cartella.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) restituisce zero, la finestra di dialogo esclude l'elemento dall'elenco di elementi.

Per includere l'elemento, restituire un valore diverso da zero dalla routine hook.

## <a name="remarks"></a>Commenti

La finestra di dialogo include sempre elementi con gli attributi **SFGAO \_ filesystem** e **SFGAO \_ FILESYSANCESTOR** , indipendentemente dal valore restituito dalla rete **CDN \_ INCLUDEITEM**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

