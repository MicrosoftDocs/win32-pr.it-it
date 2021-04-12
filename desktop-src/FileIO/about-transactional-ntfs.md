---
description: Transactional NTFS (TxF) integra le transazioni nel file system NTFS, che consente agli sviluppatori e agli amministratori di applicazioni di gestire correttamente gli errori e di mantenere l'integrità dei dati.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Informazioni su Transactional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343641"
---
# <a name="about-transactional-ntfs"></a><span data-ttu-id="ed8a3-103">Informazioni su Transactional NTFS</span><span class="sxs-lookup"><span data-stu-id="ed8a3-103">About Transactional NTFS</span></span>

<span data-ttu-id="ed8a3-104">\[Microsoft consiglia vivamente agli sviluppatori di utilizzare metodi alternativi per soddisfare le esigenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="ed8a3-105">Molti scenari in cui TxF è stato sviluppato possono essere realizzati attraverso tecniche più semplici e più facilmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="ed8a3-106">Inoltre, è possibile che TxF non sia disponibile nelle versioni future di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="ed8a3-107">Per altre informazioni e per le alternative a TxF, vedere [alternative all'uso di Transactional NTFS](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="ed8a3-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

<span data-ttu-id="ed8a3-108">Transactional NTFS (TxF) integra le transazioni nel file system NTFS, che consente agli sviluppatori e agli amministratori di applicazioni di gestire correttamente gli errori e di mantenere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-108">Transactional NTFS (TxF) integrates transactions into the NTFS file system, which makes it easier for application developers and administrators to gracefully handle errors and preserve data integrity.</span></span>

<span data-ttu-id="ed8a3-109">TxF può partecipare alle transazioni distribuite coordinate da [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) , che consente di usare TXF per gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed8a3-109">TxF can participate in distributed transactions that the [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordinates, which allows you to use TxF for the following:</span></span>

-   <span data-ttu-id="ed8a3-110">Transazioni che si estendono su più archivi dati, ad esempio una singola transazione per le operazioni di file e SQL</span><span class="sxs-lookup"><span data-stu-id="ed8a3-110">Transactions that span multiple data stores, for example, a single transaction for file and SQL operations</span></span>
-   <span data-ttu-id="ed8a3-111">Transazioni che si estendono su più computer, ad esempio una singola transazione per gli aggiornamenti di file in più computer</span><span class="sxs-lookup"><span data-stu-id="ed8a3-111">Transactions that span multiple computers, for example, a single transaction for file updates on multiple computers</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ed8a3-112">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ed8a3-112">In this section</span></span>



| <span data-ttu-id="ed8a3-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="ed8a3-113">Topic</span></span>                                                                                                                 | <span data-ttu-id="ed8a3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed8a3-114">Description</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed8a3-115">Quando utilizzare Transactional NTFS</span><span class="sxs-lookup"><span data-stu-id="ed8a3-115">When to Use Transactional NTFS</span></span>](when-to-use-transactional-ntfs.md)<br/>                                       | <span data-ttu-id="ed8a3-116">Utilizzare Transactional NTFS per mantenere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-116">Use Transactional NTFS to maintain data integrity.</span></span><br/>                                                                        |
| [<span data-ttu-id="ed8a3-117">Distribuzione di Transactional NTFS</span><span class="sxs-lookup"><span data-stu-id="ed8a3-117">Deploying Transactional NTFS</span></span>](deploying-transactional-ntfs.md)<br/>                                           | <span data-ttu-id="ed8a3-118">Controllo della memorizzazione nella cache in Transactional NTFS.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-118">Caching control in Transactional NTFS.</span></span><br/>                                                                                    |
| [<span data-ttu-id="ed8a3-119">Come utilizzare Transactional NTFS</span><span class="sxs-lookup"><span data-stu-id="ed8a3-119">How to Use Transactional NTFS</span></span>](how-to-use-transactional-ntfs.md)<br/>                                         | <span data-ttu-id="ed8a3-120">Gestione degli handle di file transazionali in NTFS transazionale.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-120">Managing transacted file handles in Transactional NTFS.</span></span><br/>                                                                   |
| [<span data-ttu-id="ed8a3-121">Concetti di base di TxF</span><span class="sxs-lookup"><span data-stu-id="ed8a3-121">Basic TxF Concepts</span></span>](txf-basic-concepts.md)<br/>                                                               | <span data-ttu-id="ed8a3-122">Descrive la coerenza Read Committed, l'isolamento Read committed e i concetti di blocco transazionale in Transactional NTFS.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-122">Describes read-committed consistency, read-committed isolation, and transactional locking concepts in Transactional NTFS.</span></span><br/> |
| [<span data-ttu-id="ed8a3-123">Considerazioni sulla programmazione per Transactional NTFS</span><span class="sxs-lookup"><span data-stu-id="ed8a3-123">Programming Considerations for Transactional NTFS</span></span>](programming-considerations-for-transacted-fileio-.md)<br/> | <span data-ttu-id="ed8a3-124">Vengono descritte le varie considerazioni di programmazione per Transactional NTFS.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-124">Describes various programming considerations for Transactional NTFS.</span></span><br/>                                                      |
| [<span data-ttu-id="ed8a3-125">Considerazioni sulle prestazioni per la funzionalità NTFS transazionale</span><span class="sxs-lookup"><span data-stu-id="ed8a3-125">Performance Considerations for Transactional NTFS</span></span>](performance-considerations-for-transactional-ntfs.md)<br/> | <span data-ttu-id="ed8a3-126">Suggerimenti per le transazioni file system ottimali.</span><span class="sxs-lookup"><span data-stu-id="ed8a3-126">Recommendations for optimal file system transactions.</span></span><br/>                                                                     |



 

 

