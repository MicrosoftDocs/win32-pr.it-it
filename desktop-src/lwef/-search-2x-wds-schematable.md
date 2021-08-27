---
title: Schema (funzionalità dell Windows legacy)
description: Lo schema documenta i valori e le proprietà utilizzati dall'indice per archiviare i dati per l'indicizzazione o l'ordinamento.
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d5c80690914073af1c67e2bd00376974547d30c4dc487c0656d4452d3fe828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753150"
---
# <a name="schema"></a>Schema

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare [invece Windows ricerca.](../search/-search-3x-wds-overview.md)

Lo schema documenta i valori e le proprietà utilizzati dall'indice per archiviare i dati per l'indicizzazione o l'ordinamento. La tabella Schema elenca le colonne e le relative proprietà (tipo e propid) incluse nello schema per Microsoft Windows Desktop Search (WDS) 2.6.5.

## <a name="schema"></a>Schema



| Nome colonna                  | Descrizione                                                                                                             | Propid                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | Commenti                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| Crea                       | Data e ora di creazione del file                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | Cartella descrittiva per l'elemento                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | Autore del documento                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| Categoria DocCategory                  | Category                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| DocKeywords                  | Parole chiave                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| DocTitlePrefix               | Prefisso dell'oggetto (Re:, Fw: e così via)                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DocTitlePrefix               |
| DocTitle                     | Title                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| FileExtDesc                  | Descrizione descrittiva del tipo di file dal Registro di sistema (ad esempio: psq --> file di query di Product Studio)                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExtDesc                  |
| FolderName                   | Nome della cartella padre                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FolderName                   |
| IsAttachment                 | Indica che l'elemento è un allegato                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsAttachment                 |
| IsDeleted                    | Indica che l'elemento è contrassegnato per l'eliminazione (Cestino, elementi eliminati e così via)                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsDeleted                    |
| LastViewed                   | Data dell'ultima visualizzazione dell'elemento da parte dell'utente                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastViewed                   |
| Persone                       | Persone coinvolte in questo elemento                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/People                       |
| PerceivedType                | PerceivedType dell'oggetto NOTA: solo per il recupero.                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType                |
| PerceivedTypeName            | Nome visualizzato di PerceivedType.  Mai visualizzato o sottoposto a query                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedTypeName            |
| PrimaryDate                  | Data più interessante (Ora ultima scrittura per i file, data di ricezione per posta elettronica)                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryDate                  |
| Dimensione                         | Dimensioni di un file.                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | Oggetto del file. NOTA: attualmente, gli oggetti di posta elettronica vengono mappati a PrimaryTitle oggi e non vengono duplicati a causa della loro lunghezza | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | URL basato su query                                                                                                         | 49691C90-7E17-101A-A91C-08002B2ECDA9/9                            |
| Scrittura                        | Data e ora dell'ultima scrittura nel file                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | Data di scadenza di un elemento                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| IsIncomplete                 | Indica che l'elemento non è completamente disponibile                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsIncomplete                 |
| IsFlaggedCompleted           | Indica che l'elemento è contrassegnato come completato                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlaggedCompleted           |
| IsFlagged                    | Indica che l'elemento è contrassegnato                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlagged                    |
| FlagText                     | Testo visualizzato per il flag, ad esempio Revisione, Follow up e così via.                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FlagText                     |
| Identità                     | Identità per gli utenti OE                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Identity                     |
| IsRead                       | Indica che l'elemento è stato letto                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRead                       |
| Importanza                   | Priorità o importanza MAPI                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Importance                   |
| ContainerHash                | Codice hash che identifica gli allegati da eliminare in base a un URL del contenitore comune                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ContainerHash                |
| DocFormat                    | Formato del documento o MIMETYPE (ad esempio 'message/rfc822' per un file EML)                                              | 0B63E350-9CCC-11D0-BCDB-00805FCCCE04/5                            |
| GatherTimeModified           | Ora dell'ultima ricerca per indicizzazione del documento per l'aggiornamento del catalogo                                                           | 0b63e350-9ccc-11d0-bcdb-00805fccce04/4                            |
| Archiviazione                        | Gestore dell'archivio o del protocollo (FILE, MAIL, OUTLOOKEXPRESS)                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Store                        |
| FileExt                      | Estensione file                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExt                      |
| FileName                     | Nome del file                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| ShortName                    | Nome file breve (8.3) per il file                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| AttachmentNames              | Nomi degli allegati in un messaggio                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AttachmentNames              |
| BccAddress                   | Campo Indirizzi in Ccn:                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccAddress                   |
| BccName                      | Nomi di persona in Ccn: campo                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccName                      |
| CcAddress                    | Campo Indirizzi nel campo Cc:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcAddress                    |
| CcName                       | Nomi di persona nel campo Cc:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcName                       |
| ConversationID               | ID univoco per una conversazione nei thread di posta elettronica                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ConversationID               |
| FromAddress                  | Campo Indirizzi nel campo Da:                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | Nome della persona nel campo Da:                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| FwdRply                      | Indica che la posta elettronica è stata inviata o inoltrata (cdoPR \_ ACTION=261 262)                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FwdRply                      |
| HasAttach                    | Indica che la posta elettronica ha un allegato (T o F)                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HasAttach                    |
| ReceivedDate                 | Ora di recapito                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ReceivedDate                 |
| ToAddress                    | Indirizzi nel campo A:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToAddress                    |
| ToName                       | Nomi di persona nel campo A:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ToName                       |
| TaskStatus                   | Stato di un'attività                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TaskStatus                   |
| EndDate                      | Ora di fine (in genere per riunioni/eventi)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EndDate                      |
| IsRecurring                  | Indica che l'elemento è ricorrente (ad esempio, riunioni)                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRecurring                  |
| StartDate                    | Ora di inizio (in genere per riunioni/eventi)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/StartDate                    |
| Durata                     | Durata della riunione in minuti                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Duration                     |
| Località                     | Posizione in cui si verifica l'elemento (ad esempio una riunione)                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Location                     |
| Anniversario                  | Data dell'anniversario                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Anniversary                  |
| AssistantName                | Nome dell'assistente                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| AssistantTelephone           | Telefono assistente                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantTelephone           |
| Data di nascita                     | Compleanni del contatto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Birthday                     |
| BusinessAddressCity          | Informazioni sull'indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| BusinessAddressPostalCode    | Informazioni sull'indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostalCode    |
| BusinessAddressPostOfficeBox | Informazioni sull'indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostOfficeBox |
| BusinessAddressState         | Informazioni sull'indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| BusinessAddressStreet        | Informazioni sull'indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressStreet        |
| BusinessAddressCountry       | Informazioni sull'indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| CallbackTelephone            | Richiamare le informazioni telefoniche                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CallbackTelephone            |
| CarTelephone                 | Informazioni telefoniche                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CarTelephone                 |
| Children                     | Nomi dei figli per il contatto                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Children                     |
| CompanyMainTelephone         | Informazioni telefoniche                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CompanyMainTelephone         |
| EmailAddress                 | Nome del messaggio di posta elettronica del contatto                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| EmailName                    | Nome visualizzato per l'indirizzo di posta elettronica                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailName                    |
| FirstName                    | Nome del contatto                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | Nome completo del contatto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| Sesso                       | Male/female/other                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Gender                       |
| Anta                        | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Ziona                        |
| HomeAddressCity              | Informazioni sull'indirizzo della casa                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | Informazioni sull'indirizzo della casa                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| HomeAddressPostalCode        | Informazioni sull'indirizzo della casa                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressPostalCode        |
| HomeAddressState             | Informazioni sull'indirizzo della casa                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressStreet            | Informazioni sull'indirizzo della casa                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressStreet            |
| HomeFaxNumber                | Informazioni facsimile                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeFaxNumber                |
| BusinessFaxNumber            | Informazioni facsimile                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessFaxNumber            |
| HomeTelephone                | Informazioni telefoniche                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeTelephone                |
| IMAddress                    | Informazioni sui messaggi immediati                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IMAddress                    |
| JobTitle                     | Posizione del contatto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| MobileTelephone              | Informazioni telefoniche                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MobileTelephone              |
| NickName                     | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Name                     |
| Office                       | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Office                       |
| OfficeTelephone              | Informazioni telefoniche                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/OfficeTelephone              |
| PagerTelephone               | Informazioni telefoniche                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| LastName                     | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastName                     |
| PersonalTitle                | Titolo del titolo (Dr., Mr., Mrs., Ms.)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PersonalTitle                |
| PrimaryTelephone             | Informazioni telefoniche                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryTelephone             |
| Profession                   | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Ziona                   |
| Coniuge                       | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/consorte                       |
| Suffisso                       | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Suffix                       |
| TelexNumber                  | Informazioni telex                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TelexNumber                  |
| TTYTDDTelephone              | Informazioni TTY/TDD                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TTYTDDTelephone              |
| WebPage                      | Pagina Web di contatto                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/WebPage                      |
| DocCompany                   | Company                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | Utente dell'ultimo documento salvato da                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DocLastPrinted               | Ultima stampa                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Manager                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| DocPresentationFormat        | PresentationTarget                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| DocSlideCount                | Diapositive                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| AudioAvgDataRate             | Velocità media dei dati in Kbps per il file audio                                                                            | 64440490-4C8B-11D1-8B70-080036B11A03/4                            |
| AudioTimeLength              | Lunghezza in millisecondi del file audio                                                                                | 56A3372E-CE9C-11D2-9F0E-006097C686F6/8                            |
| MusicAlbum                   | Nome dell'album                                                                                                              | 56A3372E-CE9C-11D2-9F0E-006097C686F6/4                            |
| MusicArtist                  | Nome dell'artista                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/2                            |
| MusicGenre                   | Genere dell'album                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/11                           |
| MusicTrack                   | Numero di tracce nell'album                                                                                           | 56A3372E-CE9C-11D2-9F0E-006097C686F6/7                            |
| MusicYear                    | Anno in cui è stato registrato l'album                                                                                    | 56A3372E-CE9C-11D2-9F0E-006097C686F6/5                            |
| ExifCameraMake               | Produttore della fotocamera                                                                                                  | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/271                          |
| ExifCameraModel              | Modello di fotocamera                                                                                                         | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/272                          |
| DateTaken                    | FILETIME dei dati presi                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| ExifOrientation              | Orientamento                                                                                                             | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/274                          |
| ImageDimensions              | Dimensioni dell'immagine                                                                                                 | 6444048F-4C8B-11D1-8B70-080036B11A03/13                           |
| ImageResX                    | Risoluzione X per l'immagine                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/5                            |
| ImageResY                    | Risoluzione Y per l'immagine                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameHeight             | Altezza dei fotogrammi per il flusso video                                                                                       | 64440491-4C8B-11D1-8B70-080036B11A03/4                            |
| VideoFrameRate               | Frequenza fotogrammi in fotogrammi per millisecondo per il flusso video                                                               | 64440491-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameWidth              | Larghezza dei fotogrammi per il flusso video                                                                                        | 64440491-4C8B-11D1-8B70-080036B11A03/3                            |
| Classe                        | Nome di classe                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/class                        |
| Funzione                     | Nome della funzione                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/func                         |
| Struct                       | Nome struttura                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/struct                       |
| Interfaccia                    | Nome dell'interfaccia                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/interface                    |
| Delegato                     | Nome delegato                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/delegate                     |
| Proprietà                     | Nome proprietà                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/property                     |
| Enumerazione                         | Nome enumerazione                                                                                                               | 8dee0300-16c2-101b-b121-08002b2ecda9/enum                         |
| Costante                        | Nome const                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/const                        |
| Evento                        | Nome evento                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/event                        |
| Campo                        | Nome del campo                                                                                                              | 8dee0300-16c2-101b-b121-08002b2ecda9/field                        |
| Definire                       | Definire il nome                                                                                                             | 8dee0300-16c2-101b-b121-08002b2ecda9/def                          |
| Componente                    | Nome componente                                                                                                          | 8dee0300-16c2-101b-b121-08002b2ecda9/component                    |
| Project                      | Project name (Nome progetto)                                                                                                            | 8dee0300-16c2-101b-b121-08002b2ecda9/project                      |
| Soluzione                     | Nome soluzione                                                                                                           | 8dee0300-16c2-101b-b121-08002b2ecda9/solution                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Sviluppo di componenti aggiuntivi IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-2x-wds-phaddins.md)
</dt> <dt>

[Sintassi di ricerca avanzata](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipi percepiti](-search-2x-wds-perceivedtype.md)
</dt> </dl>

 

 




