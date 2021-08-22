---
description: La funzione EnumForms enumera i moduli supportati dalla stampante specificata.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Funzione EnumForms (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c1e5ce18e81e4d775fdc801517867491740a7dd5035fc730226cb084e5af7d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732699"
---
# <a name="enumforms-function"></a>Funzione EnumForms

La **funzione EnumForms** enumera i moduli supportati dalla stampante specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ Pollici\]
</dt> <dd>

Handle per la stampante per cui devono essere enumerati i form. Usare la [**funzione OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle della stampante.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Specifica la versione della struttura a cui *punta pForm.* Questo valore deve essere 1 o 2.

</dd> <dt>

*pForm* \[ Cambio\]
</dt> <dd>

Puntatore a una o [**più strutture FORM INFO \_ \_ 1**](form-info-1.md) o a una o più [**strutture FORM INFO \_ \_ 2.**](form-info-2.md) Tutte le strutture avranno lo stesso livello.

</dd> <dt>

*cbBuf* \[ Pollici\]
</dt> <dd>

Specifica le dimensioni, in byte, del buffer a cui *punta pForm.*

</dd> <dt>

*pcbNeeded* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di byte copiati nella matrice a cui *punta pForm* (se l'operazione ha esito positivo) o il numero di byte necessari (se ha esito negativo perché *cbBuf* è troppo piccolo).

</dd> <dt>

*pcReturned* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di strutture copiate nella matrice a cui *punta pForm.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Se il chiamante è remoto e *Level* è 2, il valore **StringType** delle strutture [**FORM INFO \_ \_ 2**](form-info-2.md) restituite sarà sempre **STRING \_ LANGPAIR.**

In Windows Vista i dati del modulo restituiti da **EnumForms** vengono recuperati da una cache locale quando *hPrinter* fa riferimento a un server di stampa remoto o a una stampante ospitata da un server di stampa ed esiste almeno una connessione aperta a una stampante nel server di stampa remoto. In tutte le altre configurazioni, i dati del modulo vengono sottoposti a query dal server di stampa remoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **EnumFormsW** (Unicode) ed **EnumFormsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**INFORMAZIONI \_ MODULO \_ 1**](form-info-1.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




