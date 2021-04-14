---
description: Recupera il GUID, la versione e la data dei driver della stampante principale specificati e il percorso dei pacchetti.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Funzione GetCorePrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345286"
---
# <a name="getcoreprinterdrivers-function"></a>GetCorePrinterDrivers (funzione)

Recupera il GUID, la versione e la data dei driver della stampante principale specificati e il percorso dei pacchetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa. Utilizzare **null** per il computer locale.

</dd> <dt>

*pszEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **null**.

</dd> <dt>

*pszzCoreDriverDependencies* \[ in\]
</dt> <dd>

Puntatore a una stringa multistringa con terminazione null che specifica i GUID dei driver della stampante di base.

</dd> <dt>

*cCorePrinterDrivers* \[ in\]
</dt> <dd>

Numero di stringhe in *pszzCoreDriverDependencies*.

</dd> <dt>

*pCorePrinterDrivers* \[ out\]
</dt> <dd>

Puntatore a una matrice di una o più strutture [**di \_ \_ driver della stampante di base**](core-printer-driver.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.

Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **GetCorePrinterDriversW** (Unicode) e **GetCorePrinterDriversA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

