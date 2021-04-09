---
description: Il Windows Installer archivia tutte le stringhe di database in un singolo pool di stringhe condivise per ridurre le dimensioni del database e migliorare le prestazioni.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: Convalida String-Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130278"
---
# <a name="string-pool-validation"></a><span data-ttu-id="0ed27-103">Convalida String-Pool</span><span class="sxs-lookup"><span data-stu-id="0ed27-103">String-Pool Validation</span></span>

<span data-ttu-id="0ed27-104">Il Windows Installer archivia tutte le stringhe di database in un singolo pool di stringhe condivise per ridurre le dimensioni del database e migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0ed27-104">The Windows Installer stores all database strings in a single shared string pool to reduce the size of the database and to improve performance.</span></span> <span data-ttu-id="0ed27-105">L'unico mezzo per convalidare il pool di stringhe consiste nell'usare lo strumento MsiInfo disponibile in Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="0ed27-105">The only means of validating the string pool is to use the MsiInfo tool found in the Windows Installer SDK.</span></span>

<span data-ttu-id="0ed27-106">La verifica del pool di stringhe è costituita da due controlli principali:</span><span class="sxs-lookup"><span data-stu-id="0ed27-106">String pool verification consists of two main checks:</span></span>

-   [<span data-ttu-id="0ed27-107">Test di stringhe DBCS</span><span class="sxs-lookup"><span data-stu-id="0ed27-107">DBCS string tests</span></span>](#dbcs-string-tests)
-   [<span data-ttu-id="0ed27-108">Verifica conteggio riferimenti</span><span class="sxs-lookup"><span data-stu-id="0ed27-108">Reference count verification</span></span>](#reference-count-verification)

## <a name="dbcs-string-tests"></a><span data-ttu-id="0ed27-109">Test di stringhe DBCS</span><span class="sxs-lookup"><span data-stu-id="0ed27-109">DBCS String Tests</span></span>

<span data-ttu-id="0ed27-110">I test delle stringhe DBCS analizzano ogni stringa del database per due criteri: per i pacchetti con una tabella codici neutra contrassegnata, se un carattere è un carattere esteso (maggiore di 127), la stringa viene contrassegnata e viene visualizzato un messaggio che indica che la tabella codici del database non è valida perché questi caratteri richiedono che venga eseguito il rendering coerente di una tabella codici in tutti i sistemi</span><span class="sxs-lookup"><span data-stu-id="0ed27-110">The DBCS string tests scan each string in the database for two criteria: For packages with a neutral code page marked, if any character is an extended character (greater than 127), the string is flagged and a message is displayed saying that the code page of the database is invalid because these characters require a specific code page to be rendered consistently on all systems.</span></span>

<span data-ttu-id="0ed27-111">Se il database include una tabella codici, viene eseguita l'analisi di ogni stringa per un indicatore DBCS non valido.</span><span class="sxs-lookup"><span data-stu-id="0ed27-111">If the database has a code page, each string is scanned for an invalid DBCS indicator.</span></span> <span data-ttu-id="0ed27-112">Se una stringa non neutra è stata contrassegnata in modo errato, i caratteri non vengono visualizzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="0ed27-112">If a non-neutral string has been improperly marked, the characters will not render correctly.</span></span> <span data-ttu-id="0ed27-113">Questo problema si verifica in genere forzando la tabella codici su un valore specifico usando il \_ Tabella ForceCodepage con stringhe non neutre già presenti nel database. Si noti che questo controllo richiede che la tabella codici del database sia installata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="0ed27-113">(This is most commonly caused by forcing the code page to a particular value using the \_ForceCodepage table with non-neutral strings already in the database.) Note that this check requires that the code page of the database be installed on the system.</span></span>

<span data-ttu-id="0ed27-114">Se si verifica un problema nella tabella codici, l'utente può correggere l'errore usando la \_ tabella ForceCodepage per forzare il valore appropriato della tabella codici del database.</span><span class="sxs-lookup"><span data-stu-id="0ed27-114">If there is a code page problem, the user may fix the error by using the \_ForceCodepage table to force the code page of the database to the appropriate value.</span></span> <span data-ttu-id="0ed27-115">Per ulteriori informazioni, vedere la pagina relativa alla [gestione della tabella codici](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="0ed27-115">For more information, see [Code Page Handling](code-page-handling-windows-installer-.md).</span></span>

## <a name="reference-count-verification"></a><span data-ttu-id="0ed27-116">Verifica conteggio riferimenti</span><span class="sxs-lookup"><span data-stu-id="0ed27-116">Reference Count Verification</span></span>

<span data-ttu-id="0ed27-117">Per verificare i conteggi dei riferimenti di tutte le stringhe, viene eseguita l'analisi di ogni tabella per i valori stringa, viene mantenuto il conteggio di ogni stringa distinta e il risultato viene confrontato con il conteggio dei riferimenti archiviati nel pool di stringhe del database.</span><span class="sxs-lookup"><span data-stu-id="0ed27-117">To verify the reference counts of all strings, every table is scanned for string values, a count of each distinct string is kept, and the result is compared to the stored reference count in the database string pool.</span></span>

<span data-ttu-id="0ed27-118">Se si verifica un problema di conteggio dei riferimenti di stringa, l'utente deve esportare immediatamente ogni tabella del database usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), creare un nuovo database e importare le tabelle nel nuovo database usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="0ed27-118">If there is a string reference count problem, the user should immediately export each table of the database using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), create a new database, and import the tables into the new database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="0ed27-119">Il nuovo database dispone quindi dello stesso contenuto del vecchio database, ma i conteggi dei riferimenti di stringa sono corretti.</span><span class="sxs-lookup"><span data-stu-id="0ed27-119">The new database then has the same content as the old database, but the string reference counts are correct.</span></span> <span data-ttu-id="0ed27-120">L'aggiunta o l'eliminazione di dati da un database con un pool di stringhe danneggiato può aumentare il danneggiamento del database e la perdita di dati, quindi è importante eseguire rapidamente questi passaggi per evitare ulteriori perdite di dati.</span><span class="sxs-lookup"><span data-stu-id="0ed27-120">Adding or deleting data from a database with a corrupt string pool can increase corruption of the database and loss of data, so taking these steps quickly is important to prevent further data loss.</span></span>

<span data-ttu-id="0ed27-121">Quando si ricompilano i database, ricordarsi di incorporare le archiviazioni e i flussi necessari nel nuovo database (vedere la tabella [ \_ flussi](-streams-table.md) tabella e [ \_ archiviazione](-storages-table.md)) e tenere presente i problemi della tabella codici.</span><span class="sxs-lookup"><span data-stu-id="0ed27-121">When rebuilding databases, remember to embed any necessary storages and streams in the new database (see [\_Streams Table](-streams-table.md) and [\_Storages Table](-storages-table.md)) and be aware of code page issues.</span></span> <span data-ttu-id="0ed27-122">Ricordarsi inoltre di impostare tutte le proprietà del [flusso di informazioni di riepilogo](summary-information-stream.md) necessarie.</span><span class="sxs-lookup"><span data-stu-id="0ed27-122">Also remember to set each of the necessary [Summary Information Stream](summary-information-stream.md) properties.</span></span>

 

 



