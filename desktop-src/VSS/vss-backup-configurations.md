---
description: Esistono diversi tipi di backup supportati convenzionalmente&\# 8212, incrementali, differenziali e completi&\# 8212, che VSS è in grado di riconoscere, oltre a una configurazione di backup peculiare di VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurazioni del backup VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307167"
---
# <a name="vss-backup-configurations"></a><span data-ttu-id="5f0b0-103">Configurazioni del backup VSS</span><span class="sxs-lookup"><span data-stu-id="5f0b0-103">VSS Backup Configurations</span></span>

<span data-ttu-id="5f0b0-104">Sono disponibili diversi tipi di backup supportati convenzionalmente, ovvero incrementali, differenziali e completi, che VSS è in grado di riconoscere, nonché una configurazione di backup peculiare per VSS.</span><span class="sxs-lookup"><span data-stu-id="5f0b0-104">There are a number of conventionally supported backup types—incremental, differential, and full—that VSS is aware of, as well as a backup configuration peculiar to VSS.</span></span>

<span data-ttu-id="5f0b0-105">Quando si definisce una configurazione di backup, un richiedente e i writer in un sistema indicano la modalità di scrittura dei dati in un dispositivo di archiviazione, il modo in cui verrà distribuito il meccanismo di copia shadow e le informazioni da salvare.</span><span class="sxs-lookup"><span data-stu-id="5f0b0-105">In defining a backup configuration, a requester and the writers on a system indicate how data will be written to a storage device, how the shadow copy mechanism will be deployed, and what information needs to be saved.</span></span> <span data-ttu-id="5f0b0-106">L'interazione tra writer e richiedenti è determinata dal tipo di backup che un richiedente vuole eseguire e dai tipi (o schemi) che ciascun writer può supportare:</span><span class="sxs-lookup"><span data-stu-id="5f0b0-106">Interaction between writers and requesters is determined by the type of backup a requester wants to perform and the kinds (or schemas) that each writer can support:</span></span>

-   [<span data-ttu-id="5f0b0-107">Stato backup VSS</span><span class="sxs-lookup"><span data-stu-id="5f0b0-107">VSS Backup State</span></span>](vss-backup-state.md)
-   [<span data-ttu-id="5f0b0-108">Supporto dello schema di backup del writer</span><span class="sxs-lookup"><span data-stu-id="5f0b0-108">Writer Backup Schema Support</span></span>](writer-backup-schema-support.md)
-   [<span data-ttu-id="5f0b0-109">Supporto dello schema a livello di file</span><span class="sxs-lookup"><span data-stu-id="5f0b0-109">File Level Schema Support</span></span>](file-level-schema-support.md)

 

 



