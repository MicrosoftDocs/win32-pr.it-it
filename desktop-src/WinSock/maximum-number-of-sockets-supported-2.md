---
description: Il numero massimo di socket supportati da un particolare provider di servizi Windows Sockets è specifico dell'implementazione.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Numero massimo di socket supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306931"
---
# <a name="maximum-number-of-sockets-supported"></a><span data-ttu-id="2ae0f-103">Numero massimo di socket supportati</span><span class="sxs-lookup"><span data-stu-id="2ae0f-103">Maximum Number of Sockets Supported</span></span>

<span data-ttu-id="2ae0f-104">Il numero massimo di socket supportati da un particolare provider di servizi Windows Sockets è specifico dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-104">The maximum number of sockets supported by a particular Windows Sockets service provider is implementation specific.</span></span> <span data-ttu-id="2ae0f-105">Il provider Microsoft Winsock limita il numero massimo di socket supportati solo dalla memoria disponibile nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-105">The Microsoft Winsock provider limits the maximum number of sockets supported only by available memory on the local computer.</span></span> <span data-ttu-id="2ae0f-106">Tuttavia, i provider Winsock di terze parti possono avere limitazioni sul numero di socket supportati.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-106">However, third-party Winsock providers may have limitations on the numbers of sockets supported.</span></span> <span data-ttu-id="2ae0f-107">Un'applicazione non deve fare supposizioni sulla disponibilità di un determinato numero di socket.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-107">An application should make no assumptions about the availability of a certain number of sockets.</span></span> <span data-ttu-id="2ae0f-108">Per ulteriori informazioni su questo argomento, vedere [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span><span class="sxs-lookup"><span data-stu-id="2ae0f-108">For more information on this topic see [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span></span>

## <a name="fd_set-and-select"></a><span data-ttu-id="2ae0f-109">FD \_ impostare e selezionare</span><span class="sxs-lookup"><span data-stu-id="2ae0f-109">FD\_SET and select</span></span>

<span data-ttu-id="2ae0f-110">\_Nel file di intestazione *Winsock2. h* sono definite diverse macro fd XXX da usare per il porting delle applicazioni a Windows dall'ambiente UNIX.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-110">A number of FD\_XXX macros are defined in the *Winsock2.h* header file for use in porting applications to Windows from the UNIX environment.</span></span> <span data-ttu-id="2ae0f-111">Queste macro vengono usate con le funzioni [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) per il porting delle applicazioni a Windows.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-111">These macros are used with the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) and [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions for porting applications to Windows.</span></span> <span data-ttu-id="2ae0f-112">Il numero massimo di socket che possono essere usati da un'applicazione Windows Sockets non è influenzato dalla costante di manifesto FD \_ sesize.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-112">The maximum number of sockets that a Windows Sockets application can use is not affected by the manifest constant FD\_SETSIZE.</span></span> <span data-ttu-id="2ae0f-113">Questo valore definito nel file di intestazione *Winsock2. h* viene utilizzato per la costruzione delle strutture di [**\_ set FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) utilizzate con la funzione **Select** .</span><span class="sxs-lookup"><span data-stu-id="2ae0f-113">This value defined in the *Winsock2.h* header file is used in constructing the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures used with **select** function.</span></span> <span data-ttu-id="2ae0f-114">Il valore predefinito in Winsock2. h è 64.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-114">The default value in Winsock2.h is 64.</span></span> <span data-ttu-id="2ae0f-115">Se un'applicazione è progettata per essere in grado di utilizzare più di 64 socket usando le funzioni **Select** e **WSAPoll** , l'implementatore deve definire il manifesto di FD per \_ ogni file di origine prima di includere il file di intestazione *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="2ae0f-115">If an application is designed to be capable of working with more than 64 sockets using the **select** and **WSAPoll** functions, the implementor should define the manifest FD\_SETSIZE in every source file before including the *Winsock2.h* header file.</span></span> <span data-ttu-id="2ae0f-116">Un modo per eseguire questa operazione potrebbe consistere nell'includere la definizione all'interno delle opzioni del compilatore nel makefile.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-116">One way of doing this may be to include the definition within the compiler options in the makefile.</span></span> <span data-ttu-id="2ae0f-117">È ad esempio possibile aggiungere "-DFD \_ sesize = 128" come opzione alla riga di comando del compilatore per Microsoft C++.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-117">For example, you could add "-DFD\_SETSIZE=128" as an option to the compiler command line for Microsoft C++.</span></span> <span data-ttu-id="2ae0f-118">È necessario enfatizzare che \_ la definizione di dimensioni FD come un particolare valore non influisce sul numero effettivo di socket fornito da un provider di servizi Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="2ae0f-118">It must be emphasized that defining FD\_SETSIZE as a particular value has no effect on the actual number of sockets provided by a Windows Sockets service provider.</span></span> <span data-ttu-id="2ae0f-119">Questo valore influiscono solo sulle \_ macro fd xxx utilizzate dalle funzioni **SELECT** e **WSAPoll** .</span><span class="sxs-lookup"><span data-stu-id="2ae0f-119">This value only affects the FD\_XXX macros used by the **select** and **WSAPoll** functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ae0f-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ae0f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ae0f-121">**\_set FD**</span><span class="sxs-lookup"><span data-stu-id="2ae0f-121">**FD\_SET**</span></span>](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[<span data-ttu-id="2ae0f-122">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="2ae0f-122">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="2ae0f-123">**Selezionare**</span><span class="sxs-lookup"><span data-stu-id="2ae0f-123">**select**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[<span data-ttu-id="2ae0f-124">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="2ae0f-124">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="2ae0f-125">**WSAStartup**</span><span class="sxs-lookup"><span data-stu-id="2ae0f-125">**WSAStartup**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[<span data-ttu-id="2ae0f-126">**WSAPoll**</span><span class="sxs-lookup"><span data-stu-id="2ae0f-126">**WSAPoll**</span></span>](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
