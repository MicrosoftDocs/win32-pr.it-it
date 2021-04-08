---
title: BITS e ripristino del sistema
description: Non tutte le versioni di BITS utilizzano lo stesso formato per archiviare i processi.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044254"
---
# <a name="bits-and-system-restore"></a><span data-ttu-id="3dc0a-103">BITS e ripristino del sistema</span><span class="sxs-lookup"><span data-stu-id="3dc0a-103">BITS and System Restore</span></span>

<span data-ttu-id="3dc0a-104">Non tutte le versioni di BITS utilizzano lo stesso formato per archiviare i processi.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-104">Not all versions of BITS use the same format to store jobs.</span></span> <span data-ttu-id="3dc0a-105">Se il computer viene restituito a un punto di ripristino prima di un aggiornamento BITS, la versione precedente di BITS potrebbe non essere in grado di leggere le informazioni sul processo corrente.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-105">If you return the computer to a restore point prior to a BITS upgrade, the old version of BITS may not be able to read the current job information.</span></span> <span data-ttu-id="3dc0a-106">In tal caso, BITS eliminerà l'elenco dei processi e creerà un nuovo elenco di processi vuoti.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-106">If this happens, BITS will delete the jobs list and create a new empty jobs list.</span></span> <span data-ttu-id="3dc0a-107">Di conseguenza, i file temporanei associati all'elenco dei processi precedenti non vengono eliminati; per recuperare lo spazio su disco, è necessario eliminare i file manualmente.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-107">As a result, the temporary files associated with the previous jobs list are not cleaned up; to reclaim the disk space, you must delete the files manually.</span></span>

<span data-ttu-id="3dc0a-108">Gli utenti che hanno familiarità con la riga di comando di Windows possono evitare questo problema usando lo [strumento Bitsadmin](bitsadmin-tool.md) per cancellare l'elenco dei processi BITS prima di eseguire Ripristino configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-108">Users familiar with the Windows command line can avoid this problem by using the [BITSAdmin tool](bitsadmin-tool.md) to clear the BITS jobs list before running System Restore.</span></span> <span data-ttu-id="3dc0a-109">Per cancellare l'elenco dei processi BITS, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="3dc0a-109">To clear the BITS jobs list, run the following command:</span></span>

<span data-ttu-id="3dc0a-110">**Bitsadmin/reset/allusers**</span><span class="sxs-lookup"><span data-stu-id="3dc0a-110">**bitsadmin /reset /allusers**</span></span>

<span data-ttu-id="3dc0a-111">Si noti che per eseguire questo comando è necessario disporre dei privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-111">Note that you must have administrator privileges to run this command.</span></span>

 

 




