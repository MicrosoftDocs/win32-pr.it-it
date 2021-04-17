---
description: ICE03 convalida i tipi di dati e le chiavi esterne in base alla \_ tabella di convalida e alle tabelle del database nel file con estensione msi.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017c13ee568a0efe4d88c28594fb568a7b4a0736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232251"
---
# <a name="ice03"></a>ICE03

ICE03 convalida i tipi di dati e le chiavi esterne in base alla [ \_ tabella di convalida](-validation-table.md) e alle tabelle del database nel file con estensione msi.

## <a name="result"></a>Risultato

ICE03 inserisce i messaggi seguenti per gli errori di convalida.



| Messaggio di errore ICE03                                                       | Descrizione                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chiave primaria duplicata                                                     | Le chiavi primarie di una nuova riga duplicano le chiavi primarie di una riga esistente. La colonna nullable della [ \_ tabella di convalida](-validation-table.md) Mostra le chiavi primarie nel database.                                                                                              |
| Non è una colonna nullable                                                     | Una colonna di tabella non specificata come Nullable nella colonna nullable della [ \_ tabella di convalida](-validation-table.md) contiene una voce null.                                                                                                                                |
| Chiave esterna non valida                                                   | Una colonna che rappresenta una chiave esterna in una seconda tabella contiene una voce che non esiste nella chiave primaria della seconda tabella.                                                                                                                                                          |
| Il valore supera MaxValue                                                    | Il valore numerico di una voce in una tabella di database supera il limite massimo specificato per questo campo nella colonna MaxValue della [ \_ tabella di convalida](-validation-table.md).                                                                                                           |
| Valore inferiore a MinValue                                                      | Il valore numerico di una voce in una tabella di database è inferiore al limite minimo specificato per questo campo nella colonna MinValue della tabella di [ \_ convalida](-validation-table.md).                                                                                                      |
| Il valore non è un membro del set                                             | Il valore di una voce in una tabella di database non è un membro del set accettabile di valori specificati per questo campo nella colonna set della tabella di [ \_ convalida](-validation-table.md).                                                                                                  |
| Stringa di versione non valida                                                    | Vedere il tipo di dati [Version](version.md) .                                                                                                                                                                                                                                                 |
| Tutti i caratteri maiuscoli richiesti                                                   | Vedere il tipo di dati [maiuscolo](uppercase.md) .                                                                                                                                                                                                                                             |
| Stringa GUID non valida                                                       | Vedere il tipo di dati [GUID](guid.md) .                                                                                                                                                                                                                                                       |
| Nome file/utilizzo non valido dei caratteri jolly                                      | Il database contiene un nome di file non valido o un carattere jolly errato. Vedere il tipo di dati [WildCardFilename](wildcardfilename.md) .                                                                                                                                                          |
| Identificatore non valido                                                        | Vedere il tipo di dati [Identifier](identifier.md) .                                                                                                                                                                                                                                           |
| ID lingua non valido                                                       | Il database contiene un identificatore di lingua numerica (LANGID) non valido. Vedere il tipo di dati del [linguaggio](language.md) . Vedere [costanti e stringhe degli identificatori di lingua](../intl/language-identifier-constants-and-strings.md). Ad esempio, 1033 per gli Stati Uniti e 0 per la lingua neutra.<br/> |
| Nome file non valido                                                          | Vedere il tipo di dati [filename](filename.md) .                                                                                                                                                                                                                                               |
| Percorso completo non valido                                                         | Vedere i tipi di dati [path](path.md), [AnyPath](anypath.md) [e paths](paths.md) .                                                                                                                                                                                                      |
| Stringa condizionale non valida                                                    | Il database contiene una stringa condizionale non valida. Si tratta di una stringa di testo che deve restituire TRUE o FALSE in base alla [sintassi dell'istruzione condizionale](conditional-statement-syntax.md). Vedere il tipo di dati [Condition](condition.md) .                                           |
| Stringa di formato non valida                                                     | Vedere il tipo di dati [formattato](formatted.md) .                                                                                                                                                                                                                                             |
| Stringa modello non valida                                                   | Vedere il tipo di dati del [modello](template.md) .                                                                                                                                                                                                                                               |
| Stringa DefaultDir non valida                                                 | Vedere il tipo di dati [DefaultDir](defaultdir.md) .                                                                                                                                                                                                                                           |
| Percorso del registro di sistema non valido                                                     | Vedere il tipo di dati [regpath](regpath.md) .                                                                                                                                                                                                                                                 |
| Dati CustomSource non validi                                                     | Vedere il tipo di dati [CustomSource](customsource.md) .                                                                                                                                                                                                                                       |
| Stringa di proprietà non valida                                                   | Vedere il tipo di dati della [Proprietà](property.md) .                                                                                                                                                                                                                                               |
| Dati mancanti nella \_ tabella di convalida o nel database obsoleto                        | Nel database sono presenti colonne che non sono elencate nella colonna colonna della [ \_ tabella di convalida](-validation-table.md). Il database e la \_ tabella di convalida non corrispondono                                                                                                           |
| Sintassi/nome del cabinet non valido                                                   | Vedere il tipo di dati [CAB](cabinet.md) .                                                                                                                                                                                                                                                 |
| \_Tabella di convalida: stringa di categoria non valida                               | Si tratta di un errore durante la creazione della \_ tabella di convalida. La convalida non riconosce la stringa di categoria utilizzata per questa particolare colonna nella \_ tabella di convalida. Vedere [tipi di dati di colonna](column-data-types.md) e specificare una categoria valida.                                           |
| \_Tabella di convalida: i dati nella colonna della tabella sono errati                  | La colonna della tabella di \_ convalida fa riferimento a una tabella che non esiste nel database.                                                                                                                                                                                     |
| \_Tabella di convalida: valore nella colonna MaxValue < che nella colonna MinValue | Si tratta di un errore durante la creazione della [ \_ tabella di convalida](-validation-table.md). Il valore minimo deve essere minore o uguale al valore massimo.                                                                                                                                                              |
| Destinazione di collegamento non valida                                                       | Vedere il tipo di dati del [collegamento](shortcut.md) .                                                                                                                                                                                                                                               |
| Overflow di stringa (maggiore della lunghezza consentita nella colonna)                 | La lunghezza della stringa è maggiore della larghezza della colonna specificata dalla definizione di colonna. Si noti che il programma di installazione non limita internamente la larghezza della colonna al valore specificato. Vedere [formato della definizione di colonna](column-definition-format.md).                                         |
| Errore non definito                                                           | Errore sconosciuto.                                                                                                                                                                                                                                                                            |
| Impossibile localizzare la colonna                                                | Impossibile localizzare colonne chiave primaria.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 
