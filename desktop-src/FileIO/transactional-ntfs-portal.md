---
description: Transactional NTFS (TxF) consente di eseguire operazioni su file su un volume file system NTFS in una transazione.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: Transactional NTFS (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524925"
---
# <a name="transactional-ntfs-txf"></a><span data-ttu-id="2ee82-103">Transactional NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="2ee82-103">Transactional NTFS (TxF)</span></span>

<span data-ttu-id="2ee82-104">\[Microsoft consiglia vivamente agli sviluppatori di utilizzare metodi alternativi per soddisfare le esigenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2ee82-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="2ee82-105">Molti scenari in cui TxF è stato sviluppato possono essere realizzati attraverso tecniche più semplici e più facilmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="2ee82-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="2ee82-106">Inoltre, è possibile che TxF non sia disponibile nelle versioni future di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2ee82-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="2ee82-107">Per altre informazioni e per le alternative a TxF, vedere [alternative all'uso di Transactional NTFS](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="2ee82-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="2ee82-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="2ee82-108">Purpose</span></span>

<span data-ttu-id="2ee82-109">Transactional NTFS (TxF) consente di eseguire operazioni su file su un volume file system NTFS in una transazione.</span><span class="sxs-lookup"><span data-stu-id="2ee82-109">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span> <span data-ttu-id="2ee82-110">Le transazioni TxF aumentano l'affidabilità dell'applicazione proteggendo l'integrità dei dati tra errori e semplificando lo sviluppo di applicazioni riducendo notevolmente la quantità di codice di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="2ee82-110">TxF transactions increase application reliability by protecting data integrity across failures and simplify application development by greatly reducing the amount of error handling code.</span></span>

<span data-ttu-id="2ee82-111">TxF utilizza il Framework di transazione fornito da [gestione transazioni kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal) .</span><span class="sxs-lookup"><span data-stu-id="2ee82-111">TxF uses the transaction framework provided by the [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span></span> <span data-ttu-id="2ee82-112">In questo modo le operazioni di file TxF possono far parte di una transazione che interessa altre origini dati, ad esempio SQL Server e il registro di sistema transazionale (TxR).</span><span class="sxs-lookup"><span data-stu-id="2ee82-112">This allows TxF file operations to be part of a transaction involving other data sources such as SQL Server and Transacted Registry (TxR).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="2ee82-113">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="2ee82-113">Where applicable</span></span>

<span data-ttu-id="2ee82-114">Un'applicazione può usare TxF per mantenere l'integrità dei dati su disco causati da condizioni di errore impreviste e risolvere gli scenari utente del file System simultanei isolando le modifiche da altri utenti durante le modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="2ee82-114">An application can use TxF to preserve the integrity of data on disk caused by unexpected error conditions and help resolve concurrent file-system user scenarios by isolating your changes from others while the changes are being made.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2ee82-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="2ee82-115">Developer audience</span></span>

<span data-ttu-id="2ee82-116">Prima di utilizzare TxF, è necessario disporre di una conoscenza operativa delle transazioni utilizzando KTM o [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ee82-116">Before using TxF, you should have a working knowledge of transactions using either KTM or [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2ee82-117">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="2ee82-117">Run-time requirements</span></span>

<span data-ttu-id="2ee82-118">TxF è disponibile a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ee82-118">TxF is available starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ee82-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2ee82-119">In this section</span></span>



| <span data-ttu-id="2ee82-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="2ee82-120">Topic</span></span>                                                    | <span data-ttu-id="2ee82-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ee82-121">Description</span></span>                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ee82-122">Informazioni</span><span class="sxs-lookup"><span data-stu-id="2ee82-122">About</span></span>](about-transactional-ntfs.md)<br/>         | <span data-ttu-id="2ee82-123">Informazioni generali sul formato NTFS transazionale.</span><span class="sxs-lookup"><span data-stu-id="2ee82-123">General information about Transactional NTFS.</span></span><br/>                                                   |
| [<span data-ttu-id="2ee82-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2ee82-124">Reference</span></span>](transactional-ntfs-reference.md)<br/> | <span data-ttu-id="2ee82-125">Documentazione per le funzioni, le strutture dei dati, le enumerazioni e altri elementi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="2ee82-125">Documentation for the functions, data structures, enumerations, and other programming elements.</span></span><br/> |



 

 

