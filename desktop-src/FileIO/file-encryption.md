---
description: Il file system crittografato (EFS) fornisce la protezione crittografica dei singoli file nei volumi file system NTFS usando un sistema a chiave pubblica.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Crittografia file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317795"
---
# <a name="file-encryption"></a><span data-ttu-id="d6e70-103">Crittografia file</span><span class="sxs-lookup"><span data-stu-id="d6e70-103">File Encryption</span></span>

<span data-ttu-id="d6e70-104">Il file system crittografato, o EFS, fornisce un livello aggiuntivo di sicurezza per i file e le directory.</span><span class="sxs-lookup"><span data-stu-id="d6e70-104">The Encrypted File System, or EFS, provides an additional level of security for files and directories.</span></span> <span data-ttu-id="d6e70-105">Fornisce la protezione crittografica dei singoli file in NTFS file system volumi utilizzando un sistema a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="d6e70-105">It provides cryptographic protection of individual files on NTFS file system volumes using a public-key system.</span></span>

<span data-ttu-id="d6e70-106">In genere, il controllo di accesso agli oggetti file e directory fornito dal modello di sicurezza di Windows è sufficiente per proteggere l'accesso non autorizzato alle informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="d6e70-106">Typically, the access control to file and directory objects provided by the Windows security model is sufficient to protect unauthorized access to sensitive information.</span></span> <span data-ttu-id="d6e70-107">Tuttavia, se un portatile che contiene dati sensibili viene smarrito o rubato, la protezione dei dati potrebbe essere compromessa.</span><span class="sxs-lookup"><span data-stu-id="d6e70-107">However, if a laptop that contains sensitive data is lost or stolen, the security protection of that data may be compromised.</span></span> <span data-ttu-id="d6e70-108">La crittografia dei file aumenta la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d6e70-108">Encrypting the files increases security.</span></span>

<span data-ttu-id="d6e70-109">Per determinare se un file system supporta la crittografia dei file per i file e le directory, chiamare la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il flag di bit di **\_ \_ crittografia del file FS** .</span><span class="sxs-lookup"><span data-stu-id="d6e70-109">To determine whether a file system supports file encryption for files and directories, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FS\_FILE\_ENCRYPTION** bit flag.</span></span> <span data-ttu-id="d6e70-110">Si noti che non è possibile crittografare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6e70-110">Note that the following items cannot be encrypted:</span></span>

-   <span data-ttu-id="d6e70-111">File compressi</span><span class="sxs-lookup"><span data-stu-id="d6e70-111">Compressed files</span></span>
-   <span data-ttu-id="d6e70-112">File di sistema</span><span class="sxs-lookup"><span data-stu-id="d6e70-112">System files</span></span>
-   <span data-ttu-id="d6e70-113">Directory di sistema</span><span class="sxs-lookup"><span data-stu-id="d6e70-113">System directories</span></span>
-   <span data-ttu-id="d6e70-114">Directory radice</span><span class="sxs-lookup"><span data-stu-id="d6e70-114">Root directories</span></span>
-   <span data-ttu-id="d6e70-115">Transazioni</span><span class="sxs-lookup"><span data-stu-id="d6e70-115">Transactions</span></span>

<span data-ttu-id="d6e70-116">I file sparse possono essere crittografati.</span><span class="sxs-lookup"><span data-stu-id="d6e70-116">Sparse files can be encrypted.</span></span>

<span data-ttu-id="d6e70-117">TxF non supporta la maggior parte delle operazioni sui file EFS (Encrypted File System).</span><span class="sxs-lookup"><span data-stu-id="d6e70-117">TxF does not support most operations on Encrypted File System (EFS) files.</span></span> <span data-ttu-id="d6e70-118">Le uniche operazioni supportate da TxF sono operazioni di lettura, ad esempio [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span><span class="sxs-lookup"><span data-stu-id="d6e70-118">The only operations TxF supports are read operations, such as [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d6e70-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d6e70-119">In this section</span></span>



| <span data-ttu-id="d6e70-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="d6e70-120">Topic</span></span>                                                                                               | <span data-ttu-id="d6e70-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6e70-121">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6e70-122">Gestione di file e directory crittografati</span><span class="sxs-lookup"><span data-stu-id="d6e70-122">Handling Encrypted Files and Directories</span></span>](handling-encrypted-files-and-directories.md)<br/> | <span data-ttu-id="d6e70-123">Un file contrassegnato come crittografato viene crittografato dall'file system NTFS usando il driver di crittografia corrente.</span><span class="sxs-lookup"><span data-stu-id="d6e70-123">A file marked encrypted is encrypted by the NTFS file system by using the current encryption driver.</span></span><br/>                                                          |
| [<span data-ttu-id="d6e70-124">Chiavi utente e file crittografati</span><span class="sxs-lookup"><span data-stu-id="d6e70-124">Encrypted Files and User Keys</span></span>](encrypted-files-and-user-keys.md)<br/>                       | <span data-ttu-id="d6e70-125">Elenca le funzioni da usare per creare una nuova chiave, aggiungere una chiave a un file crittografato, eseguire una query sulle chiavi per un file crittografato e rimuovere le chiavi da un file crittografato.</span><span class="sxs-lookup"><span data-stu-id="d6e70-125">Lists the functions to use to create a new key, add a key to an encrypted file, query the keys for an encrypted file, and remove keys from an encrypted file.</span></span><br/> |
| [<span data-ttu-id="d6e70-126">Backup e ripristino di file crittografati</span><span class="sxs-lookup"><span data-stu-id="d6e70-126">Backup and Restore of Encrypted Files</span></span>](backup-and-restore-of-encrypted-files.md)<br/>       | <span data-ttu-id="d6e70-127">Le funzioni di crittografia RAW consentono di eseguire il backup dei file crittografati.</span><span class="sxs-lookup"><span data-stu-id="d6e70-127">The raw encryption functions enable backup of encrypted files.</span></span><br/>                                                                                                |



 

<span data-ttu-id="d6e70-128">Per ulteriori informazioni sulla crittografia, vedere [aggiunta di utenti a un file crittografato](adding-users-to-an-encrypted-file.md).</span><span class="sxs-lookup"><span data-stu-id="d6e70-128">For more information about encryption, see [Adding Users to an Encrypted File](adding-users-to-an-encrypted-file.md).</span></span>

<span data-ttu-id="d6e70-129">Per ulteriori informazioni sulla crittografia, vedere [crittografia](/windows/desktop/SecCrypto/cryptography-portal).</span><span class="sxs-lookup"><span data-stu-id="d6e70-129">For more information about cryptography, see [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).</span></span>

 

