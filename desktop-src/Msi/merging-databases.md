---
description: È possibile utilizzare il programma di installazione per aggiungere le informazioni di un database in un altro database eseguendo un'operazione di merge.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Unione di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968097"
---
# <a name="merging-databases"></a><span data-ttu-id="792ce-103">Unione di database</span><span class="sxs-lookup"><span data-stu-id="792ce-103">Merging Databases</span></span>

<span data-ttu-id="792ce-104">È possibile utilizzare il programma di installazione per aggiungere le informazioni di un database in un altro database eseguendo un'operazione di merge.</span><span class="sxs-lookup"><span data-stu-id="792ce-104">You can use the installer to add the information in one database into another database by performing a merge.</span></span> <span data-ttu-id="792ce-105">Le [unioni e le trasformazioni](merges-and-transforms.md) operano su un intero database e un'Unione combina due database in uno.</span><span class="sxs-lookup"><span data-stu-id="792ce-105">[Merges and Transforms](merges-and-transforms.md) operate on an entire database, and a merge combines two databases into one.</span></span> <span data-ttu-id="792ce-106">Le unioni sono utili per i team di sviluppo perché consentono al database di installazione di applicazioni di grandi dimensioni di essere divise in parti più piccole e quindi ricombinate nel database di installazione completo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="792ce-106">Merges are useful to development teams because they allow the installation database of large application to be divided into smaller parts and then recombined into the complete installation database later.</span></span>

<span data-ttu-id="792ce-107">**Per unire più database di componenti in un unico database completo**</span><span class="sxs-lookup"><span data-stu-id="792ce-107">**To merge several component databases into a single complete database**</span></span>

1.  <span data-ttu-id="792ce-108">Sviluppare separatamente i database dei componenti parziali.</span><span class="sxs-lookup"><span data-stu-id="792ce-108">Develop the partial component databases separately.</span></span>
2.  <span data-ttu-id="792ce-109">Unire ogni database componente nel database principale del prodotto chiamando la funzione [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .</span><span class="sxs-lookup"><span data-stu-id="792ce-109">Merge each component database into the main product database by calling the [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function.</span></span>

 

 



