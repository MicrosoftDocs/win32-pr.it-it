---
description: Descrive I concetti di base di I/O.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Concetti di I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317781"
---
# <a name="io-concepts"></a><span data-ttu-id="94999-103">Concetti di I/O</span><span class="sxs-lookup"><span data-stu-id="94999-103">I/O Concepts</span></span>

<span data-ttu-id="94999-104">In questa sezione vengono descritti i concetti di I/O seguenti.</span><span class="sxs-lookup"><span data-stu-id="94999-104">The following I/O concepts are described in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="94999-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="94999-105">In this section</span></span>



| <span data-ttu-id="94999-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="94999-106">Topic</span></span>                                                                               | <span data-ttu-id="94999-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94999-107">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94999-108">Buffering dei file</span><span class="sxs-lookup"><span data-stu-id="94999-108">File Buffering</span></span>](file-buffering.md)<br/>                                     | <span data-ttu-id="94999-109">Vengono descritte le considerazioni per il controllo dell'applicazione del buffering dei file, noto anche come input/output (I/O) file non memorizzato nel buffer.</span><span class="sxs-lookup"><span data-stu-id="94999-109">Describes considerations for application control of file buffering, also known as unbuffered file input/output (I/O).</span></span><br/>                                    |
| [<span data-ttu-id="94999-110">Memorizzazione nella cache dei file</span><span class="sxs-lookup"><span data-stu-id="94999-110">File Caching</span></span>](file-caching.md)<br/>                                         | <span data-ttu-id="94999-111">Windows memorizza nella cache i dati del file letti dai dischi e scritti nei dischi.</span><span class="sxs-lookup"><span data-stu-id="94999-111">Windows caches file data that is read from disks and written to disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="94999-112">I/O sincrono e asincrono</span><span class="sxs-lookup"><span data-stu-id="94999-112">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)<br/> | <span data-ttu-id="94999-113">Esistono due tipi di sincronizzazione di input/output (I/O): I/o sincrono e I/O asincrono.</span><span class="sxs-lookup"><span data-stu-id="94999-113">There are two types of input/output (I/O) synchronization: synchronous I/O and asynchronous I/O.</span></span> <span data-ttu-id="94999-114">L'I/O asincrono è noto anche come I/O sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="94999-114">Asynchronous I/O is also referred to as overlapped I/O.</span></span><br/> |
| [<span data-ttu-id="94999-115">Annullamento di operazioni di I/O in sospeso</span><span class="sxs-lookup"><span data-stu-id="94999-115">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)<br/> | <span data-ttu-id="94999-116">Consentire agli utenti di annullare le richieste di I/O lente o bloccate può migliorare l'usabilità e l'affidabilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="94999-116">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span><br/>                             |
| [<span data-ttu-id="94999-117">I/O Alertable</span><span class="sxs-lookup"><span data-stu-id="94999-117">Alertable I/O</span></span>](alertable-i-o.md)<br/>                                       | <span data-ttu-id="94999-118">L'I/O Alertable è il metodo mediante il quale i thread dell'applicazione elaborano le richieste I/O asincrone solo quando sono in uno stato di avviso.</span><span class="sxs-lookup"><span data-stu-id="94999-118">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span><br/>                     |
| [<span data-ttu-id="94999-119">Porte di completamento I/O</span><span class="sxs-lookup"><span data-stu-id="94999-119">I/O Completion Ports</span></span>](i-o-completion-ports.md)<br/>                         | <span data-ttu-id="94999-120">Le porte di completamento i/O forniscono un modello di threading efficiente per l'elaborazione di più richieste di I/O asincrone in un sistema multiprocessore.</span><span class="sxs-lookup"><span data-stu-id="94999-120">I/O completion ports provide an efficient threading model for processing multiple asynchronous I/O requests on a multiprocessor system.</span></span><br/>                  |



 

 

 




