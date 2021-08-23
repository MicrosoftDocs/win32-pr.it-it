---
description: La tabella UpgradedFile \_ OptionalData contiene informazioni su file specifici in un'immagine aggiornata. Questa tabella è facoltativa nel database di creazione delle patch (file con estensione pcp) e viene usata dalla funzione UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: UpgradedFiles_OptionalData tabella (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eb766f8db9d295546670c80627284991da1ff8dccb5a0c2900be74bd785dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012839"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>Tabella OptionalData upgradedFiles \_ (Patchwiz.dll)

La tabella UpgradedFile \_ OptionalData contiene informazioni su file specifici in un'immagine aggiornata. Questa tabella è facoltativa nel database di creazione delle patch (file con estensione pcp) e viene usata dalla [funzione UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabella UpgradedFile \_ OptionalData include le colonne seguenti.



| Colonna                  | Tipo    | Chiave | Nullable |
|-------------------------|---------|-----|----------|
| Aggiornato                | text    | S   | N        |
| FTK                     | text    | S   | N        |
| SymbolPaths             | text    |     | S        |
| AllowIgnoreOnPatchError | numero intero |     | S        |
| IncludeWholeFile        | numero intero |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato
</dt> <dd>

Chiave esterna per la colonna Aggiornato della [tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave della tabella file. Chiave esterna nella [tabella File](file-table.md) del .msi file dell'immagine aggiornata. Se due o più immagini aggiornate all'interno di una famiglia hanno lo stesso valore FTK, il valore deve fare riferimento allo stesso file. I file condivisi da più immagini di aggiornamento devono avere lo stesso FTK per ridurre al minimo le dimensioni del file CAB.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Il valore in questo campo viene aggiunto all'elenco delimitato da punto e virgola delle cartelle nella colonna SymbolPaths della tabella [UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) quando viene generata la patch e può essere usato per aggiungere file di simboli per un file specifico.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

Impostare su 1 per indicare che la patch non è essenziale. Impostare su 0 per indicare che la patch è essenziale. Se Windows Installer rileva un problema durante l'applicazione della patch al file specificato nella colonna FTK, il  valore in questo campo determina se la finestra di messaggio di errore include un pulsante Ignora per consentire all'utente di continuare il processo di applicazione delle patch.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

Impostare su un valore diverso da zero se l'intero file specificato nella colonna FTK deve essere installato anziché creare una patch binaria.

</dd> </dl>

 

 



