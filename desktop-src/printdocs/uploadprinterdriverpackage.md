---
description: Carica un driver della stampante nell'archivio dei driver dei server di stampa in modo che possa essere installato chiamando InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Funzione UploadPrinterDriverPackage (Winspool.h)
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
ms.openlocfilehash: 15347171299e370bd5e0128976f65e4de1f7034b083b16880ac21659bfac35f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233869"
---
# <a name="uploadprinterdriverpackage-function"></a>Funzione UploadPrinterDriverPackage

Carica un driver della stampante nell'archivio driver del server di stampa in modo che possa essere installato chiamando [**InstallPrinterDriverFromPackage.**](installprinterdriverfrompackage.md)

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

*pszServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il nome del server di stampa. Utilizzare **NULL** se il server è il computer locale.

</dd> <dt>

*pszInfPath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica il percorso di origine del file inf del driver.

</dd> <dt>

*pszEnvironment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa costante con terminazione Null che specifica l'architettura del processore del server, ad esempio Windows NT x86. Può essere **NULL.**

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Può essere uno dei valori seguenti:



| Valore                                                                                                                                                                                     | Significato                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <dt>**UPDP_SILENT_UPLOAD**</dt> </dl>             | L'interfaccia utente non verrà visualizzata durante il caricamento.<br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <dt>**UPDP_UPLOAD_ALWAYS**</dt> </dl>             | I file verranno caricati anche se il pacchetto si trova già nell'archivio driver del server.<br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <dt>**UPDP_CHECK_DRIVERSTORE**</dt> </dl> | L'archivio driver del server verrà controllato prima del caricamento per verificare se il pacchetto è già presente. Questa impostazione viene ignorata se UPDP_UPLOAD_ALWAYS è impostata.<br/> |



 

</dd> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Handle per l'interfaccia utente di copia.

</dd> <dt>

*pszDestInfPath* \[ Cambio\]
</dt> <dd>

Puntatore al percorso di destinazione, nell'archivio driver, in cui è stato copiato il file inf del driver.

</dd> <dt>

*pcchDestInfPath* \[ in, out\]
</dt> <dd>

Nell'input specifica la dimensione, in caratteri, del buffer *pszDestInfPath.* Nell'output riceve la dimensione, in caratteri, della stringa di percorso, incluso il carattere Null di terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito S_OK; in caso contrario, **HRESULT** conterrà un codice di errore.

Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

L'archivio driver è in genere %windir% \\ inf o %windir% \\ System32 \\ DriverStore \\ FileRepository.

È possibile caricare un solo pacchetto alla volta. Se un pacchetto dipende da altri, deve essere caricato separatamente.

È possibile caricare solo pacchetti driver firmati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomi Unicode e ANSI<br/>   | **UploadPrinterDriverPackageW** (Unicode) e **UploadPrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> </dl>

 

