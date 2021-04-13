---
title: Valori restituiti SYSMON
description: Di seguito è riportato un elenco dei valori restituiti di monitoraggio di sistema definiti in Smonmsg. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399440"
---
# <a name="sysmon-return-values"></a><span data-ttu-id="7d9ba-103">Valori restituiti SYSMON</span><span class="sxs-lookup"><span data-stu-id="7d9ba-103">SYSMON Return Values</span></span>

<span data-ttu-id="7d9ba-104">Di seguito è riportato un elenco dei valori restituiti di monitoraggio di sistema definiti in Smonmsg. h.</span><span class="sxs-lookup"><span data-stu-id="7d9ba-104">The following is a list of the System Monitor return values that are defined in Smonmsg.h.</span></span>



| <span data-ttu-id="7d9ba-105">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d9ba-105">Return value</span></span>                                       | <span data-ttu-id="7d9ba-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d9ba-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9ba-107">\_ \_ Percorso contatore DUPL stato smon \_ \_ (0xC0001388)</span><span class="sxs-lookup"><span data-stu-id="7d9ba-107">SMON\_STATUS\_DUPL\_COUNTER\_PATH (0xC0001388)</span></span>     | <span data-ttu-id="7d9ba-108">La raccolta di contatori contiene già il contatore specificato.</span><span class="sxs-lookup"><span data-stu-id="7d9ba-108">The counter collection already contains the specified counter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="7d9ba-109">\_Stato smon \_ nessun \_ \_ oggetto Sysmon (0xC0001389)</span><span class="sxs-lookup"><span data-stu-id="7d9ba-109">SMON\_STATUS\_NO\_SYSMON\_OBJECT (0xC0001389)</span></span>      | <span data-ttu-id="7d9ba-110">Le impostazioni non contengono alcun oggetto HTML di monitoraggio di sistema completo.</span><span class="sxs-lookup"><span data-stu-id="7d9ba-110">The settings do not contain any complete System Monitor HTML objects.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="7d9ba-111">\_Stato smon \_ insufficiente per \_ alcuni \_ esempi (0xC000138A)</span><span class="sxs-lookup"><span data-stu-id="7d9ba-111">SMON\_STATUS\_TOO\_FEW\_SAMPLES (0xC000138A)</span></span>       | <span data-ttu-id="7d9ba-112">Il file di log specificato contiene meno di due campioni di dati.</span><span class="sxs-lookup"><span data-stu-id="7d9ba-112">The specified log file contains fewer than two data samples.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="7d9ba-113">\_ \_ Limite dimensioni file di registro stato smon \_ \_ \_ (0xC000138B)</span><span class="sxs-lookup"><span data-stu-id="7d9ba-113">SMON\_STATUS\_LOG\_FILE\_SIZE\_LIMIT (0xC000138B)</span></span>  | <span data-ttu-id="7d9ba-114">Il file di log specificato supera i limiti di dimensioni del controllo di monitoraggio di sistema.</span><span class="sxs-lookup"><span data-stu-id="7d9ba-114">The specified log file exceeds the size limits of the System Monitor control.</span></span> <span data-ttu-id="7d9ba-115">Se è attualmente selezionato un file di log, selezionare l'attività corrente come origine dati per scaricare il file di log corrente, quindi selezionare nuovamente il file di log specificato.</span><span class="sxs-lookup"><span data-stu-id="7d9ba-115">If a log file is currently selected, select current activity as the data source in order to unload the current log file, then reselect the specified log file.</span></span> |
| <span data-ttu-id="7d9ba-116">\_ \_ Origine dati file di registro stato smon \_ \_ \_ (0xC000138C)</span><span class="sxs-lookup"><span data-stu-id="7d9ba-116">SMON\_STATUS\_LOG\_FILE\_DATA\_SOURCE (0xC000138C)</span></span> | <span data-ttu-id="7d9ba-117">Per aggiungere un nuovo file di log all'origine dati, è necessario modificare il tipo di origine dati in un tipo diverso da sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="7d9ba-117">To add a new log file to the data source, the data source type must be changed to a type other than sysmonLogFiles.</span></span>                                                                                                                          |
| <span data-ttu-id="7d9ba-118">SMON \_ stato \_ DUPL \_ \_ percorso file di registro \_ (0xC000138D)</span><span class="sxs-lookup"><span data-stu-id="7d9ba-118">SMON\_STATUS\_DUPL\_LOG\_FILE\_PATH (0xC000138D)</span></span>   | <span data-ttu-id="7d9ba-119">La raccolta di file di log contiene già il file di log specificato.</span><span class="sxs-lookup"><span data-stu-id="7d9ba-119">The log file collection already contains the specified log file.</span></span>                                                                                                                                                                             |



 

<span data-ttu-id="7d9ba-120">Per una descrizione dei valori restituiti aggiuntivi restituiti da monitoraggio di sistema, vedere codici di errore di [sistema](/windows/desktop/Debug/system-error-codes) e codici di [errore dell'helper dati sulle prestazioni](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span><span class="sxs-lookup"><span data-stu-id="7d9ba-120">For a description of additional return values returned by System Monitor, see [System Error Codes](/windows/desktop/Debug/system-error-codes) and [Performance Data Helper Error Codes](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span></span>

 

 