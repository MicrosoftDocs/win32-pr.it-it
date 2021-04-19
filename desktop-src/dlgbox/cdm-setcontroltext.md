---
title: CDM_SETCONTROLTEXT messaggio (Commdlg.h)
description: Imposta il testo per il controllo specificato in una finestra di dialogo Apri o Salva con nome in stile Esplora risorse.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- CDM_SETCONTROLTEXT finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d75bb3d3ac486bbb43545df80c67383a7655b8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590888"
---
# <a name="cdm_setcontroltext-message"></a>Messaggio CDM \_ SETCONTROLTEXT

\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](/windows/win32/shell/common-file-dialog). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]

Imposta il testo per il controllo  specificato in una finestra di dialogo Apri o **Salva con** nome in stile Esplora risorse. La finestra di dialogo deve essere stata creata con il flag **OFN \_ EXPLORER;** in caso contrario, il messaggio ha esito negativo.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del controllo su cui deve essere impostato il testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuovo testo per il controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

La macro corrispondente è la seguente:

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
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

 

