---
description: 'Altre informazioni su: informazioni sul motore di archiviazione estendibile'
title: Informazioni sul motore di archiviazione estendibile
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966418"
---
# <a name="about-extensible-storage-engine"></a><span data-ttu-id="c5574-103">Informazioni sul motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="c5574-103">About Extensible Storage Engine</span></span>


<span data-ttu-id="c5574-104">_**Si applica a:** Exchange Server 2013 | Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c5574-104">_**Applies to:** Exchange Server 2013 | Windows | Windows Server_</span></span>

## <a name="about-extensible-storage-engine"></a><span data-ttu-id="c5574-105">Informazioni sul motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="c5574-105">About Extensible Storage Engine</span></span>

<span data-ttu-id="c5574-106">Extensible Storage Engine (ESE) è un motore di database che archivia le informazioni in una sequenza logica.</span><span class="sxs-lookup"><span data-stu-id="c5574-106">The extensible storage engine (ESE) is a database engine that stores information in a logical sequence.</span></span> <span data-ttu-id="c5574-107">Le informazioni possono essere recuperate in sequenza oppure accedendo agli indici definiti.</span><span class="sxs-lookup"><span data-stu-id="c5574-107">Information can be retrieved either sequentially or by accessing defined indices.</span></span> <span data-ttu-id="c5574-108">Gli aggiornamenti al database vengono implementati con una transazione per garantire operazioni protette.</span><span class="sxs-lookup"><span data-stu-id="c5574-108">Updates to the database are implemented with a transaction in order to ensure secure operations.</span></span> <span data-ttu-id="c5574-109">ESE consente l'accesso simultaneo a più database, inclusi i database dei file di log delle transazioni che possono essere utilizzati per il ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="c5574-109">ESE enables simultaneous access to multiple databases, including transaction-log file databases that can be used for system recovery.</span></span> <span data-ttu-id="c5574-110">ESE è scalabile per applicazioni di grandi dimensioni o piccole.</span><span class="sxs-lookup"><span data-stu-id="c5574-110">ESE is scalable to large or small applications.</span></span> <span data-ttu-id="c5574-111">Le funzionalità seguenti sono disponibili con l'Application Programming Interface ESE (API):</span><span class="sxs-lookup"><span data-stu-id="c5574-111">The following features are available with the ESE application programming interface (API):</span></span>

  - <span data-ttu-id="c5574-112">Backup e ripristino: un'applicazione può eseguire copie coerenti dello stato dei dati mentre è in linea e modifica attivamente lo stato dei dati.</span><span class="sxs-lookup"><span data-stu-id="c5574-112">Backup and restore: An application can make consistent copies of the data state while it is on-line and actively modifying data state.</span></span>

  - <span data-ttu-id="c5574-113">Navigazione del cursore: l'applicazione può spostarsi con il cursore per accedere ai dati in sequenza o usando gli indici.</span><span class="sxs-lookup"><span data-stu-id="c5574-113">Cursor Navigation: The application can navigate with the cursor to access data either sequentially or by using indices.</span></span>

  - <span data-ttu-id="c5574-114">Database: raccolta di tabelle di cui viene eseguito il backup e il ripristino come singola unità.</span><span class="sxs-lookup"><span data-stu-id="c5574-114">Database: A collection of tables that are backed up and restored as a single unit.</span></span>

  - <span data-ttu-id="c5574-115">Registrazione e ripristino di arresto anomalo: l'API ESE garantisce che la coerenza dei dati definita dall'applicazione venga rispettata anche in caso di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="c5574-115">Logging and crash recovery: The ESE API ensures that application-defined data consistency is honored even in the event of a system crash.</span></span>

  - <span data-ttu-id="c5574-116">Tables: la struttura di base del database ESE usato per archiviare i dati.</span><span class="sxs-lookup"><span data-stu-id="c5574-116">Tables: The fundamental structure of the ESE database that is used to store data.</span></span>

  - <span data-ttu-id="c5574-117">Transazione: il motore di database ESE fornisce transazioni ACID (Atomic coerenti) atomiche che consentono alle applicazioni di recuperare i dati solo da Stati di dati affidabili e di mantenere la coerenza dei dati in caso di interruzione imprevista di un processo o di arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="c5574-117">Transaction: The ESE database engine provides Atomic Consistent Isolated Durable (ACID) transactions that allow applications to retrieve data only from reliable data states and maintains data consistency in the event of an unexpected process termination or system shutdown.</span></span>

  - <span data-ttu-id="c5574-118">Scalabile: l'applicazione può creare database di dimensioni pari a 100 GB o fino a 1 MB.</span><span class="sxs-lookup"><span data-stu-id="c5574-118">Scalable: The application can create databases as large as 100 GB or as small as 1MB.</span></span>

