---
description: Msiinfo.exe è un'utilità della riga di comando che utilizza funzioni di database e funzioni di installazione per modificare o visualizzare il flusso di informazioni di riepilogo di un database.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98291c26678efa8b17b42c08bb34c0d1df16c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884558"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe è un'utilità della riga di comando che utilizza [funzioni di database](database-functions.md) e [funzioni di installazione](installer-functions.md) per modificare o visualizzare il flusso di [informazioni di riepilogo](summary-information-stream.md) di un database.

## <a name="syntax"></a>Sintassi

**MsiInfo** *{database} \[ \[ /b \] /d \] {opzione} {dati}*

-   Il database non può essere un database di sola lettura.
-   Se nessun dato segue un'opzione, la proprietà corrispondente viene rimossa.
-   Nella riga di comando è possibile specificare un massimo di 20 opzioni. Le stesse proprietà possono essere specificate più volte.
-   Se i dati contengono uno spazio, racchiudere i dati tra virgolette. Ad esempio, ad esempio/T "MY TITLE".

## <a name="command-line-options"></a>Opzioni da riga di comando

Msiinfo.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole. Al posto di un trattino, può essere utilizzato anche un delimitatore di barra. Per altre informazioni, vedere [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md).



| Opzione | Descrizione                                                                                                                                                                                                                                                                                                                                                      | ID proprietà        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *nessuna* | Se non viene specificata alcuna opzione, l'utilità Visualizza i valori correnti delle proprietà delle informazioni di riepilogo.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Visualizza le informazioni su ogni stringa nel pool di stringhe. L'opzione-b è valida solo se viene utilizzato anche-d e-b deve precedere l'opzione-d.                                                                                                                                                                                                                 |                    |     |
| -d     | Visualizzare informazioni sul pool di stringhe. Convalida il pool di stringhe e fornisce informazioni sulla tabella codici del database. Si noti che la tabella codici del database è diversa dalla tabella codici del flusso di informazioni di riepilogo (tabella \_ codici PID). Questa opzione controlla anche ogni stringa per i caratteri non validi nella tabella codici del database. |                    |     |
| -i     | Non applicabile. Riservato.                                                                                                                                                                                                                                                                                                                                        | \_dizionario PID    | 0   |
| -c     | Imposta la [**proprietà di riepilogo codepage**](codepage-summary.md).                                                                                                                                                                                                                                                                                                  | tabella \_ codici PID      | 1   |
| -T     | Imposta la [**proprietà di riepilogo del titolo**](title-summary.md).                                                                                                                                                                                                                                                                                                        | \_titolo PID         | 2   |
| -j     | Imposta la [**proprietà di riepilogo dell'oggetto**](subject-summary.md).                                                                                                                                                                                                                                                                                                    | oggetto PID ID \_    | 3   |
| -a     | Imposta la [**proprietà di riepilogo dell'autore**](author-summary.md).                                                                                                                                                                                                                                                                                                      | \_autore PID        | 4   |
| -k     | Imposta la [**proprietà di riepilogo delle parole chiave**](keywords-summary.md).                                                                                                                                                                                                                                                                                                  | \_parole chiave PID      | 5   |
| -o     | Imposta la [**proprietà di riepilogo dei commenti**](comments-summary.md).                                                                                                                                                                                                                                                                                                  | \_Commenti PID      | 6   |
| -p     | Imposta la [**proprietà di riepilogo del modello**](template-summary.md).                                                                                                                                                                                                                                                                                                  | \_modello PID      | 7   |
| -l     | Imposta l' [**ultima proprietà di riepilogo salvata da**](last-saved-by-summary.md).                                                                                                                                                                                                                                                                                        | \_LASTAUTHOR PID    | 8   |
| -v     | Imposta la [**proprietà di riepilogo dei numeri di revisione**](revision-number-summary.md).                                                                                                                                                                                                                                                                                    | \_REVNUMBER PID     | 9   |
| -E     | Non applicabile. Riservato.                                                                                                                                                                                                                                                                                                                                        | \_EDITTIME PID      | 10  |
| -S     | Imposta l' [**ultima proprietà di riepilogo stampata**](last-printed-summary.md). Per specificare l'anno, il mese, il giorno, l'ora, il minuto e il secondo, utilizzare il formato "aaaa/mm/gg hh: mm: SS". Ad esempio, "1997/06/20 03:25:59".                                                                                                                                                     | \_LASTPRINTED PID   | 11  |
| -r     | Imposta la [**proprietà di riepilogo Data e ora di creazione**](create-time-date-summary.md). Per specificare l'anno, il mese, il giorno, l'ora, il minuto e il secondo, utilizzare il formato "aaaa/mm/gg hh: mm: SS". Ad esempio, "1997/06/20 03:25:59".                                                                                                                                             | PID \_ creare il \_ DTM   | 12  |
| -Q     | Imposta la [**proprietà di riepilogo Data e ora dell'ultimo salvataggio**](last-saved-time-date-summary.md). Per specificare l'anno, il mese, il giorno, l'ora, il minuto e il secondo, utilizzare il formato "aaaa/mm/gg hh: mm: SS". Ad esempio, "1997/06/20 03:25:59".                                                                                                                                     | PID \_ LASTSAVE \_ DTM | 13  |
| -g     | Imposta la [**proprietà di riepilogo del conteggio delle pagine**](page-count-summary.md).                                                                                                                                                                                                                                                                                              | \_PageCount PID     | 14  |
| -w     | Imposta la [**proprietà di riepilogo**](word-count-summary.md)per il conteggio delle parole.                                                                                                                                                                                                                                                                                              | \_WORDCOUNT PID     | 15  |
| -H     | Imposta la [**proprietà di riepilogo del numero di caratteri**](character-count-summary.md).                                                                                                                                                                                                                                                                                    | \_charCount PID     | 16  |
|        | Non applicabile. Riservato.                                                                                                                                                                                                                                                                                                                                        | \_Anteprima PID     | 17  |
| -n     | Imposta la [**proprietà di riepilogo della creazione dell'applicazione**](creating-application-summary.md).                                                                                                                                                                                                                                                                          | \_appname PID       | 18  |
| -U     | Imposta la [**Proprietà Riepilogo sicurezza**](security-summary.md).                                                                                                                                                                                                                                                                                                  | \_sicurezza PID      | 19  |



 

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



