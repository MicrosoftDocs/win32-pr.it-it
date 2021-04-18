---
description: La funzione GetForm recupera le informazioni relative a un modulo specificato.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: Funzione GetForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6b6ea9753e1b335936778e17562f6f26467b3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314016"
---
# <a name="getform-function"></a>Funzione GetForm

La funzione **GetForm** recupera le informazioni relative a un modulo specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pFormName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del form. Per ottenere i nomi dei form supportati dalla stampante, chiamare la funzione [**EnumForms**](enumforms.md) .

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura a cui punta *pForm* . Questo valore deve essere 1 o 2.

</dd> <dt>

*pForm* \[ out\]
</dt> <dd>

Puntatore a una matrice di byte che riceve il [**form inizializzato \_ informazioni \_ 1**](form-info-1.md) o la struttura di [**informazioni sul form \_ \_ 2**](form-info-2.md) .

</dd> <dt>

*cbBuf* \[ in\]
</dt> <dd>

Dimensione, in byte, della matrice *pForm* .

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Puntatore a un valore che specifica il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Se il chiamante è remoto e il *livello* è 2, il valore di **StringType** del modulo restituito [**\_ info \_ 2**](form-info-2.md) sarà sempre stringa \_ LANGPAIR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **GetFormW** (Unicode) e **getforma** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**DeleteForm**](deleteform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Diformi**](setform.md)
</dt> </dl>

 

 




