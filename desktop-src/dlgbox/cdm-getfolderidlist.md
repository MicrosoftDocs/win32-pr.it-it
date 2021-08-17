---
title: CDM_GETFOLDERIDLIST messaggio (Commdlg.h)
description: Recupera l'indirizzo dell'elenco di identificatori di elemento corrispondente alla cartella attualmente aperta in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f6a753cf53bdd2cde53a0e3df973457b50b8ed326a7d7ee50c05dc24f1d0a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786194"
---
# <a name="cdm_getfolderidlist-message"></a>Messaggio CDM \_ GETFOLDERIDLIST

\[A partire Windows Vista, le  **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]

Recupera l'indirizzo dell'elenco di identificatori di elemento  corrispondente  alla cartella attualmente aperta in una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse. La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in byte, del buffer *lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve l'elenco di identificatori di elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è la dimensione, in byte, dell'elenco di identificatori di elemento. Si tratta del numero di byte copiati nel buffer o delle dimensioni del buffer richieste se il buffer è troppo piccolo.

Se si verifica un errore, il valore restituito è minore di zero.

## <a name="remarks"></a>Commenti

La macro corrispondente è la seguente:

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
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

