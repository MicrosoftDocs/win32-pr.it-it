---
description: Con i file INF vengono usate le funzioni dell'API di configurazione seguenti.
ms.assetid: fb4263fc-5f59-460a-a7d9-93f10729c02a
title: Funzioni di impostazione del file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24944f19938217d40ff4a7eaebbfb638c26e4afb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315328"
---
# <a name="inf-file-setup-functions"></a>Funzioni di impostazione del file INF

Con i file INF vengono usate le funzioni dell'API di configurazione seguenti.



| Funzione                                                                         | Descrizione                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)                                   | Libera le risorse e chiude l'handle INF.                                                                                                                                                             |
| [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)                   | Copia un file e, se necessario, lo decomprime.                                                                                                                                                      |
| [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                                 | Trova la prima riga in una sezione di un file INF o, se viene specificata una chiave, la prima riga che corrisponde a tale chiave. Aggiorna il membro della **riga** di una struttura [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) . |
| [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                                   | Restituisce la riga successiva in una sezione relativa al membro della **riga** della struttura [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) specificata.                                                                    |
| [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                         | Restituisce la riga successiva in una sezione relativa al membro della **riga** dell'oggetto [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) specificato che corrisponde a una chiave specificata.                                                 |
| [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                               | Recupera i dati da una riga i cui campi sono in formato binario.                                                                                                                                          |
| [**SetupGetFieldCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)                                 | Restituisce il numero di campi in una riga.                                                                                                                                                                |
| [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)               | Recupera le informazioni di compressione dei file da un file INF.                                                                                                                                               |
| [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)                               | Ottiene un elenco dei tipi di file INF in una directory specificata.                                                                                                                                        |
| [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                         | Restituisce informazioni su un file INF (in base al membro della **riga** di un [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) o fileName).                                                                                     |
| [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                     | Restituisce il campo integer specificato di una riga in un file INF.                                                                                                                                          |
| [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                               | Aggiorna il membro della **riga** di un [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) per la riga in corrispondenza di un indice specificato nella sezione specificata.                                                                     |
| [**SetupGetLineCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)                                   | Restituisce il numero di righe nella sezione specificata.                                                                                                                                                  |
| [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                     | Recupera il contenuto di una riga specificata da un file INF.                                                                                                                                            |
| [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                             | Restituisce un elenco di stringhe, a partire dal campo specificato di una riga in un file INF.                                                                                                                   |
| [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)                 | Ottiene l'ordinale del disco di origine e il percorso (relativo alla radice di origine) in cui si trova il file di origine                                                                                                       |
| [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                         | Ottiene le dimensioni del file per un singolo file di origine o una sezione di **copia** dei file di un file inf.                                                                                                           |
| [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                                 | Recupera il percorso, il file di tag o la descrizione di un'origine.                                                                                                                                             |
| [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                               | Restituisce il campo stringa specificato di una riga in un file INF.                                                                                                                                           |
| [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                                 | Ottiene il percorso di destinazione per una sezione di **copia dei file** in un file inf.                                                                                                                                      |
| [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)                                     | Installa un file.                                                                                                                                                                                       |
| [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)                                 | Installa un file e restituisce una variabile che indica se il file è in uso o meno.                                                                                                                  |
| [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)       | Accoda tutti i file specificati nelle sezioni **copiare** i file, **eliminare file** e **rinominare i file** elencati da una sezione di **installazione** .                                                       |
| [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)                 | Esegue le direttive specificate in una sezione di **installazione** del file inf.                                                                                                                                  |
| [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) | Esegue le operazioni di installazione ed eliminazione del servizio come specificato in una sezione del **servizio** di un file inf.                                                                                            |
| [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)                         | Apre un file INF e lo accoda a un handle INF esistente.                                                                                                                                             |
| [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)                                     | Apre un file INF e restituisce un handle.                                                                                                                                                          |
| [**SetupOpenMasterInf**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)                                 | Apre il file INF contenente le informazioni sul file e sul layout per i file forniti con il sistema.                                                                                                        |
| [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)             | Esegue una query su una struttura di informazioni INF sui nomi file INF associati.                                                                                                                               |
| [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)       | Esegue una query su una struttura di informazioni INF per ottenere informazioni sulla versione in uno dei relativi file INF costitutivi.                                                                                                      |
| [**SetupSetDirectoryId**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)                               | Associa un nuovo identificatore di directory a una directory specifica.                                                                                                                                     |



 

 

 



