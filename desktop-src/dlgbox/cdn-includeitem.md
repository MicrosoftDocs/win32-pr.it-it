---
title: CDN_INCLUDEITEM di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome per determinare se la finestra di dialogo deve visualizzare un elemento nell'elenco di elementi di una cartella della shell.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM di dialogo del codice di notifica
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
ms.openlocfilehash: 78f25ea90f8eb37c829cdc86e89f6d7e8cad2312
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549256"
---
# <a name="cdn_includeitem-notification-code"></a>Codice di notifica INCLUDEITEM della rete CDN \_

\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]

Inviato da una **finestra di** dialogo Apri o **Salva** con nome per determinare se la finestra di dialogo deve visualizzare un elemento nell'elenco di elementi di una cartella della shell. Quando l'utente apre una cartella, la finestra di dialogo invia una notifica **\_ INCLUDEITEM della** rete CDN per ogni elemento nella cartella. La finestra di dialogo invia questa notifica solo se al momento della creazione della finestra di dialogo è stato impostato il flag **OFN \_ ENABLEINCLUDENOTIFY.**

La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)


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

Puntatore a una [**struttura OFNOTIFYEX.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)

La [**struttura OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contiene una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) il cui membro **di** codice indica il messaggio di notifica **\_ INCLUDEITEM** della rete CDN.

Il **membro psf** della struttura [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) è un puntatore a un'interfaccia per la cartella i cui elementi vengono enumerati. Il **membro pidl** è un puntatore a un elenco di identificatori di elemento che identifica l'elemento relativo alla cartella.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) restituisce zero, la finestra di dialogo esclude l'elemento dall'elenco di elementi.

Per includere l'elemento, restituire un valore diverso da zero dalla routine hook.

## <a name="remarks"></a>Commenti

La finestra di dialogo include sempre gli elementi con gli attributi **SFGAO \_ FILESYSTEM** e **SFGAO \_ FILESYSANCESTOR,** indipendentemente dal valore restituito da **\_ CDN INCLUDEITEM.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Getopenfilename**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> </dl>

