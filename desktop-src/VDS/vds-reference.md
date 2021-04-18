---
description: In questa sezione vengono descritte le Application Programming Interface al servizio dischi virtuali (VDS).
ms.assetid: d00fc772-331f-4d71-a418-e34acdfb6652
title: Riferimento VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369111add0b3f4b7e2742c764a6cbf8b1d8bfdd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313240"
---
# <a name="vds-reference"></a><span data-ttu-id="04e81-103">Riferimento VDS</span><span class="sxs-lookup"><span data-stu-id="04e81-103">VDS Reference</span></span>

<span data-ttu-id="04e81-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="04e81-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="04e81-105">In questa sezione vengono descritte le Application Programming Interface al servizio dischi virtuali (VDS).</span><span class="sxs-lookup"><span data-stu-id="04e81-105">This section describes the application programming interface to the Virtual Disk Service (VDS).</span></span>

<span data-ttu-id="04e81-106">Gli sviluppatori di applicazioni usano le interfacce, le strutture, le enumerazioni e le costanti simboliche in questa API per eseguire query e configurare l'archiviazione, dai dischi agli array di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="04e81-106">Application developers use the interfaces, structures, enumerations, and symbolic constants in this API to query and configure storage—from disks to storage arrays.</span></span> <span data-ttu-id="04e81-107">Per esaminare in dettaglio la relazione tra i tipi VDS, vedere il [modello a oggetti VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="04e81-107">For a detailed look at the relationship among VDS types, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="04e81-108">I produttori di archiviazione implementano molte delle interfacce definite in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="04e81-108">Storage manufacturers implement many of the interfaces defined in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="04e81-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="04e81-109">In this Section</span></span>

<dl> <dt>

[<span data-ttu-id="04e81-110">Costanti VDS</span><span class="sxs-lookup"><span data-stu-id="04e81-110">VDS Constants</span></span>](vds-constants.md)
</dt> <dd>

<span data-ttu-id="04e81-111">Elenca le costanti simboliche nell'API VDS.</span><span class="sxs-lookup"><span data-stu-id="04e81-111">Lists the symbolic constants in the VDS API.</span></span>

</dd> <dt>

[<span data-ttu-id="04e81-112">Tipi di dati VDS</span><span class="sxs-lookup"><span data-stu-id="04e81-112">VDS Data Types</span></span>](vds-data-types.md)
</dt> <dd>

<span data-ttu-id="04e81-113">Elenca i tipi di dati usati con VDS.</span><span class="sxs-lookup"><span data-stu-id="04e81-113">Lists the data types used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="04e81-114">Enumerazioni VDS</span><span class="sxs-lookup"><span data-stu-id="04e81-114">VDS Enumerations</span></span>](vds-enumerations.md)
</dt> <dd>

<span data-ttu-id="04e81-115">Descrive le enumerazioni usate con VDS.</span><span class="sxs-lookup"><span data-stu-id="04e81-115">Describes the enumerations used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="04e81-116">Interfacce VDS</span><span class="sxs-lookup"><span data-stu-id="04e81-116">VDS Interfaces</span></span>](vds-interfaces.md)
</dt> <dd>

<span data-ttu-id="04e81-117">Descrive le interfacce VDS e i metodi che espongono.</span><span class="sxs-lookup"><span data-stu-id="04e81-117">Describes VDS interfaces and the methods they expose.</span></span>

</dd> <dt>

[<span data-ttu-id="04e81-118">Strutture VDS</span><span class="sxs-lookup"><span data-stu-id="04e81-118">VDS Structures</span></span>](vds-structures.md)
</dt> <dd>

<span data-ttu-id="04e81-119">Descrive le strutture passate come parametri ai metodi VDS.</span><span class="sxs-lookup"><span data-stu-id="04e81-119">Describes the structures passed as parameters to VDS methods.</span></span>

</dd> <dt>

[<span data-ttu-id="04e81-120">Codici restituiti comuni del servizio dischi virtuali</span><span class="sxs-lookup"><span data-stu-id="04e81-120">Virtual Disk Service Common Return Codes</span></span>](virtual-disk-service-common-return-codes.md)
</dt> <dd>

<span data-ttu-id="04e81-121">Vengono descritti i codici di errore più comuni specifici per VDS.</span><span class="sxs-lookup"><span data-stu-id="04e81-121">Describes the most common error codes that are specific to VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="04e81-122">Glossario servizio dischi virtuali</span><span class="sxs-lookup"><span data-stu-id="04e81-122">Virtual Disk Service Glossary</span></span>](virtual-disk-service-glossary-all.md)
</dt> <dd>

<span data-ttu-id="04e81-123">Glossario dei termini tecnici usati nella documentazione VDS.</span><span class="sxs-lookup"><span data-stu-id="04e81-123">Glossary of technical terms used in VDS documentation.</span></span>

</dd> </dl>

 

 
