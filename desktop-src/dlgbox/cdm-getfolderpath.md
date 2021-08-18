---
title: CDM_GETFOLDERPATH messaggio (Commdlg.h)
description: Recupera il percorso della cartella o della directory attualmente aperta per una finestra di dialogo Apri o Salva con nome in stile Esplora risorse.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ccc4e1e9fec74b10c2d5937b35b7e9b3bba2005a504a79abe7b94f341732d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843451"
---
# <a name="cdm_getfolderpath-message"></a>Messaggio \_ CDM GETFOLDERPATH

\[A partire Windows Vista, **le**  finestre di dialogo comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo Elemento [comune](../shell/common-file-dialog.md). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]

Recupera il percorso della cartella o della directory  attualmente aperta per una finestra di dialogo Apri o **Salva con** nome in stile Esplora risorse. La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in caratteri, del buffer *lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve il percorso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è la dimensione, in caratteri, della stringa di percorso, incluso il carattere Null di terminazione. Si tratta del numero di byte o caratteri copiati nel buffer o della dimensione del buffer necessaria se il buffer è troppo piccolo.

Se si verifica un errore, il valore restituito è minore di zero.

## <a name="remarks"></a>Commenti

La macro corrispondente è la seguente:

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
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

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> </dl>

