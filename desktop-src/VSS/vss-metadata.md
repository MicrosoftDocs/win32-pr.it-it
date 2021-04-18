---
description: Sia i writer che i richiedenti gestiscono le informazioni necessarie per un'operazione di backup o ripristino nei propri documenti di metadati.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Metadati VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307159"
---
# <a name="vss-metadata"></a><span data-ttu-id="0fae3-103">Metadati VSS</span><span class="sxs-lookup"><span data-stu-id="0fae3-103">VSS Metadata</span></span>

<span data-ttu-id="0fae3-104">Sia i writer che i richiedenti gestiscono le informazioni necessarie per un'operazione di backup o ripristino nei propri documenti di metadati.</span><span class="sxs-lookup"><span data-stu-id="0fae3-104">Both writers and requesters maintain information necessary to a backup or restore operation in their own metadata documents.</span></span>

<span data-ttu-id="0fae3-105">Questi documenti, il [*documento di metadati del writer*](vssgloss-w.md) e il [*documento sui componenti di backup*](vssgloss-b.md), vengono usati rispettivamente come base per la comunicazione e il coordinamento del writer e del richiedente durante le attività di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="0fae3-105">These documents, the [*Writer Metadata Document*](vssgloss-w.md) and the [*Backup Components Document*](vssgloss-b.md), respectively, are used as the basis for writer and requester communication and coordination during backup and restore activities.</span></span>

<span data-ttu-id="0fae3-106">I metadati sono rappresentati in formato XML utilizzando uno schema proprietario.</span><span class="sxs-lookup"><span data-stu-id="0fae3-106">The metadata is represented in XML format using a proprietary schema.</span></span> <span data-ttu-id="0fae3-107">I metadati possono essere copiati su disco, nastro o qualsiasi altro dispositivo di archiviazione di massa.</span><span class="sxs-lookup"><span data-stu-id="0fae3-107">Metadata can be copied to disk, tape, or any other mass storage device.</span></span> <span data-ttu-id="0fae3-108">Deve essere sempre salvato nei supporti di backup durante un'operazione di backup e deve essere recuperato dal supporto nel corso di un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0fae3-108">It should always be saved to the backup media during a backup operation, and will need to be retrieved from that media in the course of a restore operation.</span></span>

<span data-ttu-id="0fae3-109">**Attenzione:** I dettagli specifici del formato e dello schema sono solo per uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="0fae3-109">**Caution:** The specific details of the format and schema are for system use only.</span></span> <span data-ttu-id="0fae3-110">Gli sviluppatori non devono tentare di modificare o utilizzare direttamente la rappresentazione XML dei metadati.</span><span class="sxs-lookup"><span data-stu-id="0fae3-110">Developers should not attempt to modify or directly use the XML representation of the metadata.</span></span>

<span data-ttu-id="0fae3-111">Ai writer e ai richiedenti viene offerta un'ampia gamma di metodi di query e set per accedere e modificare i componenti di backup e i documenti di metadati del writer:</span><span class="sxs-lookup"><span data-stu-id="0fae3-111">Writers and requesters are provided with a variety of query and set methods to access and modify the Backup Components and Writer Metadata documents:</span></span>

-   [<span data-ttu-id="0fae3-112">Utilizzo del documento di metadati del writer</span><span class="sxs-lookup"><span data-stu-id="0fae3-112">Working with the Writer Metadata Document</span></span>](working-with-the-writer-metadata-document.md)
-   [<span data-ttu-id="0fae3-113">Utilizzo del documento componenti di backup</span><span class="sxs-lookup"><span data-stu-id="0fae3-113">Working with the Backup Components Document</span></span>](working-with-the-backup-components-document.md)
-   [<span data-ttu-id="0fae3-114">Componenti dei metadati VSS</span><span class="sxs-lookup"><span data-stu-id="0fae3-114">VSS Metadata Components</span></span>](vss-metadata-components.md)

 

 



