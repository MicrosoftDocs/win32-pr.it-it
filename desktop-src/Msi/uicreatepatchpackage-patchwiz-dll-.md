---
description: La funzione UiCreatePatchPackage accetta un file di creazione del pacchetto (file con estensione PCP) e genera un pacchetto di patch Windows Installer (pacchetto msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878545"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>UiCreatePatchPackage (Patchwiz.dll)

La funzione UiCreatePatchPackage accetta un file di creazione del pacchetto (file con estensione PCP) e genera un pacchetto di patch Windows Installer (pacchetto msp). La chiamata di [Msimsp.exe](msimsp-exe.md) è il metodo consigliato per l'utilizzo di [Patchwiz.dll](patchwiz-dll.md). La funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) è disponibile nella versione 4,0 di Patchwiz.dll ed estende la funzionalità della funzione UiCreatePatchPackage.

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
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

Percorso dei file temporanei. Questo parametro può essere **null** o una stringa vuota, ma non può essere omesso. Il percorso predefinito è% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Se **true**, rimuovere la cartella temporanea e tutti i relativi contenuti, se presenti. Se **false** e la cartella è presente, la funzione ha esito negativo.

</dd> </dl>

## <a name="return-values"></a>Valori restituiti

Vedere la tabella in [valori restituiti per UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Commenti

Per un esempio di creazione di un file con estensione PCP e uso di UiCreatePatchPackage per generare un pacchetto di patch di Windows Installer, vedere la sezione esempio di applicazione di [patch per un piccolo aggiornamento](a-small-update-patching-example.md).

Per la creazione di una patch è necessaria un'immagine di installazione non compressa, ad esempio un'immagine amministrativa o un'immagine di configurazione non compressa da un CD-ROM. UiCreatePatchPackage non genera patch binarie per i file nei file CAB.

 

 



