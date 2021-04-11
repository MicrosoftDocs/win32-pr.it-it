---
description: I dati protetti vengono archiviati come BLOB con codifica ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato dati protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131299"
---
# <a name="protected-data-format"></a><span data-ttu-id="bf4b3-103">Formato dati protetto</span><span class="sxs-lookup"><span data-stu-id="bf4b3-103">Protected Data Format</span></span>

<span data-ttu-id="bf4b3-104">I dati protetti vengono archiviati come BLOB con codifica ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="bf4b3-104">Protected data is stored as an ASN.1 encoded BLOB.</span></span> <span data-ttu-id="bf4b3-105">I dati vengono formattati come contenuti in busta CMS (certificate Message Syntax).</span><span class="sxs-lookup"><span data-stu-id="bf4b3-105">The data is formatted as CMS (certificate message syntax) enveloped content.</span></span> <span data-ttu-id="bf4b3-106">La busta digitale contiene contenuto crittografato, informazioni sui destinatari contenenti una chiave di crittografia del contenuto crittografata (CEK) e un'intestazione che contiene informazioni sul contenuto, inclusa la stringa della regola descrittore di protezione non crittografata.</span><span class="sxs-lookup"><span data-stu-id="bf4b3-106">The digital envelope contains encrypted content, recipient information that contains an encrypted content encryption key (CEK), and a header that contains information about the content, including the unencrypted protection descriptor rule string.</span></span> <span data-ttu-id="bf4b3-107">Questa operazione viene illustrata nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="bf4b3-107">This is shown by the following diagram.</span></span>

![dati busta protetti](images/protecteddatablob.png)

## <a name="related-topics"></a><span data-ttu-id="bf4b3-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf4b3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf4b3-110">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="bf4b3-110">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="bf4b3-111">Descrittori di protezione</span><span class="sxs-lookup"><span data-stu-id="bf4b3-111">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> <dt>

[<span data-ttu-id="bf4b3-112">Provider di protezione</span><span class="sxs-lookup"><span data-stu-id="bf4b3-112">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



