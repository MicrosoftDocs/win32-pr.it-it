---
description: Creazione di oggetti BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Creazione di oggetti BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304831"
---
# <a name="creating-byot-objects"></a><span data-ttu-id="113cd-103">Creazione di oggetti BYOT</span><span class="sxs-lookup"><span data-stu-id="113cd-103">Creating BYOT Objects</span></span>

<span data-ttu-id="113cd-104">Un nuovo oggetto BYOT crea oggetti con transazioni manuali.</span><span class="sxs-lookup"><span data-stu-id="113cd-104">A new BYOT object creates objects with manual transactions.</span></span> <span data-ttu-id="113cd-105">Le due interfacce, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), hanno un solo metodo, **CreateInstance**, che accettano rispettivamente un puntatore all'interfaccia **ITransaction** e un URL del suggerimento.</span><span class="sxs-lookup"><span data-stu-id="113cd-105">The two interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) and [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), have a single method, **CreateInstance**, which take an **ITransaction** interface pointer and TIP URL, respectively.</span></span> <span data-ttu-id="113cd-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) restituisce un puntatore di interfaccia all'oggetto appena creato, che viene integrato nella transazione specificata.</span><span class="sxs-lookup"><span data-stu-id="113cd-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) returns an interface pointer to the newly created object, which is enlisted within the specified transaction.</span></span>

<span data-ttu-id="113cd-107">Quando viene rilasciato un oggetto con una transazione manuale, COM+ non tenta di eseguire il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="113cd-107">When an object with a manual transaction is released, COM+ does not attempt to commit the transaction.</span></span> <span data-ttu-id="113cd-108">La transazione viene controllata in modo esplicito dal gestore delle transazioni esterno che ha distribuito la transazione in cui è stato creato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="113cd-108">The transaction is controlled explicitly by the external transaction manager that dispensed the transaction under which this object had been created.</span></span>

> [!Note]  
> <span data-ttu-id="113cd-109">È necessario importare l'oggetto BYOT. ByotServerEx in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="113cd-109">The Byot.ByotServerEx object needs to be imported into a COM+ application.</span></span>

 

 

 



