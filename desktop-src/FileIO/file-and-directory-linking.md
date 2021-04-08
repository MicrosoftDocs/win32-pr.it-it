---
description: 'Nel file system NTFS sono supportati due tipi di collegamenti: collegamenti reali e giunzioni.'
ms.assetid: 548acfe5-c9e1-4227-ba20-674e071f121f
title: Collegamento di file e directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70bcb905b73f7635ba5bdc4afcc44280023c7a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968404"
---
# <a name="file-and-directory-linking"></a><span data-ttu-id="21e00-103">Collegamento di file e directory</span><span class="sxs-lookup"><span data-stu-id="21e00-103">File and Directory Linking</span></span>

<span data-ttu-id="21e00-104">Il file system NTFS consente di creare una rappresentazione di sistema di un file o di una directory in un percorso della struttura di directory diverso dall'oggetto file o directory a cui si è connessi.</span><span class="sxs-lookup"><span data-stu-id="21e00-104">The NTFS file system provides the ability to create a system representation of a file or directory in a location in the directory structure that is different from the file or directory object that is being linked to.</span></span> <span data-ttu-id="21e00-105">Questo processo viene chiamato collegamento.</span><span class="sxs-lookup"><span data-stu-id="21e00-105">This process is called linking.</span></span> <span data-ttu-id="21e00-106">Nel file system NTFS sono supportati due tipi di collegamenti: [collegamenti reali e giunzioni](hard-links-and-junctions.md).</span><span class="sxs-lookup"><span data-stu-id="21e00-106">There are two types of links supported in the NTFS file system: [hard links and junctions](hard-links-and-junctions.md).</span></span>

<span data-ttu-id="21e00-107">Il file system NTFS fornisce inoltre il [servizio di rilevamento](distributed-link-tracking-and-object-identifiers.md)dei collegamenti distribuiti, che tiene traccia automaticamente dei collegamenti quando vengono spostati.</span><span class="sxs-lookup"><span data-stu-id="21e00-107">The NTFS file system also provides the [distributed link tracking service](distributed-link-tracking-and-object-identifiers.md), which automatically tracks links as they are moved.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="21e00-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="21e00-108">In this section</span></span>



| <span data-ttu-id="21e00-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="21e00-109">Topic</span></span>                                                                                                               | <span data-ttu-id="21e00-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21e00-110">Description</span></span>                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21e00-111">Collegamenti reali e giunzioni</span><span class="sxs-lookup"><span data-stu-id="21e00-111">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)<br/>                                                 | <span data-ttu-id="21e00-112">Vengono descritti i collegamenti reali e le giunzioni.</span><span class="sxs-lookup"><span data-stu-id="21e00-112">Describes hard links and junctions.</span></span><br/>                                                                          |
| [<span data-ttu-id="21e00-113">Rilevamento dei collegamenti distribuiti e identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="21e00-113">Distributed Link Tracking and Object Identifiers</span></span>](distributed-link-tracking-and-object-identifiers.md)<br/> | <span data-ttu-id="21e00-114">Il **servizio di rilevamento dei collegamenti distribuiti** consente alle applicazioni client di rilevare le origini dei collegamenti che sono state spostate.</span><span class="sxs-lookup"><span data-stu-id="21e00-114">The **distributed link tracking service** enables client applications to track link sources that have moved.</span></span><br/> |



 

 

 




