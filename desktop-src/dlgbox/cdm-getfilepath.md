---
title: CDM_GETFILEPATH messaggio (Commdlg.h)
description: Recupera il percorso e il nome del file selezionato in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- CDM_GETFILEPATH finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdb7739cd2ab66362e18cc70f9937e75f80a82d9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590918"
---
# <a name="cdm_getfilepath-message"></a>Messaggio \_ CDM GETFILEPATH

\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](/windows/win32/shell/common-file-dialog). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]

Recupera il percorso e il nome del file  selezionato in una finestra di dialogo Apri o **Salva con** nome di tipo Esplora risorse. La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in caratteri, del buffer *lParam.* Per la versione ANSI, questo è il numero di byte. per la versione Unicode, questo è il numero di caratteri.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve il nome e il percorso del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è la dimensione, in caratteri, del nome file e della stringa di percorso, incluso il carattere NULL di terminazione. Si tratta del numero di byte o caratteri copiati nel buffer o delle dimensioni del buffer richieste se il buffer è troppo piccolo.

Se si verifica un errore, il valore restituito è minore di zero.

## <a name="remarks"></a>Commenti

La macro corrispondente è la seguente:

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

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

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

