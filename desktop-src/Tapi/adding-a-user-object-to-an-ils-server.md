---
description: Nel frammento di codice seguente viene illustrata la pubblicazione di un oggetto utente in un server ILS. Dopo la pubblicazione di un oggetto utente, le entità remote possono utilizzare l'oggetto utente per effettuare chiamate all'utente specificato.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Aggiunta di un oggetto utente a un server ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750783"
---
# <a name="adding-a-user-object-to-an-ils-server"></a><span data-ttu-id="16cee-104">Aggiunta di un oggetto utente a un server ILS</span><span class="sxs-lookup"><span data-stu-id="16cee-104">Adding a User Object to an ILS Server</span></span>

<span data-ttu-id="16cee-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="16cee-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="16cee-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="16cee-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="16cee-107">Nel frammento di codice seguente viene illustrata la pubblicazione di un oggetto utente in un server ILS.</span><span class="sxs-lookup"><span data-stu-id="16cee-107">The following code fragment illustrates publishing a user object in an ILS server.</span></span> <span data-ttu-id="16cee-108">Dopo la pubblicazione di un oggetto utente, le entità remote possono utilizzare l'oggetto utente per effettuare chiamate all'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="16cee-108">After a user object is published, remote parties can use the user object to make calls to the specified user.</span></span>

<span data-ttu-id="16cee-109">Questo frammento presuppone che la [connessione a un server ILS](connecting-to-an-ils-server.md) sia già stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="16cee-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a><span data-ttu-id="16cee-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16cee-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16cee-111">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="16cee-111">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="16cee-112">**ITDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="16cee-112">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="16cee-113">**ITDirectoryObjectUser**</span><span class="sxs-lookup"><span data-stu-id="16cee-113">**ITDirectoryObjectUser**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



