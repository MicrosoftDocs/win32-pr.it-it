---
description: La funzione AddForm aggiunge un modulo all'elenco dei moduli disponibili che è possibile selezionare per la stampante specificata.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: Funzione AddForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311570"
---
# <a name="addform-function"></a>AddForm (funzione)

La funzione **AddForm** aggiunge un modulo all'elenco dei moduli disponibili che è possibile selezionare per la stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante che supporta la stampa con il form specificato. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Livello della struttura a cui punta *pForm* . Questo valore deve essere 1 o 2.

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

 

Un'applicazione può determinare quali moduli sono disponibili per una stampante chiamando la funzione [**EnumForms**](enumforms.md) .

Se *pForm* punta a un [**modulo \_ info \_ 2**](form-info-2.md), **AddForm** avrà esito negativo se un modulo con il nome specificato esiste già o se il valore *pKeyword* della struttura esiste già.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**Informazioni sul modulo \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**Informazioni sul modulo \_ \_ 2**](form-info-2.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




