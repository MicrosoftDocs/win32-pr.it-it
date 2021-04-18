---
description: I tipi di dati supportati da VDS definiscono i valori restituiti dalla funzione, i parametri della funzione e i membri della struttura. I tipi di dati definiscono le dimensioni e il significato di questi elementi.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Tipi di dati VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318204"
---
# <a name="vds-data-types"></a><span data-ttu-id="784e5-104">Tipi di dati VDS</span><span class="sxs-lookup"><span data-stu-id="784e5-104">VDS Data Types</span></span>

<span data-ttu-id="784e5-105">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="784e5-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="784e5-106">I tipi di dati supportati da VDS definiscono i valori restituiti dalla funzione, i parametri della funzione e i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="784e5-106">The data types supported by VDS define function return values, function parameters, and structure members.</span></span> <span data-ttu-id="784e5-107">I tipi di dati definiscono le dimensioni e il significato di questi elementi.</span><span class="sxs-lookup"><span data-stu-id="784e5-107">Data types define the size and meaning of these elements.</span></span>



| <span data-ttu-id="784e5-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="784e5-108">Data type</span></span>                                                                                      | <span data-ttu-id="784e5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="784e5-109">Description</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="784e5-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ID oggetto \_ VDS**</span><span class="sxs-lookup"><span data-stu-id="784e5-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS\_OBJECT\_ID**</span></span><br/> | <span data-ttu-id="784e5-111">ID oggetto VDS.</span><span class="sxs-lookup"><span data-stu-id="784e5-111">VDS object ID.</span></span> <span data-ttu-id="784e5-112">Questi valori non sono necessariamente univoci tra i riavvii.</span><span class="sxs-lookup"><span data-stu-id="784e5-112">These values are not guaranteed to be unique across reboots.</span></span> <br/> <span data-ttu-id="784e5-113">Questo tipo viene dichiarato in VDS. h (VdsHwPrv. h per i provider hardware) come GUID.</span><span class="sxs-lookup"><span data-stu-id="784e5-113">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a GUID.</span></span> <br/> |
| <span data-ttu-id="784e5-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**\_ID percorso \_ VDS**</span><span class="sxs-lookup"><span data-stu-id="784e5-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS\_PATH\_ID**</span></span><br/>       | <span data-ttu-id="784e5-115">ID percorso VDS per la funzionalità Multipath I/O (MPIO).</span><span class="sxs-lookup"><span data-stu-id="784e5-115">VDS path ID for multipath I/O (MPIO).</span></span> <br/> <span data-ttu-id="784e5-116">Questo tipo viene dichiarato in VDS. h (VdsHwPrv. h per i provider hardware) come UINT64.</span><span class="sxs-lookup"><span data-stu-id="784e5-116">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a UINT64.</span></span><br/>                                      |



 

 

