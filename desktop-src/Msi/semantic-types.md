---
description: Le voci seguenti nelle colonne format, Type e ContextData della tabella ModuleConfiguration specificano il tipo semantico di informazioni che vengono sostituite nell'elemento configurabile specificato nella colonna Name della tabella.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Tipi semantici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2a0798a9ae7be3c2c0b56483707e3a09f67d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318985"
---
# <a name="semantic-types"></a>Tipi semantici

Le voci seguenti nelle colonne format, Type e ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md) specificano il tipo semantico di informazioni che vengono sostituite nell'elemento configurabile specificato nella colonna Name della tabella.

[Tipi di formato testo](text-format-types.md)



| Formato | Tipo       | ContextData                                                 | Descrizione                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Testo   |            |                                                             | Testo arbitrario. Vedere [tipo di testo arbitrario](arbitrary-text-type.md).                                        |
| Testo   | Enumerazione       | <A>=<a>;<B>=<b>;<C>=<c> | Valore selezionato da un set. Vedere [tipo enum](enum-type.md).                                                 |
| Testo   | Formattazione  |                                                             | Valore che soddisfa la definizione del testo formattato nel programma di installazione. Vedere [tipo formattato](formatted-type.md). |
| Testo   | RTF        |                                                             | Stringa di testo RTF. Vedere [tipo RTF](rtf-type.md).                                                          |
| Testo   | Identificatore |                                                             | Stringa di testo conforme a un [identificatore](identifier.md)Windows Installer.                              |



 

[Tipi di formato Integer](integer-format-types.md)



| Formato  | Tipo | ContextData | Descrizione                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Integer |      |             | Qualsiasi valore intero. Vedere [tipo Integer arbitrario](arbitrary-integer-type.md). |



 

[Tipi di formato chiave](key-format-types.md)



| Formato | Tipo      | ContextData      | Descrizione                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Chiave    | File      | AssemblyContext  | Consente agli utenti di configurare chiavi esterne per gli assembly Win32 o Common Language Runtime. Vedere [tipo di file](file-type.md). |
| Chiave    | Binary    | Bitmap           | Chiave esterna per una riga di tabella binaria che contiene una bitmap da utilizzare nell'interfaccia utente. Vedere [tipo binario](binary-type.md).                  |
| Chiave    | Binary    | Icona             | Chiave esterna per una riga di tabella binaria contenente un'icona da utilizzare nell'interfaccia utente. Vedere [tipo binario](binary-type.md).                   |
| Chiave    | Binary    | EXE              | Chiave esterna per una riga di tabella binaria che contiene un file EXE a 32 bit. Vedere [tipo binario](binary-type.md).                             |
| Chiave    | Binary    | EXE64            | Chiave esterna per una riga di tabella binaria che contiene un file EXE a 32 o a 64 bit. Vedere [tipo binario](binary-type.md).                       |
| Chiave    | Icona      | ShortcutIcon     | Chiave esterna per una riga di tabella icona contenente un'icona per l'uso da un collegamento. Vedere [tipo di icona](icon-type.md).                |
| Chiave    | Finestra di dialogo    | DialogNext       | Chiave esterna per una riga della tabella della finestra di dialogo. Vedere [tipo di finestra di dialogo](dialog-type.md).                                                 |
| Chiave    | Finestra di dialogo    | DialogPrev       | Chiave esterna per una riga della tabella della finestra di dialogo. Vedere [tipo di finestra di dialogo](dialog-type.md).                                                 |
| Chiave    | Directory | IsolationDir     | Chiave esterna per una riga della tabella di directory in cui appartengono i file isolati. Vedere [tipo di directory](directory-type.md).            |
| Chiave    | Directory | ShortcutLocation | Chiave esterna per una riga della tabella di directory in cui deve essere installato un collegamento. Vedere [tipo di directory](directory-type.md).   |
| Chiave    | Proprietà  |                  | Chiave esterna per una riga di proprietà. Vedere [tipo di proprietà](property-type.md).                                                 |
| Chiave    | Proprietà  | Pubblico           | Chiave esterna per una riga di proprietà. Vedere [tipo di proprietà](property-type.md).                                                 |
| Chiave    | Proprietà  | Privato          | Chiave esterna per una riga di proprietà. Vedere [tipo di proprietà](property-type.md).                                                 |



 

[Tipi di formato bit](bitfield-format-types.md)



| Formato   | Tipo | ContextData                                  | Descrizione                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Bit |      | <mask>;<A>=<a>;<B> = b | Modifica un subset di bit in una colonna. Vedere [tipo bit arbitrario](arbitrary-bitfield-type.md). |



 

 

 



