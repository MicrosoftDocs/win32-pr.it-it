---
title: Installazione del provider
description: La procedura per l'installazione del provider WMI DNS varia a seconda della versione di Windows in cui è installata.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Domain Name System, provider WMI, installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708647"
---
# <a name="installing-the-provider"></a><span data-ttu-id="7f54e-104">Installazione del provider</span><span class="sxs-lookup"><span data-stu-id="7f54e-104">Installing the Provider</span></span>

<span data-ttu-id="7f54e-105">La procedura per l'installazione del provider WMI DNS varia a seconda della versione di Windows in cui è installata.</span><span class="sxs-lookup"><span data-stu-id="7f54e-105">The procedure for installing the DNS WMI Provider differs based on the version of Windows on which it is installed.</span></span> <span data-ttu-id="7f54e-106">Nella procedura seguente viene descritto come installare e configurare il provider WMI DNS in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7f54e-106">The following procedure describes how to install and set up the DNS WMI Provider on Windows 2000.</span></span> <span data-ttu-id="7f54e-107">Per ottenere il provider WMI DNS per Windows 2000, scaricare il file seguente:</span><span class="sxs-lookup"><span data-stu-id="7f54e-107">To obtain the DNS WMI Provider for Windows 2000, download the following file:</span></span>

<span data-ttu-id="7f54e-108">**Avviso:** I file del provider WMI DNS non sono intercambiabili.</span><span class="sxs-lookup"><span data-stu-id="7f54e-108">**WARNING:** DNS WMI Provider files are not interchangeable.</span></span> <span data-ttu-id="7f54e-109">I server DNS di Windows 2000 richiedono file diversi e una procedura diversa rispetto ai server DNS di Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7f54e-109">Windows 2000 DNS Servers require different files and a different procedure than Windows Server 2003 DNS Servers.</span></span> <span data-ttu-id="7f54e-110">Viene fornita la procedura per ogni.</span><span class="sxs-lookup"><span data-stu-id="7f54e-110">The procedure for each is provided.</span></span>

<span data-ttu-id="7f54e-111">**Per installare il provider WMI DNS in Windows Server 2000**</span><span class="sxs-lookup"><span data-stu-id="7f54e-111">**To install the DNS WMI Provider on Windows 2000 Server**</span></span>

1.  <span data-ttu-id="7f54e-112">Ottenere il provider WMI DNS per Windows 2000 dal Resource Kit di Windows 2000 Server oppure scaricare il file Dnsprov.zip da: ftp://ftp.microsoft.com/reskit/win2000/</span><span class="sxs-lookup"><span data-stu-id="7f54e-112">Obtain the DNS WMI Provider for Windows 2000 from the Windows 2000 Server Resource Kit, or download the file, Dnsprov.zip, from: ftp://ftp.microsoft.com/reskit/win2000/</span></span>
2.  <span data-ttu-id="7f54e-113">Copiare i file del provider WMI DNS (Dnsprov.dll) e Dnsschema. mof nella <winntdir> \\ \\ directory WBEM di system32.</span><span class="sxs-lookup"><span data-stu-id="7f54e-113">Copy the DNS WMI Provider (Dnsprov.dll) and Dnsschema.mof files to the <winntdir>\\system32\\wbem directory.</span></span>
3.  <span data-ttu-id="7f54e-114">Compilare il file MOF.</span><span class="sxs-lookup"><span data-stu-id="7f54e-114">Compile the MOF file.</span></span> <span data-ttu-id="7f54e-115">Questa operazione consente di personalizzare lo schema in modo che corrisponda al server.</span><span class="sxs-lookup"><span data-stu-id="7f54e-115">Doing so customizes the schema to match the server.</span></span>

    <span data-ttu-id="7f54e-116">**mofcomp Dnsschema. mof**</span><span class="sxs-lookup"><span data-stu-id="7f54e-116">**mofcomp dnsschema.mof**</span></span>

4.  <span data-ttu-id="7f54e-117">Registrare la DLL nel server DNS.</span><span class="sxs-lookup"><span data-stu-id="7f54e-117">Register the DLL on the DNS Server.</span></span>

    <span data-ttu-id="7f54e-118">**regsvr32 dnsprov.dll**</span><span class="sxs-lookup"><span data-stu-id="7f54e-118">**regsvr32 dnsprov.dll**</span></span>

5.  <span data-ttu-id="7f54e-119">È possibile utilizzare script o programmi che utilizzano il provider WMI DNS per gestire i server DNS.</span><span class="sxs-lookup"><span data-stu-id="7f54e-119">Scripts or programs that use the DNS WMI Provider to manage DNS Servers can then be used.</span></span> <span data-ttu-id="7f54e-120">Gli script o i programmi possono essere eseguiti dal server DNS o da un computer client.</span><span class="sxs-lookup"><span data-stu-id="7f54e-120">The scripts or programs can be run from either the DNS Server, or from a client computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="7f54e-121">WMI SDK non è necessario per eseguire il provider WMI DNS, ma contiene molti strumenti utili.</span><span class="sxs-lookup"><span data-stu-id="7f54e-121">The WMI SDK is not required to run the DNS WMI Provider, but it contains many useful tools.</span></span>

     

<span data-ttu-id="7f54e-122">Il provider WMI DNS deve essere installato in qualsiasi server DNS da gestire; gli script DNS, tuttavia, possono essere eseguiti nel server DNS o in un host remoto.</span><span class="sxs-lookup"><span data-stu-id="7f54e-122">The DNS WMI Provider must be installed on any DNS Server to be managed; the DNS scripts, however, can be run on the DNS Server or on a remote host.</span></span>

<span data-ttu-id="7f54e-123">**Per installare il provider WMI DNS in Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f54e-123">**To install the DNS WMI Provider on Windows Server 2003**</span></span>

-   <span data-ttu-id="7f54e-124">Per i sistemi operativi Windows Server 2003, il provider WMI DNS viene installato e registrato automaticamente e il relativo file MOF viene compilato quando viene installato il servizio server DNS.</span><span class="sxs-lookup"><span data-stu-id="7f54e-124">For Windows Server 2003 operating systems, the DNS WMI Provider is automatically installed and registered, and its MOF file is compiled when the DNS Server service is installed.</span></span>

 

 




