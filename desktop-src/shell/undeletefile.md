---
description: Specifica una funzione di callback definita dall'applicazione chiamata da file Manager quando l'utente sceglie il comando Annulla eliminazione dal menu file.
title: Puntatore a funzione FM_UNDELETE_PROC (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233561"
---
# <a name="fm_undelete_proc-function-pointer"></a>\_Puntatore alla funzione di annullamento dell'eliminazione FM \_

Specifica una funzione di callback definita dall'applicazione chiamata da file Manager quando l'utente sceglie il comando **Annulla eliminazione** dal menu **file** .

## <a name="syntax"></a>Sintassi


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndOwner* 
</dt> <dd>

Tipo: **HWND**

Handle della finestra per file Manager. Una DLL di annullamento dell'eliminazione deve utilizzare questo handle per specificare la finestra proprietaria per qualsiasi finestra di dialogo o finestra di messaggio che può essere visualizzata dalla DLL.

</dd> <dt>

*lpszDir* 
</dt> <dd>

Tipo: **LPSTR**

Indirizzo di una stringa con terminazione null che contiene il nome della directory iniziale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **DWORD**

Restituisce uno dei valori seguenti.



| Codice restituito                                                                             | Descrizione                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | Si è verificato un errore.<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | Un file non è stato eliminato. Gestione file ridisegna la finestra.<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | Nessun file eliminato.<br/>                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



 

 




