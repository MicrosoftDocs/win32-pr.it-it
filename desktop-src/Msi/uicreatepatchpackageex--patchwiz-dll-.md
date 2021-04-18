---
description: La funzione UiCreatePatchPackageEx accetta un file di creazione del pacchetto (file con estensione PCP) e genera un pacchetto di patch Windows Installer (pacchetto msp). La chiamata di Msimsp.exe è il metodo consigliato per l'utilizzo di Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: UiCreatePatchPackageEx (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305626"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a>UiCreatePatchPackageEx (Patchwiz.dll)

La funzione UiCreatePatchPackageEx accetta un file di creazione del pacchetto (file con estensione PCP) e genera un pacchetto di patch Windows Installer (pacchetto msp). La chiamata di [Msimsp.exe](msimsp-exe.md) è il metodo consigliato per l'utilizzo di [Patchwiz.dll](patchwiz-dll.md).

La funzione UiCreatePatchPackageEx è disponibile a partire dalla versione Patchwiz.dll 4,0 ed estende la funzionalità della funzione [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*
</dt> <dd>

Percorso completo del file delle proprietà di creazione della patch (file con estensione PCP) per questa patch.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

Percorso completo del pacchetto di patch Windows Installer (file con estensione msp) da creare. Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso. Se è **null** o una stringa vuota, la funzione utilizza il valore di PatchOutputPath nella [tabella Properties (Patchwiz.dll)](properties-table-patchwiz-dll-.md).

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*
</dt> <dd>

Percorso completo di un file di log di testo che verrà accodato. Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*
</dt> <dd>

Handle per una finestra che Visualizza il testo dello stato. Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*
</dt> <dd>

Percorso dei file temporanei. Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso. L'utente deve disporre di privilegi sufficienti per la lettura e la scrittura in questa cartella. Il percorso predefinito è% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Se **true**, rimuovere la cartella temporanea e tutti i relativi contenuti, se presenti. Se **false** e la cartella è presente, la funzione ha esito negativo.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Questo parametro può essere impostato su uno o una combinazione dei valori seguenti per specificare le opzioni di registrazione o dell'interfaccia utente.



| Flag            | valore       | Significato                                  |
|-----------------|-------------|------------------------------------------|
| LOGNONE         | 0x00000000  | Non scrivere alcun messaggio nel log.            |
| LOGINFO         | 0x00000001  | Scrivere messaggi informativi nel log. |
| LOGWARN         | 0x00000002  | Scrivere gli avvisi nel log.               |
| LOGERR          | 0x00000004  | Scrivere i messaggi di errore nel log.         |
| LOGPERFMESSAGES | 0x00000008  | Scrivere i messaggi relativi alle prestazioni nel log.   |
| UINONE          | 0x00000000f | Non visualizzare l'interfaccia utente.       |
| UIALL           | 0x00000010  | Visualizzare l'interfaccia utente.              |



 

</dd> <dt>

<span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*
</dt> <dd>

Riservato. Questo parametro deve essere impostato su zero.

</dd> </dl>

## <a name="return-values"></a>Valori restituiti

Vedere la tabella in [valori restituiti per UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Commenti

Per un esempio di creazione di un file con estensione PCP e uso di [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) per generare un pacchetto di patch di Windows Installer, vedere la sezione esempio di applicazione di [patch per un piccolo aggiornamento](a-small-update-patching-example.md).

Per la creazione di una patch è necessaria un'immagine di installazione non compressa, ad esempio un'immagine amministrativa o un'immagine di configurazione non compressa da un CD-ROM. [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) non genera patch binarie per i file nei file CAB.

 

 



