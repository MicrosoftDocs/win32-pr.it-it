---
description: Funzioni transazionali NTFS (TxF).
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: Funzioni TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758831"
---
# <a name="txf-functions"></a><span data-ttu-id="e41cc-103">Funzioni TxF</span><span class="sxs-lookup"><span data-stu-id="e41cc-103">TxF Functions</span></span>

<span data-ttu-id="e41cc-104">Transactional NTFS (TxF) fornisce le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e41cc-104">Transactional NTFS (TxF) provides the following functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e41cc-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e41cc-105">In this section</span></span>



| <span data-ttu-id="e41cc-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="e41cc-106">Function</span></span>                                                                      | <span data-ttu-id="e41cc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e41cc-107">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e41cc-108">**TxfLogCreateFileReadContext**</span><span class="sxs-lookup"><span data-stu-id="e41cc-108">**TxfLogCreateFileReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | <span data-ttu-id="e41cc-109">Crea un contesto da utilizzare per leggere i record di replica.</span><span class="sxs-lookup"><span data-stu-id="e41cc-109">Creates a context to be used to read replication records.</span></span><br/>                                                         |
| [<span data-ttu-id="e41cc-110">**TxfLogDestroyReadContext**</span><span class="sxs-lookup"><span data-stu-id="e41cc-110">**TxfLogDestroyReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | <span data-ttu-id="e41cc-111">Chiude un contesto di lettura creato dalla funzione [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) .</span><span class="sxs-lookup"><span data-stu-id="e41cc-111">Closes a read context created by the [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) function.</span></span><br/> |
| [<span data-ttu-id="e41cc-112">**TxfLogReadRecords**</span><span class="sxs-lookup"><span data-stu-id="e41cc-112">**TxfLogReadRecords**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | <span data-ttu-id="e41cc-113">Legge i record di rollforward dal log.</span><span class="sxs-lookup"><span data-stu-id="e41cc-113">Reads the redo records from the log.</span></span><br/>                                                                              |



 

 

 




