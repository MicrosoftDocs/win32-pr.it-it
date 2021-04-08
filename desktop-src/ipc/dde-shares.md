---
description: Le condivisioni DDE sono una risorsa del computer.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Condivisioni DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882234"
---
# <a name="dde-shares"></a><span data-ttu-id="725fc-103">Condivisioni DDE</span><span class="sxs-lookup"><span data-stu-id="725fc-103">DDE Shares</span></span>

<span data-ttu-id="725fc-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="725fc-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="725fc-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="725fc-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="725fc-106">Le condivisioni DDE sono una risorsa del computer.</span><span class="sxs-lookup"><span data-stu-id="725fc-106">DDE shares are a machine resource.</span></span> <span data-ttu-id="725fc-107">Sono simili alle condivisioni file perché vengono usate per controllare l'accesso a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="725fc-107">They are similar to file shares because they are used to control access to a resource.</span></span> <span data-ttu-id="725fc-108">Con le condivisioni file, la risorsa è un file.</span><span class="sxs-lookup"><span data-stu-id="725fc-108">With file shares, the resource is a file.</span></span> <span data-ttu-id="725fc-109">Con le condivisioni DDE, la risorsa viene scambiata dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="725fc-109">With DDE shares, the resource is dynamically exchanged data.</span></span> <span data-ttu-id="725fc-110">Il tipo di dati scambiati è determinato dall'applicazione server che fornisce i dati e l'applicazione client che richiede i dati.</span><span class="sxs-lookup"><span data-stu-id="725fc-110">The type of data exchanged is determined by the server application that supplies the data and the client application that requests the data.</span></span>

<span data-ttu-id="725fc-111">Il server chiama la funzione [**NDDEShareAdd**](nddeshareadd.md) per creare la condivisione DDE, archiviata in gestione database di condivisione DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="725fc-111">The server calls the [**NDdeShareAdd**](nddeshareadd.md) function to create the DDE share, which is stored in the DDE share database manager (DSDM).</span></span>

<span data-ttu-id="725fc-112">Il client avvia la conversazione DDE connettendosi alla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="725fc-112">The client starts the DDE conversation by connecting to the DDE share.</span></span> <span data-ttu-id="725fc-113">Il client deve chiamare la funzione [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) per inizializzare DDEML e chiamare la funzione [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) per connettersi alla condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="725fc-113">The client must call the [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) function to initialize DDEML and call the [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) function to connect to the DDE share.</span></span> <span data-ttu-id="725fc-114">Nella chiamata a **DdeConnect** , il client specifica il nome del servizio come segue:</span><span class="sxs-lookup"><span data-stu-id="725fc-114">In the **DdeConnect** call, the client specifies the service name as follows:</span></span>

<span data-ttu-id="725fc-115">\\\\*Nomecomputer* \\ NDDE $</span><span class="sxs-lookup"><span data-stu-id="725fc-115">\\\\*ComputerName*\\NDDE$</span></span>

<span data-ttu-id="725fc-116">dove *nomecomputer* è il nome del computer in cui è in esecuzione l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="725fc-116">where *ComputerName* is the name of the computer running the server application.</span></span> <span data-ttu-id="725fc-117">NDDE $ indica che l'argomento fornito a [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) è il nome della condivisione DDE nel computer remoto denominato *ComputerName*.</span><span class="sxs-lookup"><span data-stu-id="725fc-117">The NDDE$ indicates that the topic provided to [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) is the DDE share name on the remote computer named *ComputerName*.</span></span>

<span data-ttu-id="725fc-118">Sono disponibili tre tipi di condivisioni DDE: vecchio stile, nuovo stile e statico.</span><span class="sxs-lookup"><span data-stu-id="725fc-118">There are three types of DDE shares: old style, new style, and static.</span></span> <span data-ttu-id="725fc-119">È tipico per supportare solo il tipo statico.</span><span class="sxs-lookup"><span data-stu-id="725fc-119">It is typical to support only the static type.</span></span> <span data-ttu-id="725fc-120">I nomi delle condivisioni statiche utilizzano la convenzione seguente: *ShareName*$.</span><span class="sxs-lookup"><span data-stu-id="725fc-120">The names of static shares use the following convention: *ShareName*$.</span></span>

 

 
