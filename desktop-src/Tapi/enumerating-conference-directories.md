---
description: Nel frammento di codice seguente viene illustrata l'enumerazione delle conferenze in un server ILS specificato. Questo frammento presuppone che la connessione a un server ILS sia già stata eseguita.
ms.assetid: da01c534-c700-4b4f-ac22-cede9930f80d
title: Enumerazione delle directory delle conferenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eedffb44d92f52293dc9d1add8b53588503282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485412"
---
# <a name="enumerating-conference-directories"></a><span data-ttu-id="8abf2-104">Enumerazione delle directory delle conferenze</span><span class="sxs-lookup"><span data-stu-id="8abf2-104">Enumerating Conference Directories</span></span>

<span data-ttu-id="8abf2-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8abf2-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8abf2-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8abf2-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8abf2-107">Nel frammento di codice seguente viene illustrata l'enumerazione delle conferenze in un server ILS specificato.</span><span class="sxs-lookup"><span data-stu-id="8abf2-107">The following code fragment illustrates the enumeration of conferences on a specified ILS server.</span></span> <span data-ttu-id="8abf2-108">Questo frammento presuppone che la [connessione a un server ILS](connecting-to-an-ils-server.md) sia già stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="8abf2-108">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
SysFreeString( bNameToSearch );
```



## <a name="related-topics"></a><span data-ttu-id="8abf2-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8abf2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8abf2-110">**IEnumDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="8abf2-110">**IEnumDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)
</dt> </dl>

 

 



