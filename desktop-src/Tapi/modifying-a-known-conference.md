---
description: Nel frammento di codice seguente viene illustrata la modifica di un intervallo di tempo di conferenze. L'intervallo di tempo predefinito è 30 minuti. In questo frammento, l'intervallo di tempo è impostato su un anno.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Modifica di una conferenza Nota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225861"
---
# <a name="modifying-a-known-conference"></a><span data-ttu-id="ee050-105">Modifica di una conferenza Nota</span><span class="sxs-lookup"><span data-stu-id="ee050-105">Modifying a Known Conference</span></span>

<span data-ttu-id="ee050-106">\[I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ee050-106">\[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ee050-107">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ee050-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ee050-108">Nel frammento di codice seguente viene illustrata la modifica dell'intervallo di tempo di una conferenza.</span><span class="sxs-lookup"><span data-stu-id="ee050-108">The following code fragment illustrates modification of a conference's time span.</span></span> <span data-ttu-id="ee050-109">L'intervallo di tempo predefinito è 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="ee050-109">The default time span is thirty minutes.</span></span> <span data-ttu-id="ee050-110">In questo frammento, l'intervallo di tempo è impostato su un anno.</span><span class="sxs-lookup"><span data-stu-id="ee050-110">In this fragment, the time span is set to one year.</span></span>

<span data-ttu-id="ee050-111">Questo frammento presuppone che la [connessione a un server ILS](connecting-to-an-ils-server.md) sia già stata eseguita e che sia stata eseguita un' [enumerazione della directory della conferenza](enumerating-conference-directories.md) per ottenere la voce della directory che verrà modificata.</span><span class="sxs-lookup"><span data-stu-id="ee050-111">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed and that a [conference directory enumeration](enumerating-conference-directories.md) has been performed to obtain the directory entry that will be modified.</span></span>

<span data-ttu-id="ee050-112">Questo frammento presuppone inoltre che non si tratta di una conferenza multicast.</span><span class="sxs-lookup"><span data-stu-id="ee050-112">This fragment also assumes this is not a multicast conference.</span></span> <span data-ttu-id="ee050-113">Per modificare gli orari di una conferenza multicast è necessario notificare il server di allocazione indirizzi multicast.</span><span class="sxs-lookup"><span data-stu-id="ee050-113">Changing the times on a multicast conference requires notification of the multicast address allocation server.</span></span> <span data-ttu-id="ee050-114">Per un esempio di utilizzo dell'indirizzamento multicast, vedere [acquisizione di un indirizzo multicast](acquiring-a-multicast-address.md) .</span><span class="sxs-lookup"><span data-stu-id="ee050-114">See [Acquiring a Multicast Address](acquiring-a-multicast-address.md) for an example of working with multicast addressing.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="ee050-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee050-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee050-116">**ITDirectoryObjectConference**</span><span class="sxs-lookup"><span data-stu-id="ee050-116">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



