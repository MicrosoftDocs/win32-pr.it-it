---
description: La funzione CorePrinterDriverInstalled segnala se è installato un driver della stampante principale con un GUID, una data e una versione specificati.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Funzione CorePrinterDriverInstalled (winspool. h)
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
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057906"
---
# <a name="coreprinterdriverinstalled-function"></a>CorePrinterDriverInstalled (funzione)

La funzione **CorePrinterDriverInstalled** segnala se è installato un driver della stampante principale con un GUID, una data e una versione specificati.

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

*pszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa. Utilizzare **null** per il computer locale.

</dd> <dt>

*pszEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86. Può essere **null**.

</dd> <dt>

*CoreDriverGUID* \[ in\]
</dt> <dd>

GUID del driver della stampante principale.

</dd> <dt>

*ftDriverDate* \[ in\]
</dt> <dd>

Data del driver della stampante principale.

</dd> <dt>

*dwlDriverVersion* \[ in\]
</dt> <dd>

Versione del driver della stampante principale.

</dd> <dt>

*pbDriverInstalled* \[ out\]
</dt> <dd>

Puntatore a **true** se il driver, o una versione più recente, è installato; in caso contrario, **false** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.

Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **CorePrinterDriverInstalledW** (Unicode) e **CorePrinterDriverInstalledA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

