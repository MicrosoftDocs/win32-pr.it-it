---
description: L'API di migrazione Hyper-V definisce gli elementi di programmazione seguenti.
ms.assetid: E1FE7351-2F14-4C8F-AF5C-9009CC61CE22
title: Informazioni di riferimento sull'API di migrazione Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a05bc976cf1722aba558eeca9c7b04cdf7287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309519"
---
# <a name="hyper-v-migration-api-reference"></a><span data-ttu-id="6565b-103">Informazioni di riferimento sull'API di migrazione Hyper-V</span><span class="sxs-lookup"><span data-stu-id="6565b-103">Hyper-V migration API reference</span></span>

<span data-ttu-id="6565b-104">L'API di migrazione Hyper-V definisce gli elementi di programmazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="6565b-104">The Hyper-V migration API defines the following programming elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6565b-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6565b-105">In this section</span></span>



| <span data-ttu-id="6565b-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="6565b-106">Topic</span></span>                                                                                                                                | <span data-ttu-id="6565b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6565b-107">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6565b-108">**\_MigrationJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="6565b-108">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)<br/>                                                                           | <span data-ttu-id="6565b-109">Questa classe rappresenta un processo dell'operazione di migrazione creato per la migrazione dell'archiviazione o del sistema virtuale da parte del servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="6565b-109">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span><br/>                                                 |
| [<span data-ttu-id="6565b-110">**\_VirtualSystemMigrationCapabilities MSVM**</span><span class="sxs-lookup"><span data-stu-id="6565b-110">**Msvm\_VirtualSystemMigrationCapabilities**</span></span>](msvm-virtualsystemmigrationcapabilities.md)<br/>                               | <span data-ttu-id="6565b-111">Definisce i mezzi mediante i quali un client può individuare i metodi forniti dal servizio di migrazione e un intervallo valido di dati dell'impostazione della migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="6565b-111">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span><br/>                                |
| [<span data-ttu-id="6565b-112">**\_VirtualSystemMigrationNetworkSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="6565b-112">**Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>](msvm-virtualsystemmigrationnetworksettingdata.md)<br/>                   | <span data-ttu-id="6565b-113">Rappresenta la rete in cui il servizio migrazione del sistema virtuale è in ascolto della migrazione del sistema virtuale in ingresso.</span><span class="sxs-lookup"><span data-stu-id="6565b-113">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span><br/>                                                                 |
| [<span data-ttu-id="6565b-114">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="6565b-114">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)<br/>                                         | <span data-ttu-id="6565b-115">Rappresenta il servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="6565b-115">Represents the virtual system migration service.</span></span> <span data-ttu-id="6565b-116">Viene utilizzato per la migrazione di un sistema virtuale o per la migrazione dell'archiviazione di un sistema virtuale da una piattaforma di virtualizzazione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="6565b-116">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span><br/> |
| [<span data-ttu-id="6565b-117">**\_VirtualSystemMigrationServiceSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="6565b-117">**Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>](msvm-virtualsystemmigrationservicesettingdata.md)<br/>                   | <span data-ttu-id="6565b-118">Rappresenta le impostazioni per il servizio migrazione del sistema virtuale in un host.</span><span class="sxs-lookup"><span data-stu-id="6565b-118">Represents the settings for the virtual system migration service on a host.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="6565b-119">**\_VirtualSystemMigrationServiceSettingDataComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="6565b-119">**Msvm\_VirtualSystemMigrationServiceSettingDataComponent**</span></span>](msvm-virtualsystemmigrationservicesettingdatacomponent.md)<br/> | <span data-ttu-id="6565b-120">Associazione utilizzata per rappresentare le impostazioni della rete di migrazione del sistema virtuale del servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="6565b-120">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span><br/>                                                                      |
| [<span data-ttu-id="6565b-121">**\_VirtualSystemMigrationSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="6565b-121">**Msvm\_VirtualSystemMigrationSettingData**</span></span>](msvm-virtualsystemmigrationsettingdata.md)<br/>                                 | <span data-ttu-id="6565b-122">Rappresenta le impostazioni di migrazione per la migrazione di un sistema virtuale e dello spazio di archiviazione collegato a un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="6565b-122">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span><br/>                                                                           |



 

 

 




