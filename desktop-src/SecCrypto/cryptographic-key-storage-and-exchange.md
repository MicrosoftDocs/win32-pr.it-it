---
description: Esistono situazioni in cui le chiavi devono essere esportate dall'ambiente protetto del provider del servizio di crittografia (CSP) nello spazio dati di un'applicazione. Le chiavi esportate vengono archiviate in strutture BLOB di chiavi crittografate.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Archiviazione delle chiavi crittografiche ed Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306460"
---
# <a name="cryptographic-key-storage-and-exchange"></a><span data-ttu-id="d1e75-104">Archiviazione delle chiavi crittografiche ed Exchange</span><span class="sxs-lookup"><span data-stu-id="d1e75-104">Cryptographic Key Storage and Exchange</span></span>

<span data-ttu-id="d1e75-105">Esistono situazioni in cui le chiavi devono essere esportate dall'ambiente protetto del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) nello spazio dati di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1e75-105">There are situations where keys must be exported from the secure environment of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) into an application's data space.</span></span> <span data-ttu-id="d1e75-106">Le chiavi esportate vengono archiviate in strutture [*BLOB di chiavi*](../secgloss/k-gly.md) crittografate.</span><span class="sxs-lookup"><span data-stu-id="d1e75-106">Keys that have been exported are stored in encrypted [*key BLOB*](../secgloss/k-gly.md) structures.</span></span>

<span data-ttu-id="d1e75-107">Esistono due situazioni specifiche in cui è necessario esportare le chiavi:</span><span class="sxs-lookup"><span data-stu-id="d1e75-107">There are two specific situations where it is necessary to export keys:</span></span>

-   <span data-ttu-id="d1e75-108">Per salvare una [*chiave di sessione*](../secgloss/s-gly.md) per un uso successivo da un'applicazione, se, ad esempio, un'applicazione ha appena crittografato un file di database da decrittografare in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="d1e75-108">To save a [*session key*](../secgloss/s-gly.md) for later use by an application, if, for example, an application has just encrypted a database file to be decrypted at a later time.</span></span> <span data-ttu-id="d1e75-109">L'applicazione è responsabile dell'archiviazione della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="d1e75-109">The application is responsible for storing the encryption key.</span></span> <span data-ttu-id="d1e75-110">Questa operazione è necessaria perché i CSP non conservano le [*chiavi simmetriche*](../secgloss/s-gly.md) dalla sessione alla sessione.</span><span class="sxs-lookup"><span data-stu-id="d1e75-110">This is necessary because CSPs do not preserve [*symmetric keys*](../secgloss/s-gly.md) from session to session.</span></span>
-   <span data-ttu-id="d1e75-111">Per inviare una chiave a un altro utente.</span><span class="sxs-lookup"><span data-stu-id="d1e75-111">To send a key to someone else.</span></span> <span data-ttu-id="d1e75-112">Questo sarebbe più semplice se i rispettivi CSP potessero comunicare direttamente, ma non possono.</span><span class="sxs-lookup"><span data-stu-id="d1e75-112">This would be easier if the respective CSPs could communicate directly, but they cannot.</span></span> <span data-ttu-id="d1e75-113">Poiché i CSP non possono comunicare, la chiave deve essere esportata da un CSP, trasmessa all'applicazione di destinazione e quindi importata nel CSP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d1e75-113">Because CSPs cannot communicate, the key has to be exported from one CSP, transmitted to the destination application, and then imported into the destination CSP.</span></span> <span data-ttu-id="d1e75-114">Questo processo può diventare più complesso se il percorso di comunicazione non è attendibile.</span><span class="sxs-lookup"><span data-stu-id="d1e75-114">This process can become more complicated if the communication path is not trusted.</span></span>

<span data-ttu-id="d1e75-115">In entrambi i casi, un'applicazione deve archiviare una chiave di sessione all'esterno del CSP per un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="d1e75-115">In either case, an application must store a session key outside the CSP for a period of time.</span></span> <span data-ttu-id="d1e75-116">Per ulteriori informazioni, vedere [la procedura per l'archiviazione di una chiave di sessione](procedure-for-storing-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="d1e75-116">For more information, see [Procedure for Storing a Session Key](procedure-for-storing-a-session-key.md).</span></span>

 

 
