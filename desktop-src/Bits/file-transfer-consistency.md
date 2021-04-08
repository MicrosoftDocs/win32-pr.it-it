---
title: Coerenza del trasferimento di file
description: BITS garantisce che la versione del file da trasferire sia coerente in base alla dimensione del file e al timestamp, non al contenuto (i bit non proteggono dagli attacchi man-in-the-Middle).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855477"
---
# <a name="file-transfer-consistency"></a><span data-ttu-id="69dcd-103">Coerenza del trasferimento di file</span><span class="sxs-lookup"><span data-stu-id="69dcd-103">File Transfer Consistency</span></span>

<span data-ttu-id="69dcd-104">BITS garantisce che la versione del file da trasferire sia coerente in base alla dimensione del file e al timestamp, non al contenuto (i bit non proteggono dagli attacchi man-in-the-Middle).</span><span class="sxs-lookup"><span data-stu-id="69dcd-104">BITS guarantees that the version of the file it transfers is consistent based on the file size and time stamp, not content (BITS does not protect against man-in-the-middle attacks).</span></span> <span data-ttu-id="69dcd-105">Per verificare il contenuto, è possibile usare il metodo [**IBackgroundCopyFile3:: Gettemporaryname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) per ottenere il nome del file che contiene il contenuto scaricato, verificare il contenuto usando un meccanismo personalizzato, quindi chiamare il metodo [**IBackgroundCopyFile3:: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) per indicare a BITS se il contenuto del file è valido.</span><span class="sxs-lookup"><span data-stu-id="69dcd-105">To verify the contents yourself, you can use the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method to get the name of the file that contains the downloaded content, verify the contents using your own mechanism, and then call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method to indicate to BITS if the contents of the file is valid.</span></span> <span data-ttu-id="69dcd-106">Se si imposta lo stato di convalida su **false** e il contenuto proviene dal server di origine, il processo passa allo stato di errore.</span><span class="sxs-lookup"><span data-stu-id="69dcd-106">If you set the validation state to **FALSE** and the content is from the origin server, the job goes into the error state.</span></span> <span data-ttu-id="69dcd-107">Se il contenuto proviene da un peer, BITS scarica il file dal server di origine.</span><span class="sxs-lookup"><span data-stu-id="69dcd-107">If the content is from a peer, BITS downloads the file from the origin server.</span></span>

<span data-ttu-id="69dcd-108">Per i download, se le dimensioni del file o l'indicatore di data e ora cambiano mentre BITS sta trasferendo il file, BITS riavvia solo il trasferimento del file.</span><span class="sxs-lookup"><span data-stu-id="69dcd-108">For downloads, if the file size or time stamp changes while BITS is transferring the file, BITS restarts the transfer of that file only.</span></span> <span data-ttu-id="69dcd-109">Se, ad esempio, il processo di download contiene due file e i file vengono aggiornati nel server mentre BITS trasferisce il secondo file, BITS riavvia il trasferimento solo del secondo file.</span><span class="sxs-lookup"><span data-stu-id="69dcd-109">For example, if the download job contains two files and the files are updated on the server while BITS is transferring the second file, BITS restarts the transfer of the second file only.</span></span> <span data-ttu-id="69dcd-110">Il primo file, che è già stato trasferito correttamente, non viene aggiornato in modo da riflettere le nuove modifiche.</span><span class="sxs-lookup"><span data-stu-id="69dcd-110">The first file, which already transferred successfully, is not updated to reflect the new changes.</span></span>

<span data-ttu-id="69dcd-111">Si noti che se il file viene scaricato dal server, è necessario creare un nuovo URL per ogni nuova versione del file.</span><span class="sxs-lookup"><span data-stu-id="69dcd-111">Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file.</span></span> <span data-ttu-id="69dcd-112">Se si utilizza lo stesso URL per le nuove versioni del file, alcuni server proxy possono fornire dati non aggiornati dalla propria cache perché non vengono verificati con il server originale se il file non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="69dcd-112">If you use the same URL for new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale.</span></span>

<span data-ttu-id="69dcd-113">Per i caricamenti, se le dimensioni del file o l'indicatore di data e ora cambiano durante il trasferimento di file, BITS genera un errore e il processo viene inserito nello \_ \_ stato di errore dello stato del processo BG \_ .</span><span class="sxs-lookup"><span data-stu-id="69dcd-113">For uploads, if the file size or time stamp changes during the file transfer, BITS generates an error and the job is placed in the BG\_JOB\_STATE\_ERROR state.</span></span>

<span data-ttu-id="69dcd-114">BITS non sincronizza le richieste di trasferimento quando uno o più utenti richiedono che lo stesso file venga trasferito nello stesso percorso.</span><span class="sxs-lookup"><span data-stu-id="69dcd-114">BITS does not synchronize transfer requests when one or more users request that the same file be transferred to the same location.</span></span> <span data-ttu-id="69dcd-115">BITS trasferisce il file per ogni richiesta separatamente.</span><span class="sxs-lookup"><span data-stu-id="69dcd-115">BITS transfers the file for each request separately.</span></span>

 

 




