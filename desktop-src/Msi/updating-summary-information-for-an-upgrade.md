---
description: Il codice del pacchetto di aggiornamento deve essere modificato rispetto a quello del prodotto originale.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Aggiornamento delle informazioni di riepilogo per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6849a315f5251538acc749d3c3a2ed5605d82ec4159fadf584b5a087a9beaeee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141597"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Aggiornamento delle informazioni di riepilogo per un aggiornamento

Il codice del pacchetto di aggiornamento deve essere modificato rispetto a quello del prodotto originale. Il codice del pacchetto viene archiviato nella [**proprietà Riepilogo numero revisione.**](revision-number-summary.md) Per informazioni dettagliate, vedere [Codici pacchetto](package-codes.md). Usare Msiinfo.exe o un altro editor per modificare le informazioni di riepilogo MNP2001.msi come descritto in [Aggiunta di informazioni di riepilogo](adding-summary-information.md).



| Proprietà Delle informazioni di riepilogo                                                   | Dati                                                                             | Note                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modello**](template-summary.md)(piattaforma e linguaggio)<br/>         | ;1033                                                                            | Piattaforma e linguaggio usati dal database. Se la specifica della piattaforma non è presente nel [**valore della proprietà Riepilogo**](template-summary.md) modello, il programma di installazione presuppone l'architettura Intel. La [**proprietà ProductLanguage**](productlanguage.md) del database viene in genere usata per questa proprietà di riepilogo. L'ID lingua dell'esempio indica che il pacchetto usa l'inglese degli Stati Uniti. |
| [**Numero di revisione**](revision-number-summary.md)(codice pacchetto)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | Si tratta del GUID del codice [del pacchetto](guid.md) che identifica in modo univoco il pacchetto di esempio. Se si riproduce questo esempio, usare un'utilità come GUIDGEN per generare un GUID diverso per il pacchetto. I risultati di GUIDGEN contengono caratteri minuscoli, si noti che è necessario modificare tutti i caratteri minuscoli in lettere maiuscole per un codice di pacchetto valido.                                                     |
| [**Numero di pagine**](page-count-summary.md)(versione minima del programma di installazione)<br/> | 200                                                                              | Per un minimo Windows Installer versione 2.0, questa proprietà deve essere impostata sul numero intero 200.                                                                                                                                                                                                                                                                                                         |
| [**Conteggio parole**](word-count-summary.md)(tipo di origine)<br/>            | 0                                                                                | Il tipo di origine globale per il pacchetto è nomi di file lunghi e non compressi. Per altre informazioni, vedere [Origini compresse](compressed-and-uncompressed-sources.md) e non compresse e la descrizione della colonna Attributi della [tabella File](file-table.md).                                                                                                                               |
| [**Titolo**](title-summary.md)                                                 | Database di installazione                                                            | Informa gli utenti che questo database è per un'installazione anziché per una trasformazione o una patch.                                                                                                                                                                                                                                                                                                          |
| [**Oggetto**](subject-summary.md)                                             | MNP2001                                                                          | I browser di file possono visualizzarlo come prodotto da installare con questo database.                                                                                                                                                                                                                                                                                                                    |
| [**Parole chiavi**](keywords-summary.md)                                           | Programma di installazione, MSI, database                                                         | I browser di file in grado di eseguire la ricerca di parole chiave possono cercare queste parole.                                                                                                                                                                                                                                                                                                                      |
| [**Autore**](author-summary.md)                                               | Microsoft Corporation                                                            | Nome del produttore del prodotto.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Commenti**](comments-summary.md)                                           | Questo database del programma di installazione contiene la logica e i dati necessari per installare Blocco note. | Informa gli utenti sullo scopo di questo database.                                                                                                                                                                                                                                                                                                                                                    |
| [**Creazione di un'applicazione**](creating-application-summary.md)                   | Orca                                                                             | Applicazione utilizzata per creare il database di installazione. L'esempio specifica l'editor di database Orca come esempio.                                                                                                                                                                                                                                                                                   |
| [**Sicurezza**](security-summary.md)                                           | 0                                                                                | Il database di esempio è di lettura/scrittura senza restrizioni.                                                                                                                                                                                                                                                                                                                                                      |



 

[Continua](validating-an-installation-upgrade.md)

 

 




