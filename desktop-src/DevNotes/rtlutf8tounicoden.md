---
description: Converte la stringa di origine specificata in una stringa Unicode, usando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Funzione RtlUTF8ToUnicodeN (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225593"
---
# <a name="rtlutf8tounicoden-function"></a>RtlUTF8ToUnicodeN (funzione)

Converte la stringa di origine specificata in una stringa Unicode, usando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UnicodeStringDestination* \[ out\]
</dt> <dd>

Puntatore a un buffer allocato dal chiamante che riceve la stringa tradotta.

</dd> <dt>

*UnicodeStringMaxByteCount* \[ in\]
</dt> <dd>

Numero massimo di byte da scrivere in *UnicodeStringDestination*. Se questo valore fa sì che la stringa tradotta venga troncata, **RtlUTF8ToUnicodeN** restituisce uno stato di errore.

</dd> <dt>

*UnicodeStringActualByteCount* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile allocata dal chiamante che riceve la lunghezza, in byte, della stringa tradotta. Questo parametro è facoltativo e può essere **null**. Se la stringa viene troncata, il numero restituito conteggia il conteggio effettivo delle stringhe troncate.

</dd> <dt>

*UTF8StringSource* \[ in\]
</dt> <dd>

Puntatore alla stringa da tradurre.

</dd> <dt>

*UTF8StringByteCount* \[ in\]
</dt> <dd>

Dimensione, in byte, della stringa in corrispondenza di *UTF8StringSource*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**RtlUTF8ToUnicodeN** restituisce uno dei valori NTSTATUS seguenti:



| Codice restituito                                                                                                  | Descrizione                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATO \_ riuscito**</dt> </dl>               | La stringa è stata convertita in Unicode.<br/>                                                                 |
| <dl> <dt>**STATO \_ \_ non \_ mappato**</dt> </dl>     | È stato rilevato e sostituito un carattere di input non valido. Questo stato è considerato uno stato di esito positivo.<br/> |
| <dl> <dt>**STATO \_ parametro non valido \_**</dt> </dl>    | Entrambi i puntatori a *UnicodeStringDestination* e *UnicodeStringActualByteCount* sono **null**.<br/>       |
| <dl> <dt>**STATO \_ parametro non valido \_ \_ 4**</dt> </dl> | *UTF8StringSource* è **null**.<br/>                                                                 |
| <dl> <dt>**BUFFER di stato \_ \_ troppo \_ piccolo**</dt> </dl>    | *UnicodeStringDestination* troncato.<br/>                                                            |



 

## <a name="remarks"></a>Commenti

Anche se *UnicodeStringActualByteCount* è facoltativo e può essere **null**, i chiamanti devono fornire lo spazio di archiviazione, perché la lunghezza ricevuta può essere usata per determinare se la conversione è stata eseguita correttamente.

Se l'output viene troncato e viene rilevato un carattere di input non valido, la funzione restituisce un errore di buffer di stato \_ \_ troppo \_ piccolo.

Se *UnicodeStringDestination* è impostato su **null** , la funzione restituirà il numero di byte richiesto per ospitare la stringa tradotta senza troncamenti in *UnicodeStringActualByteCount*.

**RtlUTF8ToUnicodeN** non modifica la stringa di origine a meno che i puntatori *UnicodeStringDestination* e *UTF8StringSource* non siano equivalenti. La stringa Unicode restituita non è con terminazione null.

I chiamanti di **RtlUTF8ToUnicodeN** devono essere in esecuzione a livello IRQL < livello di invio \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlUnicodeToUTF8N**](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




