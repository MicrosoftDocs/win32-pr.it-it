---
description: Converte la stringa Unicode specificata in una nuova stringa di caratteri usando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Funzione RtlUnicodeToUTF8N (Wdm.h)
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
ms.openlocfilehash: 3580eb86deba77bcc214cf69fbd21f65fee2735ef3a5ff73319b415d2c814d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538031"
---
# <a name="rtlunicodetoutf8n-function"></a>Funzione RtlUnicodeToUTF8N

Converte la stringa Unicode specificata in una nuova stringa di caratteri usando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.

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

*UTF8StringDestination* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer allocato dal chiamante per ricevere la stringa convertita.

</dd> <dt>

*UTF8StringMaxByteCount* \[ Pollici\]
</dt> <dd>

Numero massimo di byte da scrivere in *UTF8StringDestination.* Se questo valore causa il troncamento della stringa convertita, **RtlUnicodeToUTF8N** restituisce uno stato di errore.

</dd> <dt>

*UTF8StringActualByteCount* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile allocata dal chiamante che riceve la lunghezza, in byte, della stringa convertita. Questo parametro è facoltativo e può essere **NULL.** Se la stringa viene troncata, il numero restituito conta il conteggio effettivo delle stringhe troncate.

</dd> <dt>

*UnicodeStringSource* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa di origine Unicode da convertire.

</dd> <dt>

*UnicodeStringByteCount * \[ in\]
</dt> <dd>

Specifica il numero di byte nella stringa di origine Unicode a cui punta il *parametro UnicodeStringSource.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**RtlUnicodeToUTF8N** restituisce uno dei valori NTSTATUS seguenti:



| Codice restituito                                                                                                  | Descrizione                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATO \_ RIUSCITO**</dt> </dl>               | La stringa Unicode è stata convertita in UTF-8.<br/>                                                           |
| <dl> <dt>**STATO \_ DI ALCUNI NON \_ \_ MAPPATI**</dt> </dl>     | È stato rilevato e sostituito un carattere di input non valido. Questo stato viene considerato uno stato di esito positivo.<br/> |
| <dl> <dt>**STATO \_ PARAMETRO NON \_ VALIDO**</dt> </dl>    | Entrambi i puntatori *a UTF8StringDestination* *e UTF8StringActualByteCount* erano **NULL.**<br/>              |
| <dl> <dt>**STATO \_ PARAMETRO NON VALIDO \_ \_ 4**</dt> </dl> | *UnicodeStringSource era* **NULL.**<br/>                                                              |
| <dl> <dt>**BUFFER \_ DI STATO TROPPO \_ \_ PICCOLO**</dt> </dl>    | *UTF8StringDestination* è stato troncato.<br/>                                                               |



 

## <a name="remarks"></a>Commenti

Anche *se UTF8StringActualByteCount* è facoltativo e può essere **NULL,** i chiamanti devono fornire spazio di archiviazione, perché la lunghezza ricevuta può essere usata per determinare se la conversione ha avuto esito positivo. Questa routine non modifica la stringa di origine. Restituisce una stringa UTF-8 con terminazione Null se l'oggetto *UnicodeStringSource* specificato include un terminatore NULL e se l'oggetto *UTF8StringMaxByteCount* specificato non ha causato il troncamento.

Se l'output viene troncato e viene rilevato un carattere di input non valido, la funzione restituisce l'errore STATUS \_ BUFFER \_ TOO \_ SMALL.

Se *UTF8StringDestination* è impostato su **NULL,** la funzione restituirà il numero necessario di byte per ospitare la stringa convertita senza alcun troncamento in *UTF8StringActualByteCount.*

I chiamanti **di RtlUnicodeToUTF8N** devono essere in esecuzione in IRQL < DISPATCH \_ LEVEL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wdm.h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




