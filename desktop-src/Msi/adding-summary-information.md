---
description: Le proprietà delle informazioni di riepilogo seguenti devono essere definite in ogni pacchetto di installazione, usando uno strumento software per accedere all'interfaccia Istream del flusso di informazioni di riepilogo.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Aggiunta di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dc43ba8df737fb4d7c30998ec6c9581376df6ef6274140e68ec767e3a416f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328581"
---
# <a name="adding-summary-information"></a>Aggiunta di informazioni di riepilogo

Le proprietà delle informazioni di riepilogo seguenti devono essere definite in ogni pacchetto di installazione, usando uno strumento software per accedere **all'interfaccia Istream** del [flusso di informazioni di riepilogo](summary-information-stream.md). Ad esempio, è possibile usare lo strumento Msiinfo.exe con l'SDK Windows Installer per impostare queste proprietà. Se queste proprietà non sono impostate, il pacchetto non supererà [convalida pacchetto](package-validation.md).



| Proprietà Delle informazioni di riepilogo                                                   | Dati                                   | Note                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modello**](template-summary.md)(piattaforma e linguaggio)<br/>         | ;1033                                  | Piattaforma e linguaggio usati dal database. Se la specifica della piattaforma non è presente nel valore [**della proprietà Riepilogo**](template-summary.md) modello, il programma di installazione presuppone l'architettura Intel. La [**proprietà ProductLanguage**](productlanguage.md) del database viene in genere usata per questa proprietà di riepilogo. L'ID lingua dell'esempio indica che il pacchetto usa l'inglese (Stati Uniti). |
| [**Numero di revisione**](revision-number-summary.md)(codice pacchetto)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | Si tratta del GUID del codice [del pacchetto che](guid.md) identifica in modo univoco il pacchetto di esempio. Se si riproduce questo esempio, usare un'utilità come GUIDGEN per generare un GUID diverso per il pacchetto. I risultati di GUIDGEN contengono caratteri minuscoli. Si noti che è necessario modificare tutti i caratteri minuscoli in lettere maiuscole per un codice di pacchetto valido. Vedere [Codici dei pacchetti.](package-codes.md)             |
| [**Conteggio pagine**](page-count-summary.md)(versione minima del programma di installazione)<br/> | 200                                    | Per un minimo Windows Installer 2.0, questa proprietà deve essere impostata sul numero intero 200.                                                                                                                                                                                                                                                                                                                 |
| [**Conteggio parole**](word-count-summary.md)(tipo di origine)<br/>            | 0                                      | Il tipo di origine globale per il pacchetto è nomi di file lunghi e non compressi. Per [altre informazioni, vedere Origini compresse](compressed-and-uncompressed-sources.md) e non compresse e la descrizione della colonna Attributi della tabella [File](file-table.md) .                                                                                                                                |



 

Le proprietà rimanenti del flusso di informazioni di riepilogo non sono necessarie, ma devono essere impostate per l'MNP2000.msi esempio.



| Proprietà Delle informazioni di riepilogo                                 | Dati                                                                             | Note                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Titolo**](title-summary.md)                               | Database di installazione                                                            | Informa gli utenti che il database è per un'installazione anziché per una trasformazione o una patch.                        |
| [**Oggetto**](subject-summary.md)                           | MNP2000                                                                          | I browser di file possono visualizzarlo come prodotto da installare con questo database.                                  |
| [**Parole chiavi**](keywords-summary.md)                         | Programma di installazione, MSI, database                                                         | I browser di file in grado di eseguire la ricerca di parole chiave possono cercare queste parole.                                    |
| [**Autore**](author-summary.md)                             | Microsoft Corporation                                                            | Nome del produttore del prodotto.                                                                                |
| [**Commenti**](comments-summary.md)                         | Questo database del programma di installazione contiene la logica e i dati necessari per installare Blocco note. | Informa gli utenti sullo scopo di questo database.                                                                  |
| [**Creazione di un'applicazione**](creating-application-summary.md) | Orca                                                                             | Applicazione utilizzata per creare il database di installazione. L'esempio specifica l'editor di database Orca come esempio. |
| [**Sicurezza**](security-summary.md)                         | 0                                                                                | Il database di esempio è di lettura/scrittura senza restrizioni.                                                                    |



 

Per completare questo database di esempio, non è [](create-time-date-summary.md)necessario impostare le proprietà di riepilogo [](codepage-summary.md) Ultimo salvataggio, Data/ora ultimo [**salvataggio,**](last-saved-time-date-summary.md)Data creazione, Ultima [**stampa,**](last-printed-summary.md)Conteggio caratteri e Tabella codici. [](last-saved-by-summary.md) [](character-count-summary.md) L'esempio si basa su uno strumento di modifica del database per impostare e aggiornare queste proprietà facoltative.

Ad esempio, per usare MsiInfo per aggiungere le informazioni di riepilogo all'esempio, passare alla directory contenente il database e usare la riga di comando seguente. Non riutilizzare l'ID pacchetto di esempio illustrato di seguito.

**Msiinfo.exe MNP2000.msi -T "Database di installazione" -J Subject -A "Microsoft Corporation" -K "Installer, MSI, Database" -O "Questo database del programma di installazione contiene la logica e i dati necessari per installare Blocco note." -P ;1033 -V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} -G 200 -W 0 -N Orca -U 0**

Per altre informazioni dettagliate sulle informazioni di riepilogo, vedere [Informazioni sul flusso di informazioni](about-the-summary-information-stream.md)di riepilogo , Uso del [flusso](using-the-summary-information-stream.md)di informazioni di riepilogo e Informazioni di riferimento sul flusso di informazioni [di riepilogo](summary-information-stream-reference.md).

Per un elenco completo di tutte le proprietà delle informazioni di riepilogo e delle descrizioni delle proprietà di riepilogo per la relativa descrizione, vedere Summary [Information Stream Property Set (Set](summary-information-stream-property-set.md) di proprietà del flusso di informazioni di riepilogo). [](summary-property-descriptions.md)

[Continua](importing-the-user-interface.md)

 

 




