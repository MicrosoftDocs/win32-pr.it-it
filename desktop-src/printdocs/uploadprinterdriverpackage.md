---
description: Carica un driver della stampante nell'archivio driver dei server di stampa, in modo che possa essere installato chiamando InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Funzione UploadPrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233341"
---
# <a name="uploadprinterdriverpackage-function"></a>UploadPrinterDriverPackage (funzione)

Carica un driver della stampante nell'archivio driver del server di stampa, in modo che possa essere installato chiamando [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszServer* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa. Utilizzare **null** se il server è il computer locale.

</dd> <dt>

*pszInfPath* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica il percorso di origine del file. inf del driver.

</dd> <dt>

*pszEnvironment* \[ in\]
</dt> <dd>

Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore del server (ad esempio, Windows NT x86). Può essere **null**.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

I possibili valori sono i seguenti:



| Valore                                                                                                                                                                                     | Significato                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <dt>**UPDP_SILENT_UPLOAD**</dt> </dl>             | L'interfaccia utente non verrà visualizzata durante il caricamento.<br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <dt>**UPDP_UPLOAD_ALWAYS**</dt> </dl>             | I file verranno caricati anche se il pacchetto è già presente nell'archivio driver del server.<br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <dt>**UPDP_CHECK_DRIVERSTORE**</dt> </dl> | L'archivio driver del server verrà verificato prima del caricamento per verificare se il pacchetto è già presente. Questa impostazione viene ignorata se è impostato UPDP_UPLOAD_ALWAYS.<br/> |



 

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per l'interfaccia utente di copia.

</dd> <dt>

*pszDestInfPath* \[ out\]
</dt> <dd>

Puntatore al percorso di destinazione, nell'archivio driver, in cui è stato copiato il file. inf del driver.

</dd> <dt>

*pcchDestInfPath* \[ in uscita\]
</dt> <dd>

In input, specifica la dimensione, in caratteri, del buffer *pszDestInfPath* . Nell'output, riceve la dimensione, in caratteri, della stringa di percorso, incluso il carattere null di terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito viene S_OK. in caso contrario, **HRESULT** conterrà un codice di errore.

Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

L'archivio driver è in genere% windir% \\ inf o% windir% \\ system32 \\ DriverStore \\ FileRepository.

È possibile caricare un solo pacchetto alla volta. Se un pacchetto dipende da altri, è necessario caricarlo separatamente.

È possibile caricare solo i pacchetti driver firmati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **UploadPrinterDriverPackageW** (Unicode) e **UploadPrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

