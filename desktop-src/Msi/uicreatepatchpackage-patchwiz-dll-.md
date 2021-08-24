---
description: La funzione UiCreatePatchPackage accetta un file di creazione del pacchetto (file con estensione pcp) e genera un pacchetto patch Windows Installer (pacchetto msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2802eb92d9df42a683053198ab14bbe7894fa512c63f25e1cd4afe060ea74c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810501"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>UiCreatePatchPackage (Patchwiz.dll)

La funzione UiCreatePatchPackage accetta un file di creazione del pacchetto (file con estensione pcp) e genera un pacchetto patch Windows Installer (pacchetto msp). La [Msimsp.exe](msimsp-exe.md) è il metodo consigliato per l'uso [ diPatchwiz.dll](patchwiz-dll.md). La [funzione UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) è disponibile nella versione 4.0 di Patchwiz.dll ed estende la funzionalità della funzione UiCreatePatchPackage.

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

Percorso completo del file delle proprietà di creazione della patch (file con estensione pcp) per questa patch.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

Percorso completo del pacchetto Windows di patch del programma di installazione (file msp) da creare. Questo parametro può essere **NULL** o una stringa vuota, ma non può essere omesso. Se è **NULL** o una stringa vuota, la funzione usa il valore di PatchOutputPath nella tabella [delle proprietà (Patchwiz.dll).](properties-table-patchwiz-dll-.md)

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*
</dt> <dd>

Percorso completo di un file di log di testo che verrà aggiunto. Questo parametro può essere **NULL** o una stringa vuota, ma non può essere omesso.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*
</dt> <dd>

Handle per una finestra che visualizza il testo dello stato. Questo parametro può essere **NULL** o una stringa vuota, ma non può essere omesso.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*
</dt> <dd>

Percorso per i file temporanei. Questo parametro può essere **NULL** o una stringa vuota, ma non può essere omesso. Il percorso predefinito è %TMP% \\ ~pcw \_ tmp.tmp. \\

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Se **TRUE,** rimuovere la cartella temporanea e tutto il relativo contenuto, se presente. Se **è presente FALSE** e folder, la funzione ha esito negativo.

</dd> </dl>

## <a name="return-values"></a>Valori restituiti

Vedere la tabella in [Valori restituiti per UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Commenti

Per un esempio di creazione di un file con estensione pcp e l'uso di UiCreatePatchPackage per generare un pacchetto patch del programma di installazione di Windows, vedere la sezione [A Small Update Patching Example](a-small-update-patching-example.md).

La creazione di una patch richiede un'immagine di installazione non compressa, ad esempio un'immagine amministrativa o un'immagine di installazione non compressa da un CD-ROM. UiCreatePatchPackage non genera patch binarie per i file in archivi.

 

 



