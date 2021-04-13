---
description: La funzione seform imposta le informazioni sul form per la stampante specificata.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: Funzione seform (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345281"
---
# <a name="setform-function"></a>Funzione seform

La funzione **seform** imposta le informazioni sul form per la stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante per cui sono impostate le informazioni sul form. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*pFormName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del modulo per il quale sono impostate le informazioni sul form.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura a cui punta *pForm* . Questo valore deve essere 1 o 2.

</dd> <dt>

*pForm* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ informazioni \_ su form 1**](form-info-1.md) o [**form \_ info \_ 2**](form-info-2.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

È **possibile chiamare** il metodo più volte per un'informazione sul [**form esistente \_ \_ 2**](form-info-2.md), ogni chiamata che aggiunge altre coppie di valori **pDisplayName** e **wLangId** . Tutte le versioni dei linguaggi del modulo otterranno i valori **size** e **ImageableArea** del **form \_ info \_ 2** nella chiamata più recente a **seform**.

Se il chiamante è remoto e il *livello* è 2, il valore di **StringType** nel [**formato \_ info \_ 2**](form-info-2.md) non può essere \_ MUIDLL di stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **SetFormW** (Unicode) e **seforma** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Informazioni sul modulo \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**Informazioni sul modulo \_ \_ 2**](form-info-2.md)
</dt> </dl>

 

 




