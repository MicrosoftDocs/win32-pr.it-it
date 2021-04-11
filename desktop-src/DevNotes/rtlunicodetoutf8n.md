---
description: Converte la stringa Unicode specificata in una nuova stringa di caratteri utilizzando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Funzione RtlUnicodeToUTF8N (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126399"
---
# <a name="rtlunicodetoutf8n-function"></a>RtlUnicodeToUTF8N (funzione)

Converte la stringa Unicode specificata in una nuova stringa di caratteri utilizzando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UTF8StringDestination* \[ out\]
</dt> <dd>

Puntatore a un buffer allocato dal chiamante per ricevere la stringa tradotta.

</dd> <dt>

*UTF8StringMaxByteCount* \[ in\]
</dt> <dd>

Numero massimo di byte da scrivere in *UTF8StringDestination*. Se questo valore fa sì che la stringa tradotta venga troncata, **RtlUnicodeToUTF8N** restituisce uno stato di errore.

</dd> <dt>

*UTF8StringActualByteCount* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile allocata dal chiamante che riceve la lunghezza, in byte, della stringa tradotta. Questo parametro è facoltativo e può essere **null**. Se la stringa viene troncata, il numero restituito conteggia il conteggio effettivo delle stringhe troncate.

</dd> <dt>

*UnicodeStringSource* \[ in\]
</dt> <dd>

Puntatore alla stringa di origine Unicode da tradurre.

</dd> <dt>

* UnicodeStringByteCount * \[ in\]
</dt> <dd>

Specifica il numero di byte nella stringa di origine Unicode a cui punta il parametro *UnicodeStringSource* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**RtlUnicodeToUTF8N** restituisce uno dei valori NTSTATUS seguenti:



| Codice restituito                                                                                                  | Descrizione                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATO \_ riuscito**</dt> </dl>               | La stringa Unicode è stata convertita in UTF-8.<br/>                                                           |
| <dl> <dt>**STATO \_ \_ non \_ mappato**</dt> </dl>     | È stato rilevato e sostituito un carattere di input non valido. Questo stato è considerato uno stato di esito positivo.<br/> |
| <dl> <dt>**STATO \_ parametro non valido \_**</dt> </dl>    | Entrambi i puntatori a *UTF8StringDestination* e *UTF8StringActualByteCount* sono **null**.<br/>              |
| <dl> <dt>**STATO \_ parametro non valido \_ \_ 4**</dt> </dl> | *UnicodeStringSource* è **null**.<br/>                                                              |
| <dl> <dt>**BUFFER di stato \_ \_ troppo \_ piccolo**</dt> </dl>    | *UTF8StringDestination* troncato.<br/>                                                               |



 

## <a name="remarks"></a>Commenti

Anche se *UTF8StringActualByteCount* è facoltativo e può essere **null**, i chiamanti devono fornire lo spazio di archiviazione, perché la lunghezza ricevuta può essere usata per determinare se la conversione è stata eseguita correttamente. Questa routine non modifica la stringa di origine. Restituisce una stringa UTF-8 con terminazione null se il *UnicodeStringSource* specificato include un carattere di terminazione null e se il *UTF8StringMaxByteCount* specificato non ha causato il troncamento.

Se l'output viene troncato e viene rilevato un carattere di input non valido, la funzione restituisce un errore di buffer di stato \_ \_ troppo \_ piccolo.

Se *UTF8StringDestination* è impostato su **null** , la funzione restituirà il numero di byte richiesto per ospitare la stringa tradotta senza troncamenti in *UTF8StringActualByteCount*.

I chiamanti di **RtlUnicodeToUTF8N** devono essere in esecuzione a livello IRQL < livello di invio \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




