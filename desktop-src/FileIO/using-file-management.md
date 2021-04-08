---
description: Negli esempi seguenti vengono utilizzate le funzioni di gestione file.
ms.assetid: 0879898b-b661-48b3-af94-9ba24811503f
title: Uso della gestione dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88838ee99dde16c5c2288c00e2e2f3b35747dae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058116"
---
# <a name="using-file-management"></a><span data-ttu-id="581e7-103">Uso della gestione dei file</span><span class="sxs-lookup"><span data-stu-id="581e7-103">Using File Management</span></span>

<span data-ttu-id="581e7-104">Negli esempi seguenti vengono utilizzate le funzioni di gestione file.</span><span class="sxs-lookup"><span data-stu-id="581e7-104">The following samples use the file management functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="581e7-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="581e7-105">In this section</span></span>



| <span data-ttu-id="581e7-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="581e7-106">Topic</span></span>                                                                                                   | <span data-ttu-id="581e7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="581e7-107">Description</span></span>                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="581e7-108">Aggiunta di utenti a un file crittografato</span><span class="sxs-lookup"><span data-stu-id="581e7-108">Adding Users to an Encrypted File</span></span>](adding-users-to-an-encrypted-file.md)<br/>                   | <span data-ttu-id="581e7-109">Codice di esempio che illustra come aggiungere un nuovo utente a un file crittografato esistente tramite la funzione [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) .</span><span class="sxs-lookup"><span data-stu-id="581e7-109">Example code that shows how to add a new user to an existing encrypted file by using the [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) function.</span></span><br/>                         |
| [<span data-ttu-id="581e7-110">Aggiunta di un file a un altro file</span><span class="sxs-lookup"><span data-stu-id="581e7-110">Appending One File to Another File</span></span>](appending-one-file-to-another-file.md)<br/>                 | <span data-ttu-id="581e7-111">Codice di esempio che illustra come un'applicazione può accodare un file alla fine di un altro file, incluse le modalità di apertura e chiusura dei file, di lettura e scrittura nei file e di blocco e sblocco di file.</span><span class="sxs-lookup"><span data-stu-id="581e7-111">Example code that shows how an application can append one file to the end of another file, including how to open and close files, read and write to files, and lock and unlock files.</span></span><br/> |
| [<span data-ttu-id="581e7-112">Creazione e utilizzo di un file temporaneo</span><span class="sxs-lookup"><span data-stu-id="581e7-112">Creating and Using a Temporary File</span></span>](creating-and-using-a-temporary-file.md)<br/>               | <span data-ttu-id="581e7-113">Codice di esempio che illustra come creare un file temporaneo per scopi di manipolazione dei dati tramite le funzioni GetTempFileName e GetTempPath.</span><span class="sxs-lookup"><span data-stu-id="581e7-113">Example code that shows how to create a temporary file for data manipulation purposes by using the GetTempFileName and GetTempPath functions.</span></span><br/>                                         |
| [<span data-ttu-id="581e7-114">Blocco e sblocco degli intervalli di byte nei file</span><span class="sxs-lookup"><span data-stu-id="581e7-114">Locking and Unlocking Byte Ranges in Files</span></span>](locking-and-unlocking-byte-ranges-in-files.md)<br/> | <span data-ttu-id="581e7-115">Codice di esempio che mostra il blocco e lo sblocco di intervalli di byte usando le funzioni LockFileEx e UnlockFileEx.</span><span class="sxs-lookup"><span data-stu-id="581e7-115">Example code that shows byte range locking and unlocking by using the LockFileEx and UnlockFileEx functions.</span></span><br/>                                                                          |
| [<span data-ttu-id="581e7-116">Apertura di un file per la lettura o la scrittura</span><span class="sxs-lookup"><span data-stu-id="581e7-116">Opening a File for Reading or Writing</span></span>](opening-a-file-for-reading-or-writing.md)<br/>           | <span data-ttu-id="581e7-117">Codice di esempio che illustra come utilizzare la funzione CreateFile per creare un nuovo file o aprire un file esistente.</span><span class="sxs-lookup"><span data-stu-id="581e7-117">Example code that shows how to use the CreateFile function to create a new file or open an existing file.</span></span><br/>                                                                             |
| [<span data-ttu-id="581e7-118">Recupero e modifica degli attributi di file</span><span class="sxs-lookup"><span data-stu-id="581e7-118">Retrieving and Changing File Attributes</span></span>](retrieving-and-changing-file-attributes.md)<br/>       | <span data-ttu-id="581e7-119">Codice di esempio che illustra come usare la funzione GetFileAttributesEx per recuperare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="581e7-119">Example code that shows how to use the GetFileAttributesEx function to retrieve file attributes.</span></span><br/>                                                                                      |
| [<span data-ttu-id="581e7-120">Test per la fine di un file</span><span class="sxs-lookup"><span data-stu-id="581e7-120">Testing for the End of a File</span></span>](testing-for-the-end-of-a-file.md)<br/>                           | <span data-ttu-id="581e7-121">Codice di esempio che illustra come verificare la fine del file durante un'operazione di lettura sincrona e durante un'operazione di lettura asincrona.</span><span class="sxs-lookup"><span data-stu-id="581e7-121">Example code that shows how to test for the end of file during a synchronous read operation and during an asynchronous read operation.</span></span><br/>                                                |
| [<span data-ttu-id="581e7-122">Uso di flussi</span><span class="sxs-lookup"><span data-stu-id="581e7-122">Using Streams</span></span>](using-streams.md)<br/>                                                           | <span data-ttu-id="581e7-123">Codice di esempio che illustra come usare i flussi di file system NTFS di base.</span><span class="sxs-lookup"><span data-stu-id="581e7-123">Example code that shows how to use basic NTFS file system streams.</span></span><br/>                                                                                                                    |



 

 

 




