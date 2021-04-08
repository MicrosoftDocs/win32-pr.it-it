---
title: Schema (funzionalità legacy dell'ambiente Windows)
description: Nello schema vengono documentati i valori e le proprietà utilizzati dall'indice per archiviare i dati per l'indicizzazione o l'ordinamento.
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a122959b007ba4d4434e65b53fc2e330857cafe
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "104046415"
---
# <a name="schema"></a>SCHEMA

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

Nello schema vengono documentati i valori e le proprietà utilizzati dall'indice per archiviare i dati per l'indicizzazione o l'ordinamento. Nella tabella dello schema sono elencate le colonne e le relative proprietà (Type e propid) incluse nello schema per Microsoft Windows Desktop Search (WDS) 2.6.5.

## <a name="schema"></a>SCHEMA



| Nome colonna                  | Descrizione                                                                                                             | Propid                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | Commenti                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| Crea                       | Data e ora di creazione del file                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | Cartella intuitiva per l'elemento                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | Autore del documento                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| DocCategory                  | Category                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| DocKeywords                  | Parole chiave                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| DocTitlePrefix               | Prefisso dell'oggetto (Re:, FW: e così via)                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DocTitlePrefix               |
| DocTitle                     | Titolo                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| FileExtDesc                  | Descrizione intuitiva del tipo di file dal registro di sistema (ad esempio:. PSQ--> file di query di Product Studio)                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExtDesc                  |
| FolderName                   | Nome della cartella padre                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FolderName                   |
| Associazione                 | Indica che l'elemento è un allegato                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/alconnessione                 |
| IsDeleted                    | Indica che l'elemento è contrassegnato per l'eliminazione (Cestino, elementi eliminati e così via)                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/eliminato                    |
| LastViewed                   | Data dell'ultima visualizzazione dell'elemento da parte dell'utente                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastViewed                   |
| Persone                       | Utenti interessati a questo elemento                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/persone                       |
| PerceivedType                | PerceivedType dell'oggetto Nota: questa operazione è solo per il recupero.                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType                |
| PerceivedTypeName            | Nome visualizzato di PerceivedType.Mai visualizzato o sottoposto a query                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedTypeName            |
| DataPrincipale                  | Data più interessante (ora dell'ultima scrittura per i file, data di ricezione per la posta elettronica)                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DataPrincipale                  |
| Dimensione                         | Dimensioni di un file.                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | Oggetto del file. Nota: attualmente gli argomenti di posta elettronica vengono mappati a PrimaryTitle oggi e non vengono duplicati a causa della loro lunghezza | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | URL basato su query                                                                                                         | 49691C90-7E17-101A-A91C-08002B2ECDA9/9                            |
| Scrittura                        | Data e ora dell'ultima scrittura nel file                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | Data di scadenza di un elemento                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| Incomplete                 | Indica che l'elemento non è completamente disponibile                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/incompleto                 |
| IsFlaggedCompleted           | Indica che l'elemento è contrassegnato come completato                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlaggedCompleted           |
| Con flag                    | Indica che l'elemento è contrassegnato                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/contrassegnato                    |
| FlagText                     | Testo visualizzato per il flag, ad esempio revisione, completamento e così via.                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FlagText                     |
| Identità                     | Identità per gli utenti di OE                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/identità                     |
| IsRead                       | Indica che l'elemento è stato letto                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/lettura                       |
| Importanza                   | Importanza o priorità MAPI                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/importanza                   |
| ContainerHash                | Codice hash che identifica gli allegati da eliminare in base a un URL del contenitore comune                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ContainerHash                |
| DocFormat                    | Formato di documento o MIMETYPE (ad esempio, "Message/RFC822" per un file EML)                                              | 0B63E350-9CCC-11D0-BCDB-00805FCCCE04/5                            |
| GatherTimeModified           | Ora dell'ultima ricerca per indicizzazione del documento per l'aggiornamento del catalogo                                                           | 0b63e350-9ccc-11D0-Bcdb-00805fccce04/4                            |
| Archivio                        | Gestore di archivio o di protocollo (FILE, posta elettronica, OUTLOOKEXPRESS)                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/archivio                        |
| FileExt                      | Estensione file                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExt                      |
| FileName                     | Nome del file                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| ShortName                    | Breve (8,3) nome file per il file                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| AttachmentNames              | Nomi degli allegati in un messaggio                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AttachmentNames              |
| BccAddress                   | Indirizzi nel campo Ccn:                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccAddress                   |
| BccName                      | Nomi di persona in Ccn: Field                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccName                      |
| CcAddress                    | Indirizzi in CC: Field                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcAddress                    |
| CcName                       | Nomi di persona in CC: Field                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcName                       |
| Conversation.ID               | ID univoco per una conversazione nei thread di posta elettronica                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Conversation.ID               |
| FromAddress                  | Indirizzi nel campo da:                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | Nome persona in da: campo                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| FwdRply                      | Indica che il messaggio è stato risposto o inviato ( \_ azione cdoPR = 261 262)                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FwdRply                      |
| HasAttach                    | Indica che la posta è associata a un allegato (T o F)                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HasAttach                    |
| ReceivedDate                 | Tempo di recapito                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ReceivedDate                 |
| ToAddress                    | Indirizzi nel campo a:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/toaddress                    |
| Nome                       | Nomi di persona nel campo a:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/toName                       |
| TaskStatus                   | Stato di un'attività                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TaskStatus                   |
| EndDate                      | Ora di fine (in genere per riunioni/eventi)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EndDate                      |
| IsRecurring                  | Indica che l'elemento è ricorrente (ad esempio, riunioni)                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRecurring                  |
| StartDate                    | Ora di inizio (in genere per riunioni/eventi)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/StartDate                    |
| Duration                     | Lunghezza della riunione in minuti                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/durata                     |
| Location                     | Posizione in cui si verifica l'elemento (ad esempio una riunione)                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/località                     |
| Dell'anniversario                  | Data anniversario                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/anniversario                  |
| AssistantName                | Nome assistente                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| AssistantTelephone           | Telefono assistente                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantTelephone           |
| Data di nascita                     | Compleanno del contatto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/birthday                     |
| BusinessAddressCity          | Informazioni indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| BusinessAddressPostalCode    | Informazioni indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostalCode    |
| BusinessAddressPostOfficeBox | Informazioni indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostOfficeBox |
| BusinessAddressState         | Informazioni indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| BusinessAddressStreet        | Informazioni indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressStreet        |
| BusinessAddressCountry       | Informazioni indirizzo aziendale                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| CallbackTelephone            | Chiama le informazioni sul telefono                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CallbackTelephone            |
| CarTelephone                 | Informazioni sul telefono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CarTelephone                 |
| Children                     | Nomi degli elementi figlio per il contatto                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/figli                     |
| CompanyMainTelephone         | Informazioni sul telefono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CompanyMainTelephone         |
| EmailAddress                 | Nome e-mail contatto                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| EmailName                    | Nome visualizzato per l'indirizzo di posta elettronica                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailName                    |
| FirstName                    | Nome del contatto                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | Nome completo del contatto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| Sesso                       | Maschio/femmina/altro                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Gender                       |
| Hobby                        | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Hobby                        |
| HomeAddressCity              | Informazioni indirizzo Home                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | Informazioni indirizzo Home                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| HomeAddressPostalCode        | Informazioni indirizzo Home                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressPostalCode        |
| HomeAddressState             | Informazioni indirizzo Home                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressStreet            | Informazioni indirizzo Home                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressStreet            |
| HomeFaxNumber                | Informazioni facsimile                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeFaxNumber                |
| BusinessFaxNumber            | Informazioni facsimile                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessFaxNumber            |
| HomeTelephone                | Informazioni sul telefono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeTelephone                |
| Imindirizzo                    | Informazioni sul messaggio istantaneo                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/imindirizzo                    |
| JobTitle                     | Titolo del processo del contatto                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| MobileTelephone              | Informazioni sul telefono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MobileTelephone              |
| NickName                     | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/soprannome                     |
| Office                       | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Office                       |
| OfficeTelephone              | Informazioni sul telefono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/OfficeTelephone              |
| PagerTelephone               | Informazioni sul telefono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| LastName                     | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastName                     |
| PersonalTitle                | Titolo della professione (Dr., Sig., Mrs., MS)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PersonalTitle                |
| PrimaryTelephone             | Informazioni sul telefono                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryTelephone             |
| Profession                   | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/professione                   |
| Coniuge                       | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/sposo                       |
| Suffisso                       | Informazioni di contatto                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/suffisso                       |
| TelexNumber                  | Informazioni telex                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TelexNumber                  |
| TTYTDDTelephone              | Informazioni su TTY/TDD                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TTYTDDTelephone              |
| WebPage                      | Pagina Web di contatto                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/pagina Web                      |
| DocCompany                   | Company                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | Utente che ha salvato l'ultimo documento WA                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DocLastPrinted               | Ultima stampa                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Manager                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| DocPresentationFormat        | DestinazionePresentazione                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| DocSlideCount                | Diapositive                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| AudioAvgDataRate             | Velocità media dei dati in kbps per il file audio                                                                            | 64440490-4C8B-11D1-8B70-080036B11A03/4                            |
| AudioTimeLength              | Lunghezza in millisecondi del file audio                                                                                | 56A3372E-CE9C-11D2-9F0E-006097C686F6/8                            |
| MusicAlbum                   | Nome album                                                                                                              | 56A3372E-CE9C-11D2-9F0E-006097C686F6/4                            |
| MusicArtist                  | Nome dell'artista                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/2                            |
| MusicGenre                   | Genere dell'album                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/11                           |
| MusicTrack                   | Numero di tracce nell'album                                                                                           | 56A3372E-CE9C-11D2-9F0E-006097C686F6/7                            |
| MusicYear                    | Anno in cui è stato registrato l'album                                                                                    | 56A3372E-CE9C-11D2-9F0E-006097C686F6/5                            |
| ExifCameraMake               | Produttore della fotocamera                                                                                                  | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/271                          |
| ExifCameraModel              | Modello di fotocamera                                                                                                         | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/272                          |
| DateTaken                    | FILETIME di dati presi                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| ExifOrientation              | Orientamento                                                                                                             | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/274                          |
| ImageDimensions              | Dimensioni dell'immagine                                                                                                 | 6444048F-4C8B-11D1-8B70-080036B11A03/13                           |
| ImageResX                    | Risoluzione X per l'immagine                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/5                            |
| ImageResY                    | Risoluzione Y per l'immagine                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameHeight             | Altezza del frame per il flusso video                                                                                       | 64440491-4C8B-11D1-8B70-080036B11A03/4                            |
| VideoFrameRate               | Frequenza dei fotogrammi in frame per millisecondi per il flusso video                                                               | 64440491-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameWidth              | Larghezza del frame per il flusso video                                                                                        | 64440491-4C8B-11D1-8B70-080036B11A03/3                            |
| Classe                        | Nome di classe                                                                                                              | 8dee0300-16C2-101B-B121-08002b2ecda9/classe                        |
| Funzione                     | Nome della funzione                                                                                                           | 8dee0300-16C2-101B-B121-08002b2ecda9/Func                         |
| Struct                       | Nome struttura                                                                                                          | 8dee0300-16C2-101B-B121-08002b2ecda9/struct                       |
| Interfaccia                    | Nome interfaccia                                                                                                          | 8dee0300-16C2-101B-B121-08002b2ecda9/interfaccia                    |
| Delegato                     | Nome delegato                                                                                                           | 8dee0300-16C2-101B-B121-08002b2ecda9/delegato                     |
| Proprietà                     | Nome proprietà                                                                                                           | 8dee0300-16C2-101B-B121-08002b2ecda9/proprietà                     |
| Enumerazione                         | Nome enum                                                                                                               | 8dee0300-16C2-101B-B121-08002b2ecda9/enum                         |
| Costante                        | Nome const                                                                                                              | 8dee0300-16C2-101B-B121-08002b2ecda9/const                        |
| Evento                        | Nome evento                                                                                                              | 8dee0300-16C2-101B-B121-08002b2ecda9/evento                        |
| Campo                        | Nome del campo                                                                                                              | 8dee0300-16C2-101B-B121-08002b2ecda9/campo                        |
| Definire                       | Definisci nome                                                                                                             | 8dee0300-16C2-101B-B121-08002b2ecda9/def                          |
| Componente                    | Nome componente                                                                                                          | 8dee0300-16C2-101B-B121-08002b2ecda9/componente                    |
| Project                      | Project name (Nome progetto)                                                                                                            | 8dee0300-16C2-101B-B121-08002b2ecda9/progetto                      |
| Soluzione                     | Nome soluzione                                                                                                           | 8dee0300-16C2-101B-B121-08002b2ecda9/soluzione                     |



 

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

 

 




