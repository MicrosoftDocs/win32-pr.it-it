---
description: In questa sezione vengono descritte le considerazioni sul porting Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Porting delle applicazioni socket in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306908"
---
# <a name="porting-socket-applications-to-winsock"></a><span data-ttu-id="62432-103">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="62432-103">Porting Socket Applications to Winsock</span></span>

<span data-ttu-id="62432-104">In questa sezione vengono descritte le considerazioni sul porting Winsock.</span><span class="sxs-lookup"><span data-stu-id="62432-104">This section describes Winsock porting considerations.</span></span>

<span data-ttu-id="62432-105">Il numero di istanze di Windows Sockets è limitato da una stretta aderenza alle convenzioni di Berkeley, in genere a causa di problemi di implementazione nell'ambiente Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="62432-105">There are a limited number of instances where Windows Sockets has diverted from strict adherence to the Berkeley conventions, usually due to implementation difficulties in the Microsoft Windows environment.</span></span>

<span data-ttu-id="62432-106">Quando si verifica una deviazione dalle convenzioni di Berkeley in Windows Sockets, la deviazione è specifica e chiaramente nota.</span><span class="sxs-lookup"><span data-stu-id="62432-106">When a deviation from Berkeley conventions occurs in Windows Sockets, the deviation is specifically and clearly noted.</span></span> <span data-ttu-id="62432-107">Ad esempio, se una funzione è specifica di Windows Sockets, tale deviazione viene specificata con una frase nella descrizione della funzione simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="62432-107">For example, if a function is specific to Windows Sockets, that deviation is specified with a phrase in the function description similar to the following:</span></span>

<span data-ttu-id="62432-108">La funzione del **\[ nome \] di funzione** è un'estensione specifica di Microsoft per l'API di Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="62432-108">The **\[function-name\]** function is a Microsoft-specific extension to the Windows Sockets 2 API.</span></span>

<span data-ttu-id="62432-109">In questa sezione vengono fornite informazioni sul porting delle applicazioni socket UNIX di Berkeley (BSD) a Winsock:</span><span class="sxs-lookup"><span data-stu-id="62432-109">This section provides information about porting Berkeley (BSD) UNIX socket applications to Winsock:</span></span>

-   [<span data-ttu-id="62432-110">Tipo di dati socket</span><span class="sxs-lookup"><span data-stu-id="62432-110">Socket Data Type</span></span>](socket-data-type-2.md)
-   [<span data-ttu-id="62432-111">Macro Select, FD \_ set e FD \_ xxx</span><span class="sxs-lookup"><span data-stu-id="62432-111">Select, FD\_SET, and FD\_XXX Macros</span></span>](select-and-fd---2.md)
-   [<span data-ttu-id="62432-112">Codici di errore-errno, h \_ errno e WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="62432-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [<span data-ttu-id="62432-113">Pointers</span><span class="sxs-lookup"><span data-stu-id="62432-113">Pointers</span></span>](pointers-2.md)
-   [<span data-ttu-id="62432-114">Funzioni rinominate</span><span class="sxs-lookup"><span data-stu-id="62432-114">Renamed Functions</span></span>](renamed-functions-2.md)
-   [<span data-ttu-id="62432-115">Numero massimo di socket supportati</span><span class="sxs-lookup"><span data-stu-id="62432-115">Maximum Number of Sockets Supported</span></span>](maximum-number-of-sockets-supported-2.md)
-   [<span data-ttu-id="62432-116">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="62432-116">Include Files</span></span>](include-files-2.md)
-   [<span data-ttu-id="62432-117">Valori restituiti sull'errore della funzione</span><span class="sxs-lookup"><span data-stu-id="62432-117">Return Values on Function Failure</span></span>](return-values-on-function-failure-2.md)
-   [<span data-ttu-id="62432-118">Socket non elaborati</span><span class="sxs-lookup"><span data-stu-id="62432-118">Raw Sockets</span></span>](service-provided-raw-sockets-2.md)
-   [<span data-ttu-id="62432-119">Ordinamento byte</span><span class="sxs-lookup"><span data-stu-id="62432-119">Byte Ordering</span></span>](byte-ordering-2.md)
-   [<span data-ttu-id="62432-120">Routine di conversione Byte-Order estese</span><span class="sxs-lookup"><span data-stu-id="62432-120">Extended Byte-Order Conversion Routines</span></span>](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a><span data-ttu-id="62432-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62432-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62432-122">Gestione degli errori Winsock</span><span class="sxs-lookup"><span data-stu-id="62432-122">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="62432-123">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="62432-123">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="62432-124">Codici di errore di Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="62432-124">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="62432-125">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="62432-125">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



