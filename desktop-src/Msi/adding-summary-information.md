---
description: È necessario definire le proprietà delle informazioni di riepilogo seguenti in ogni pacchetto di installazione, usando uno strumento software per accedere all'interfaccia IStream del flusso di informazioni di riepilogo.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Aggiunta di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26486e0082a05b05fbdc9609881083e10cddb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131502"
---
# <a name="adding-summary-information"></a>Aggiunta di informazioni di riepilogo

È necessario definire le proprietà delle informazioni di riepilogo seguenti in ogni pacchetto di installazione, usando uno strumento software per accedere all'interfaccia **IStream** del [flusso di informazioni di riepilogo](summary-information-stream.md). Ad esempio, è possibile usare lo strumento Msiinfo.exe fornito con Windows Installer SDK per impostare queste proprietà. Se queste proprietà non vengono impostate, non verrà superata la [convalida del pacchetto](package-validation.md).



| Proprietà informazioni di riepilogo                                                   | Data                                   | Note                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modello**](template-summary.md)(piattaforma e linguaggio)<br/>         | ; 1033                                  | Piattaforma e linguaggio utilizzati dal database. Se la specifica della piattaforma non è presente nel valore della proprietà di riepilogo del [**modello**](template-summary.md) , il programma di installazione presuppone l'architettura Intel. La proprietà [**ProductLanguage**](productlanguage.md) del database viene in genere utilizzata per questa proprietà di riepilogo. L'ID di lingua dell'esempio indica che il pacchetto utilizza l'inglese (Stati Uniti). |
| [**Numero revisione**](revision-number-summary.md)(codice pacchetto)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | [GUID](guid.md) del codice del pacchetto che identifica in modo univoco il pacchetto di esempio. Se si riproduce questo esempio, usare un'utilità, ad esempio GUIDGEN, per generare un GUID diverso per il pacchetto. I risultati di GUIDGEN contengono caratteri minuscoli. si noti che è necessario modificare tutti i caratteri minuscoli in maiuscolo per un codice di pacchetto valido. Vedere [codici di pacchetto](package-codes.md).             |
| [**Conteggio pagine**](page-count-summary.md)(versione minima del programma di installazione)<br/> | 200                                    | Per un valore minimo di Windows Installer 2,0, questa proprietà deve essere impostata sul valore integer 200.                                                                                                                                                                                                                                                                                                                 |
| [**Conteggio parole**](word-count-summary.md)(tipo di origine)<br/>            | 0                                      | Il tipo di origine globale per il pacchetto è un nome di file lungo e non compresso. Per ulteriori informazioni, vedere [origini compresse e non compresse](compressed-and-uncompressed-sources.md) e la descrizione della colonna attributi della [tabella file](file-table.md) .                                                                                                                                |



 

Le proprietà del flusso di informazioni di riepilogo rimanenti non sono necessarie, ma devono essere impostate per l'esempio MNP2000.msi.



| Proprietà informazioni di riepilogo                                 | Data                                                                             | Note                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Titolo**](title-summary.md)                               | Database di installazione                                                            | Informa gli utenti che il database è per un'installazione anziché una trasformazione o una patch.                        |
| [**Oggetto**](subject-summary.md)                           | MNP2000                                                                          | I browser file possono visualizzarlo come prodotto da installare con il database.                                  |
| [**Parole chiave**](keywords-summary.md)                         | Programma di installazione, MSI, database                                                         | I browser di file in grado di eseguire ricerche di parole chiave possono cercare queste parole.                                    |
| [**Autore**](author-summary.md)                             | Microsoft Corporation                                                            | Nome del produttore del prodotto.                                                                                |
| [**Commenti**](comments-summary.md)                         | Questo database del programma di installazione contiene la logica e i dati necessari per installare il blocco note. | Informa gli utenti sullo scopo di questo database.                                                                  |
| [**Creazione dell'applicazione**](creating-application-summary.md) | Orca                                                                             | Applicazione utilizzata per creare il database di installazione. Nell'esempio viene specificato come esempio l'editor di database Orca. |
| [**Sicurezza**](security-summary.md)                         | 0                                                                                | Il database di esempio è di lettura/scrittura senza restrizioni.                                                                    |



 

Per completare questo database di esempio, non è necessario impostare le proprietà per l' [**ultimo salvataggio**](last-saved-by-summary.md), la data e l'ora dell'ultimo [**salvataggio**](last-saved-time-date-summary.md), la data e l' [**ora di creazione**](create-time-date-summary.md), [**l'ultima stampa**](last-printed-summary.md), il [**numero di caratteri**](character-count-summary.md)e il riepilogo delle tabelle [**codici**](codepage-summary.md) . L'esempio si basa sullo strumento di modifica del database per impostare e aggiornare le proprietà facoltative.

Ad esempio, per utilizzare MsiInfo per aggiungere le informazioni di riepilogo all'esempio, passare alla directory contenente il database e utilizzare la riga di comando seguente. Non riutilizzare l'ID del pacchetto di esempio illustrato di seguito.

**Msiinfo.exe MNP2000.msi-T "database di installazione"-J oggetto-A "Microsoft Corporation"-K "Installer, MSI, database"-O "questo database del programma di installazione contiene la logica e i dati necessari per l'installazione del blocco note."-P; 1033-V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3}-G 200-W 0-N Orca-U 0**

Per altri dettagli sulle informazioni di riepilogo, vedere informazioni sul [flusso di informazioni di riepilogo](about-the-summary-information-stream.md), [uso del flusso di informazioni](using-the-summary-information-stream.md)di riepilogo e [riferimento al flusso di informazioni di riepilogo](summary-information-stream-reference.md).

Per un elenco completo di tutte le proprietà delle informazioni di riepilogo e le descrizioni delle proprietà di [Riepilogo](summary-property-descriptions.md) per la descrizione, vedere la [proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md) .

[Continua](importing-the-user-interface.md)

 

 




