---
description: Specifica una funzione di callback definita dall'applicazione chiamata da File Manager quando l'utente sceglie il comando Annulla eliminazione dal menu File.
title: FM_UNDELETE_PROC puntatore a funzione (Wfext.h)
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
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842422"
---
# <a name="fm_undelete_proc-function-pointer"></a>Puntatore alla funzione FM \_ UNDELETE \_ PROC

Specifica una funzione di callback definita dall'applicazione chiamata da  File Manager quando l'utente sceglie il comando Annulla eliminazione dal menu **File.**

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

Handle di finestra per File Manager. Una DLL di annullamento dell'eliminazione deve utilizzare questo handle per specificare la finestra del proprietario per qualsiasi finestra di dialogo o finestra di messaggio che potrebbe essere visualizzata nella DLL.

</dd> <dt>

*lpszDir* 
</dt> <dd>

Tipo: **LPSTR**

Indirizzo di una stringa con terminazione Null che contiene il nome della directory iniziale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **DWORD**

Restituisce uno dei valori seguenti.



| Codice restituito                                                                             | Descrizione                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | Si è verificato un errore.<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | È stata annullata l'eliminazione di un file. File Manager ridisegna la finestra.<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | Nessun file è stato annullato.<br/>                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



 

 




