---
description: Msiinfo.exe è un'utilità della riga di comando che usa Funzioni di database e Funzioni del programma di installazione per modificare o visualizzare il flusso di informazioni di riepilogo di un database.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57487406533b060d9343d4afbdf7e5254c32e15149bb3385f81cc7dc3923fc71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628099"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe è un'utilità della riga di [](installer-functions.md) comando che usa Funzioni di [database](database-functions.md) e Funzioni del programma di installazione per modificare o visualizzare il flusso di [informazioni](summary-information-stream.md) di riepilogo di un database.

## <a name="syntax"></a>Sintassi

**MsiInfo** *{database} \[ \[ /B \] /D \] {option}{data}*

-   Il database non può essere di sola lettura.
-   Se nessun dato segue un'opzione, la proprietà corrispondente viene rimossa.
-   Nella riga di comando è possibile specificare un massimo di 20 opzioni. Le stesse proprietà possono essere specificate più volte.
-   Se i dati contengono uno spazio, racchiudere i dati tra virgolette. Ad esempio, ad esempio /T "TITOLO".

## <a name="command-line-options"></a>Opzioni da riga di comando

Msiinfo.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole. È anche possibile usare un delimitatore barra al posto di un trattino. Per altre informazioni, vedere [Summary Information Stream Property Set](summary-information-stream-property-set.md).



| Opzione | Descrizione                                                                                                                                                                                                                                                                                                                                                      | ID proprietà        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *nessuna* | Se non viene specificata alcuna opzione, l'utilità visualizza i valori correnti delle proprietà Informazioni di riepilogo.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Visualizzare informazioni su ogni stringa nel pool di stringhe. L'opzione -b è valida solo se si usa anche -d e -b deve essere prima dell'opzione -d.                                                                                                                                                                                                                 |                    |     |
| -d     | Visualizzare informazioni sul pool di stringhe. Convalida il pool di stringhe e fornisce informazioni sulla tabella codici del database. Si noti che la tabella codici del database è diversa dalla tabella codici del flusso di informazioni di riepilogo \_ (CODEPAGE PID). Questa opzione controlla anche in ogni stringa la presenza di caratteri non validi nella tabella codici del database. |                    |     |
| -i     | Non applicabile. Riservato.                                                                                                                                                                                                                                                                                                                                        | DIZIONARIO \_ PID    | 0   |
| -c     | Imposta la [**proprietà Summary della tabella codici.**](codepage-summary.md)                                                                                                                                                                                                                                                                                                  | TABELLA CODICI \_ PID      | 1   |
| -T     | Imposta la [**proprietà Riepilogo titolo**](title-summary.md).                                                                                                                                                                                                                                                                                                        | TITOLO \_ PID         | 2   |
| -j     | Imposta la [**proprietà Riepilogo oggetto**](subject-summary.md).                                                                                                                                                                                                                                                                                                    | ID PID \_ SUBJECT    | 3   |
| -a     | Imposta la [**proprietà Riepilogo autore**](author-summary.md).                                                                                                                                                                                                                                                                                                      | PID \_ AUTHOR        | 4   |
| -k     | Imposta la [**proprietà Summary delle parole chiave**](keywords-summary.md).                                                                                                                                                                                                                                                                                                  | PAROLE CHIAVE \_ PID      | 5   |
| -o     | Imposta la [**proprietà Riepilogo commenti**](comments-summary.md).                                                                                                                                                                                                                                                                                                  | COMMENTI \_ PID      | 6   |
| -p     | Imposta la [**proprietà riepilogo modello**](template-summary.md).                                                                                                                                                                                                                                                                                                  | MODELLO \_ PID      | 7   |
| -l     | Imposta la [**proprietà Summary dell'ultimo salvataggio in base a**](last-saved-by-summary.md).                                                                                                                                                                                                                                                                                        | PID \_ LASTAUTHOR    | 8   |
| -v     | Imposta la [**proprietà Riepilogo numero revisione**](revision-number-summary.md).                                                                                                                                                                                                                                                                                    | PID \_ REVNUMBER     | 9   |
| -E     | Non applicabile. Riservato.                                                                                                                                                                                                                                                                                                                                        | PID \_ EDITTIME      | 10  |
| -S     | Imposta la [**proprietà Riepilogo ultima stampata**](last-printed-summary.md). Per specificare anno, mese, giorno, ora, minuto e secondo, usare il formato "aaaa/mm/gg hh:mm:ss". Ad esempio, "1997/06/20 03:25:59".                                                                                                                                                     | PID \_ LASTPRINTED   | 11  |
| -r     | Imposta la [**proprietà Riepilogo data/ora di creazione**](create-time-date-summary.md). Per specificare anno, mese, giorno, ora, minuto e secondo, usare il formato "aaaa/mm/gg hh:mm:ss". Ad esempio, "1997/06/20 03:25:59".                                                                                                                                             | PID \_ CREATE \_ DTM   | 12  |
| -Q     | Imposta la [**proprietà Riepilogo data/ora ultimo salvataggio**](last-saved-time-date-summary.md). Per specificare anno, mese, giorno, ora, minuto e secondo, usare il formato "aaaa/mm/gg hh:mm:ss". Ad esempio, "1997/06/20 03:25:59".                                                                                                                                     | PID \_ LASTSAVE \_ DTM | 13  |
| -g     | Imposta la [**proprietà Riepilogo conteggio pagine**](page-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ PAGECOUNT     | 14  |
| -w     | Imposta la [**proprietà Riepilogo conteggio parole**](word-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ WORDCOUNT     | 15  |
| -H     | Imposta la [**proprietà Riepilogo conteggio caratteri**](character-count-summary.md).                                                                                                                                                                                                                                                                                    | PID \_ CHARCOUNT     | 16  |
|        | Non applicabile. Riservato.                                                                                                                                                                                                                                                                                                                                        | ANTEPRIMA \_ PID     | 17  |
| -n     | Imposta la [**proprietà Riepilogo dell'applicazione per la creazione di**](creating-application-summary.md).                                                                                                                                                                                                                                                                          | PID \_ APPNAME       | 18  |
| -U     | Imposta la [**proprietà Riepilogo sicurezza**](security-summary.md).                                                                                                                                                                                                                                                                                                  | SICUREZZA \_ PID      | 19  |



 

Questo strumento è disponibile solo in componenti Windows [SDK per sviluppatori Windows Programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



