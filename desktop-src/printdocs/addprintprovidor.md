---
description: La funzione AddPrintProvidor installa un provider di stampa locale e collega i file di configurazione, i dati e il provider.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Funzione AddPrintProvidor (winspool. h)
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
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311564"
---
# <a name="addprintprovidor-function"></a>AddPrintProvidor (funzione)

La funzione **AddPrintProvidor** installa un provider di stampa locale e collega i file di configurazione, i dati e il provider.

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

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il provider. Per i sistemi che supportano solo l'installazione locale di provider, questo parametro deve essere **null**.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Livello della struttura a cui punta *pProviderInfo* . Può essere uno dei seguenti.



| Valore                                                                                                | Significato                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | La funzione usa una struttura [**PROVIDOR \_ info \_ 1**](providor-info-1.md) .<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | La funzione usa una struttura [**PROVIDOR \_ info \_ 2**](providor-info-2.md) .<br/> |



 

</dd> <dt>

*pProviderInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura di provider di stampa, come indicato dal *livello*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Prima che un'applicazione chiami la funzione **AddPrintProvidor** , tutti i file richiesti dal provider devono essere copiati nella directory system32.

Un provider aggiunto da **AddPrintProvidor** può essere rimosso chiamando [**DeletePrintProvidor**](deleteprintprovidor.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrintProvidorW** (Unicode) e **AddPrintProvidorA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrintProvidor**](deleteprintprovidor.md)
</dt> <dt>

[**PROVIDOR \_ info \_ 1**](providor-info-1.md)
</dt> <dt>

[**PROVIDOR \_ info \_ 2**](providor-info-2.md)
</dt> </dl>

 

 




