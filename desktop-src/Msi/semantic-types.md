---
description: Le voci seguenti nelle colonne Format, Type e ContextData della tabella ModuleConfiguration specificano il tipo semantico di informazioni da sostituire nell'elemento configurabile specificato nella colonna Nome della tabella.
ms.assetid: f44e234e-b45a-40be-993d-956b8966c321
title: Tipi semantici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01845bd7790f618794816182bb4b11fc0d13baf9216d17bbd15c63a390a52a90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040301"
---
# <a name="semantic-types"></a>Tipi semantici

Le voci seguenti nelle colonne Format, Type e ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md) specificano il tipo semantico di informazioni da sostituire nell'elemento configurabile specificato nella colonna Nome della tabella.

[Tipi di formato testo](text-format-types.md)



| Formato | Tipo       | ContextData                                                 | Descrizione                                                                                                |
|--------|------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Testo   |            |                                                             | Testo arbitrario. Vedere [Tipo di testo arbitrario](arbitrary-text-type.md).                                        |
| Testo   | Enumerazione       | <A>=<a>;<B>=<b>;<C>=<c> | Valore selezionato da un set. Vedere [Tipo enum](enum-type.md).                                                 |
| Testo   | Formattazione  |                                                             | Valore che incontra la definizione di testo formattato nel programma di installazione. Vedere [Tipo formattato](formatted-type.md). |
| Testo   | RTF        |                                                             | Stringa di testo RTF. Vedere [Tipo RTF](rtf-type.md).                                                          |
| Testo   | Identificatore |                                                             | Stringa di testo conforme a un identificatore Windows [installer](identifier.md).                              |



 

[Tipi di formato Integer](integer-format-types.md)



| Formato  | Tipo | ContextData | Descrizione                                                                  |
|---------|------|-------------|------------------------------------------------------------------------------|
| Intero |      |             | Qualsiasi valore intero. Vedere [Tipo integer arbitrario](arbitrary-integer-type.md). |



 

[Tipi di formato chiave](key-format-types.md)



| Formato | Tipo      | ContextData      | Descrizione                                                                                                            |
|--------|-----------|------------------|------------------------------------------------------------------------------------------------------------------------|
| Chiave    | File      | AssemblyContext  | Consentire agli utenti di configurare chiavi esterne per assembly Win32 o Common Language Runtime. Vedere [Tipo di file](file-type.md). |
| Chiave    | Binary    | Bitmap           | Chiave esterna in una riga di tabella binaria che contiene una bitmap da usare nell'interfaccia utente. Vedere [Tipo binario](binary-type.md).                  |
| Chiave    | Binary    | Icona             | Chiave esterna a una riga di tabella binaria che contiene un'icona da usare nell'interfaccia utente. Vedere [Tipo binario](binary-type.md).                   |
| Chiave    | Binary    | EXE              | Chiave esterna in una riga di tabella binaria contenente un file EXE a 32 bit. Vedere [Tipo binario](binary-type.md).                             |
| Chiave    | Binary    | EXE64            | Chiave esterna in una riga di tabella binaria contenente un file EXE a 32 o 64 bit. Vedere [Tipo binario](binary-type.md).                       |
| Chiave    | Icona      | ShortcutIcon     | Chiave esterna a una riga della tabella Icon che contiene un'icona che può essere utilizzata da un collegamento. Vedere [Tipo di icona](icon-type.md).                |
| Chiave    | Finestra di dialogo    | DialogNext       | Chiave esterna in una riga della tabella Dialog. Vedere [Tipo di finestra di dialogo](dialog-type.md).                                                 |
| Chiave    | Finestra di dialogo    | DialogPrev       | Chiave esterna in una riga della tabella Dialog. Vedere [Tipo di finestra di dialogo](dialog-type.md).                                                 |
| Chiave    | Directory | IsolationDir     | Chiave esterna a una riga della tabella Directory a cui appartengono i file isolati. Vedere [Tipo di directory](directory-type.md).            |
| Chiave    | Directory | ShortcutLocation | Chiave esterna in una riga della tabella Directory in cui deve essere installato un collegamento. Vedere [Tipo di directory](directory-type.md).   |
| Chiave    | Proprietà  |                  | Chiave esterna in una riga di proprietà. Vedere [Tipo di proprietà](property-type.md).                                                 |
| Chiave    | Proprietà  | Pubblico           | Chiave esterna in una riga di proprietà. Vedere [Tipo di proprietà](property-type.md).                                                 |
| Chiave    | Proprietà  | Privato          | Chiave esterna in una riga di proprietà. Vedere [Tipo di proprietà.](property-type.md)                                                 |



 

[Tipi di formato dei campi di bit](bitfield-format-types.md)



| Formato   | Tipo | ContextData                                  | Descrizione                                                                                       |
|----------|------|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| Campo di bit |      | <mask>;<A>=<a>;<B> =b | Modifica un subset di bit in una colonna. Vedere [Tipo di campo di bit arbitrario](arbitrary-bitfield-type.md). |



 

 

 



