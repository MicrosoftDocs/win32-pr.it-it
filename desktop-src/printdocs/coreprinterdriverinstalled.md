---
description: La funzione CorePrinterDriverInstalled indica se è installato un driver della stampante core con un GUID, una data e una versione specificati.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Funzione CorePrinterDriverInstalled (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 014b9932046ab6d66b64794bbe042f43a390f9f6a4b6183d36a6338eca434526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719771"
---
# <a name="coreprinterdriverinstalled-function"></a>Funzione CorePrinterDriverInstalled

La **funzione CorePrinterDriverInstalled** indica se è installato un driver della stampante core con un GUID, una data e una versione specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il nome del server di stampa. Usare **NULL** per il computer locale.

</dd> <dt>

*pszEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **NULL.**

</dd> <dt>

*Guida di base* \[ Pollici\]
</dt> <dd>

GUID del driver della stampante principale.

</dd> <dt>

*ftDriverDate* \[ Pollici\]
</dt> <dd>

Data del driver della stampante principale.

</dd> <dt>

*dwlDriverVersion* \[ Pollici\]
</dt> <dd>

Versione del driver della stampante principale.

</dd> <dt>

*pbDriverInstalled* \[ Cambio\]
</dt> <dd>

Puntatore a **TRUE se** è installato il driver o una versione più recente, FALSE in **caso contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è S OK. In \_ caso contrario, **HRESULT** conterrà un codice di errore.

Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **CorePrinterDriverInstalledW** (Unicode) e **CorePrinterDriverInstalledA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

