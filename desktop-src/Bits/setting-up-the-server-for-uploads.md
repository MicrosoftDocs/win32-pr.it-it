---
title: Configurazione del server per i caricamenti
description: Per caricare file in un server utilizzando BITS, è necessario che nel server sia installato IIS e l'ISAPI estensione server BITS. Per i requisiti di IIS, vedere requisiti di IIS per i caricamenti BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220970"
---
# <a name="setting-up-the-server-for-uploads"></a><span data-ttu-id="d9c9a-104">Configurazione del server per i caricamenti</span><span class="sxs-lookup"><span data-stu-id="d9c9a-104">Setting Up the Server for Uploads</span></span>

<span data-ttu-id="d9c9a-105">Per caricare file in un server utilizzando BITS, è necessario che nel server sia installato IIS e l'ISAPI estensione server BITS.</span><span class="sxs-lookup"><span data-stu-id="d9c9a-105">To upload files to a server using BITS, the server must have IIS and the BITS server extension ISAPI installed.</span></span> <span data-ttu-id="d9c9a-106">Per i requisiti di IIS, vedere [requisiti di IIS per i caricamenti bits](iis-requirements-for-bits-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="d9c9a-106">For IIS requirements, see [IIS Requirements for BITS Uploads](iis-requirements-for-bits-uploads.md).</span></span>

<span data-ttu-id="d9c9a-107">Per informazioni sulla configurazione della directory virtuale IIS utilizzata da BITS per il caricamento, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9c9a-107">For information on configuring the IIS virtual directory that BITS uses for uploads, see the following topics.</span></span>

-   [<span data-ttu-id="d9c9a-108">Impostazione delle autorizzazioni per le directory virtuali</span><span class="sxs-lookup"><span data-stu-id="d9c9a-108">Setting Permissions on Virtual Directories</span></span>](setting-permissions-on-virtual-directories.md)
-   [<span data-ttu-id="d9c9a-109">Scrittura di uno script per configurare la directory virtuale</span><span class="sxs-lookup"><span data-stu-id="d9c9a-109">Writing a Script to Configure the Virtual Directory</span></span>](writing-a-script-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="d9c9a-110">Utilizzo dell'interfaccia utente di IIS per configurare la directory virtuale</span><span class="sxs-lookup"><span data-stu-id="d9c9a-110">Using the IIS UI to Configure the Virtual Directory</span></span>](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="d9c9a-111">Prevenzione di più caricamenti</span><span class="sxs-lookup"><span data-stu-id="d9c9a-111">Preventing Multiple Uploads</span></span>](preventing-multiple-uploads.md)
-   [<span data-ttu-id="d9c9a-112">Procedure consigliate per il caricamento</span><span class="sxs-lookup"><span data-stu-id="d9c9a-112">Upload Best Practices</span></span>](upload-best-practices.md)

> [!Note]  
> <span data-ttu-id="d9c9a-113">Alcune installazioni IIS includono il componente di filtro UrlScan.</span><span class="sxs-lookup"><span data-stu-id="d9c9a-113">Some IIS installations include the UrlScan filtering component.</span></span> <span data-ttu-id="d9c9a-114">Se UrlScan è abilitato, è necessario che l'amministratore aggiunga il \_ verbo "bits post" all'elenco di verbi HTTP consentiti di URLScan.</span><span class="sxs-lookup"><span data-stu-id="d9c9a-114">If UrlScan is enabled, the administrator must add the "BITS\_POST" verb to UrlScan's list of allowed HTTP verbs.</span></span> <span data-ttu-id="d9c9a-115">In caso contrario, i caricamenti client BITS avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d9c9a-115">Otherwise, BITS client uploads will fail.</span></span> <span data-ttu-id="d9c9a-116">Per ulteriori informazioni sull'abilitazione dei verbi in UrlScan, vedere la documentazione di UrlScan.</span><span class="sxs-lookup"><span data-stu-id="d9c9a-116">For further details on enabling verbs in UrlScan, see the UrlScan documentation.</span></span>

 

 

 




