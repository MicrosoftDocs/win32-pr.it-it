---
description: ICE03 convalida i tipi di dati e le chiavi esterne in base alla tabella Validation e alle tabelle di \_ database nel file .msi dati.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814bb8023b32c85e752201909f77bd851ec3545c907c03e1c2349a34117d4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946645"
---
# <a name="ice03"></a>ICE03

ICE03 convalida i tipi di dati e le chiavi esterne in base alla [ \_ tabella Validation](-validation-table.md) e alle tabelle di database nel file .msi dati.

## <a name="result"></a>Risultato

ICE03 invia i messaggi seguenti per gli errori di convalida.



| Messaggio di errore ICE03                                                       | Descrizione                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Duplica chiave primaria                                                     | Le chiavi primarie di una nuova riga duplicano le chiavi primarie di una riga esistente. La colonna Nullable della [ \_ tabella Validation mostra](-validation-table.md) le chiavi primarie nel database.                                                                                              |
| Colonna non nullable                                                     | Una colonna di tabella non specificata come nullable nella colonna Nullable della tabella [ \_ Validation](-validation-table.md) contiene una voce Null.                                                                                                                                |
| Chiave esterna non valida                                                   | Una colonna che rappresenta una chiave esterna in una seconda tabella contiene una voce che non esiste nella chiave primaria della seconda tabella.                                                                                                                                                          |
| Il valore supera MaxValue                                                    | Il valore numerico di una voce in una tabella di database supera il limite massimo specificato per questo campo nella colonna MaxValue della [ \_ tabella Validation](-validation-table.md).                                                                                                           |
| Valore inferiore a MinValue                                                      | Il valore numerico di una voce in una tabella di database è minore del limite minimo specificato per questo campo nella colonna MinValue della tabella [ \_ Validation](-validation-table.md).                                                                                                      |
| Valore non membro del set                                             | Il valore di una voce in una tabella di database non è un membro del set di valori accettabile specificato per questo campo nella colonna Set della [ \_ tabella Validation](-validation-table.md).                                                                                                  |
| Stringa di versione non valida                                                    | Vedere il [tipo di](version.md) dati Version.                                                                                                                                                                                                                                                 |
| Tutte maiuscole obbligatorie                                                   | Vedere il [tipo di dati UpperCase.](uppercase.md)                                                                                                                                                                                                                                             |
| Stringa GUID non valida                                                       | Vedere il tipo di dati [GUID.](guid.md)                                                                                                                                                                                                                                                       |
| Nome file/utilizzo di caratteri jolly non valido                                      | Il database contiene un nome file non valido o un carattere jolly non corretto. Vedere il [tipo di dati WildCardFilename.](wildcardfilename.md)                                                                                                                                                          |
| Identificatore non valido                                                        | Vedere Il tipo [di dati](identifier.md) Identificatore.                                                                                                                                                                                                                                           |
| ID lingua non valido                                                       | Il database contiene un identificatore di lingua numerico (LANGID) non valido. Vedere Il tipo [di dati](language.md) Language. Vedere [Costanti e stringhe degli identificatori di linguaggio.](../intl/language-identifier-constants-and-strings.md) Ad esempio, 1033 per gli Stati Uniti e 0 per la lingua neutra.<br/> |
| Nome file non valido                                                          | Vedere il tipo [di dati Filename.](filename.md)                                                                                                                                                                                                                                               |
| Percorso completo non valido                                                         | Vedere i [tipi di](path.md)dati Path , [AnyPath](anypath.md) [e Paths.](paths.md)                                                                                                                                                                                                      |
| Stringa condizionale non valida                                                    | Il database contiene una stringa condizionale non valida. Si tratta di una stringa di testo che deve restituire TRUE o FALSE in base alla [sintassi dell'istruzione condizionale](conditional-statement-syntax.md). Vedere il [tipo di](condition.md) dati Condizione.                                           |
| Stringa di formato non valida                                                     | Vedere Il [tipo di dati](formatted.md) Formattato.                                                                                                                                                                                                                                             |
| Stringa di modello non valida                                                   | Vedere Il [tipo di](template.md) dati Modello.                                                                                                                                                                                                                                               |
| Stringa DefaultDir non valida                                                 | Vedere il [tipo di dati DefaultDir.](defaultdir.md)                                                                                                                                                                                                                                           |
| Percorso del Registro di sistema non valido                                                     | Vedere il [tipo di dati RegPath.](regpath.md)                                                                                                                                                                                                                                                 |
| Dati CustomSource non validi                                                     | Vedere il [tipo di dati CustomSource.](customsource.md)                                                                                                                                                                                                                                       |
| Stringa di proprietà non valida                                                   | Vedere Il [tipo di dati](property.md) Proprietà.                                                                                                                                                                                                                                               |
| Dati mancanti nella \_ tabella di convalida o nel database precedente                        | Nel database sono presenti colonne non elencate nella colonna Colonna della [ \_ tabella Convalida](-validation-table.md). Il database e \_ la tabella di convalida non corrispondono                                                                                                           |
| Sintassi/nome dell'archivio non valido                                                   | Vedere il [tipo di dati Cab.](cabinet.md)                                                                                                                                                                                                                                                 |
| \_Tabella di convalida: stringa di categoria non valida                               | Si tratta di un errore durante la creazione della \_ tabella Validation. La convalida non riconosce la stringa di categoria usata per questa particolare colonna nella \_ tabella Convalida. Vedere [Tipi di dati delle colonne](column-data-types.md) e specificare una categoria valida.                                           |
| \_Tabella di convalida: i dati nella colonna KeyTable non sono corretti                  | La colonna KeyTable nella \_ tabella Validation fa riferimento a una tabella che non esiste nel database.                                                                                                                                                                                     |
| \_Tabella di convalida: valore nella colonna MaxValue < nella colonna MinValue | Si tratta di un errore durante la creazione della [ \_ tabella di convalida](-validation-table.md). Min deve essere sempre minore o uguale a Max.                                                                                                                                                              |
| Destinazione collegamento non erta                                                       | Vedere Il tipo [di dati Collegamento.](shortcut.md)                                                                                                                                                                                                                                               |
| Overflow della stringa (lunghezza maggiore di consentita nella colonna)                 | La lunghezza della stringa è maggiore della larghezza della colonna specificata dalla definizione della colonna. Si noti che il programma di installazione non limita internamente la larghezza della colonna al valore specificato. Vedere [Formato di definizione della colonna.](column-definition-format.md)                                         |
| Errore non definito                                                           | Errore sconosciuto.                                                                                                                                                                                                                                                                            |
| La colonna non può essere localizzata                                                | Le colonne chiave primaria non possono essere localizzate.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 
