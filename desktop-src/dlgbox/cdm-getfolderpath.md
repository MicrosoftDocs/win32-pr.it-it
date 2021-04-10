---
title: Messaggio CDM_GETFOLDERPATH (COMMDLG. h)
description: Recupera il percorso della cartella o della directory attualmente aperta per una finestra di dialogo Apri o Salva con nome in stile Esplora risorse.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- Finestre di dialogo CDM_GETFOLDERPATH messaggio
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
ms.openlocfilehash: 9ff15e72d93e921968601f9c8472901d20769478
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964304"
---
# <a name="cdm_getfolderpath-message"></a>\_Messaggio GETFOLDERPATH CDM

\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]

Recupera il percorso della cartella o della directory attualmente aperta per una finestra di dialogo **Apri** o **Salva con nome in** stile Esplora risorse. La finestra di dialogo deve essere stata creata con il flag **OFN \_ Explorer** . in caso contrario, il messaggio ha esito negativo.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in caratteri, del buffer *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve il percorso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è la dimensione, in caratteri, della stringa di percorso, incluso il carattere null di terminazione. Si tratta del numero di byte o di caratteri copiati nel buffer o della dimensione del buffer necessaria se il buffer è troppo piccolo.

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
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

