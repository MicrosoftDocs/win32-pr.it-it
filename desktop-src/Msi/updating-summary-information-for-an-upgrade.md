---
description: Il codice del pacchetto di aggiornamento deve essere modificato rispetto a quello del prodotto originale.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Aggiornamento delle informazioni di riepilogo per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9bee3457b9ebbe0264d569f37d8ed5a3e372df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058229"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Aggiornamento delle informazioni di riepilogo per un aggiornamento

Il codice del pacchetto di aggiornamento deve essere modificato rispetto a quello del prodotto originale. Il codice del pacchetto viene archiviato nella proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) . Per informazioni dettagliate, vedere [codici di pacchetto](package-codes.md). Usare Msiinfo.exe o un altro editor per modificare le informazioni di riepilogo di MNP2001.msi come descritto in [aggiunta di informazioni di riepilogo](adding-summary-information.md).



| Proprietà informazioni di riepilogo                                                   | Data                                                                             | Note                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modello**](template-summary.md)(piattaforma e linguaggio)<br/>         | ; 1033                                                                            | Piattaforma e linguaggio utilizzati dal database. Se la specifica della piattaforma non è presente nel valore della proprietà di riepilogo del [**modello**](template-summary.md) , il programma di installazione presuppone l'architettura Intel. La proprietà [**ProductLanguage**](productlanguage.md) del database viene in genere utilizzata per questa proprietà di riepilogo. L'ID di lingua dell'esempio indica che il pacchetto utilizza l'inglese (Stati Uniti). |
| [**Numero revisione**](revision-number-summary.md)(codice pacchetto)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | [GUID](guid.md) del codice del pacchetto che identifica in modo univoco il pacchetto di esempio. Se si riproduce questo esempio, usare un'utilità, ad esempio GUIDGEN, per generare un GUID diverso per il pacchetto. I risultati di GUIDGEN contengono caratteri minuscoli. si noti che è necessario modificare tutti i caratteri minuscoli in maiuscolo per un codice di pacchetto valido.                                                     |
| [**Conteggio pagine**](page-count-summary.md)(versione minima del programma di installazione)<br/> | 200                                                                              | Per almeno Windows Installer versione 2,0, questa proprietà deve essere impostata sul valore integer 200.                                                                                                                                                                                                                                                                                                         |
| [**Conteggio parole**](word-count-summary.md)(tipo di origine)<br/>            | 0                                                                                | Il tipo di origine globale per il pacchetto è un nome di file lungo e non compresso. Per ulteriori informazioni, vedere [origini compresse e non compresse](compressed-and-uncompressed-sources.md) e la descrizione della colonna attributi della [tabella file](file-table.md).                                                                                                                               |
| [**Titolo**](title-summary.md)                                                 | Database di installazione                                                            | Informa gli utenti che il database è per un'installazione anziché una trasformazione o una patch.                                                                                                                                                                                                                                                                                                          |
| [**Oggetto**](subject-summary.md)                                             | MNP2001                                                                          | I browser file possono visualizzarlo come prodotto da installare con il database.                                                                                                                                                                                                                                                                                                                    |
| [**Parole chiave**](keywords-summary.md)                                           | Programma di installazione, MSI, database                                                         | I browser di file in grado di eseguire ricerche di parole chiave possono cercare queste parole.                                                                                                                                                                                                                                                                                                                      |
| [**Autore**](author-summary.md)                                               | Microsoft Corporation                                                            | Nome del produttore del prodotto.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Commenti**](comments-summary.md)                                           | Questo database del programma di installazione contiene la logica e i dati necessari per installare il blocco note. | Informa gli utenti sullo scopo di questo database.                                                                                                                                                                                                                                                                                                                                                    |
| [**Creazione dell'applicazione**](creating-application-summary.md)                   | Orca                                                                             | Applicazione utilizzata per creare il database di installazione. Nell'esempio viene specificato come esempio l'editor di database Orca.                                                                                                                                                                                                                                                                                   |
| [**Sicurezza**](security-summary.md)                                           | 0                                                                                | Il database di esempio è di lettura/scrittura senza restrizioni.                                                                                                                                                                                                                                                                                                                                                      |



 

[Continua](validating-an-installation-upgrade.md)

 

 




