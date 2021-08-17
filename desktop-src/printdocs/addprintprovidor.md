---
description: La funzione AddPrintProvidor installa un provider di stampa locale e collega la configurazione, i dati e i file del provider.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Funzione AddPrintProvidor (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ca968397441765455e74059201c128be53f50916e5e28212c700078f52124fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868736"
---
# <a name="addprintprovidor-function"></a>Funzione AddPrintProvidor

La **funzione AddPrintProvidor** installa un provider di stampa locale e collega la configurazione, i dati e i file del provider.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server in cui deve essere installato il provider. Per i sistemi che supportano solo l'installazione locale dei provider, questo parametro deve essere **NULL.**

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Livello della struttura a cui *punta pProviderInfo.* Può essere uno dei seguenti.



| Valore                                                                                                | Significato                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | La funzione usa una [**struttura PROVIDOR \_ INFO \_ 1.**](providor-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La funzione usa una [**struttura PROVIDOR \_ INFO \_ 2.**](providor-info-2.md)<br/> |



 

</dd> <dt>

*pProviderInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura del provider di stampa, come indicato da *Level*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. Chiamando questa funzione da un thread che gestisce l'interazione con l'interfaccia utente, l'applicazione potrebbe non rispondere.

 

Prima che un'applicazione chiami **la funzione AddPrintProvidor,** tutti i file richiesti dal provider devono essere copiati nella directory SYSTEM32.

Un provider aggiunto da **AddPrintProvidor** può essere rimosso chiamando [**DeletePrintProvidor**](deleteprintprovidor.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrintProvidorW** (Unicode) e **AddPrintProvidorA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**PROVIDOR \_ INFO \_ 1**](providor-info-1.md)
</dt> <dt>

[**PROVIDOR \_ INFO \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




