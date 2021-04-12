---
description: La \_ tabella UpgradedFile OptionalData contiene informazioni su file specifici in un'immagine aggiornata. Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Tabella UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233706"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>\_Tabella UpgradedFiles OptionalData (Patchwiz.dll)

La \_ tabella UpgradedFile OptionalData contiene informazioni su file specifici in un'immagine aggiornata. Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La \_ tabella OptionalData di UpgradedFile include le colonne seguenti.



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

Chiave esterna per la colonna aggiornata della [tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave della tabella file. Chiave esterna nella [tabella file](file-table.md) del file con estensione msi dell'immagine aggiornata. Se due o più immagini aggiornate all'interno di una famiglia hanno lo stesso valore FTK, il valore deve fare riferimento allo stesso file. I file condivisi da più immagini di aggiornamento devono avere lo stesso FTK per ridurre al minimo le dimensioni del file CAB.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Il valore in questo campo viene aggiunto all'elenco delimitato da punti e virgola di cartelle nella colonna SymbolPaths della [tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) durante la generazione della patch e può essere usato per aggiungere i file di simboli per un file specifico.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

Impostare su 1 per indicare che la patch è non vitale. Impostare su 0 per indicare che la patch è fondamentale. Se Windows Installer rileva un problema quando si applica questa patch al file specificato nella colonna FTK, il valore in questo campo determina se la finestra di messaggio di errore include un pulsante **Ignora** per consentire all'utente di continuare il processo di applicazione di patch.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

Impostare su un valore diverso da zero se è necessario installare l'intero file specificato nella colonna FTK anziché creare una patch binaria.

</dd> </dl>

 

 



