---
title: Immissione dello stato passivo
description: Immissione dello stato passivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856781"
---
# <a name="entering-the-passive-state"></a><span data-ttu-id="18603-103">Immissione dello stato passivo</span><span class="sxs-lookup"><span data-stu-id="18603-103">Entering the Passive State</span></span>

<span data-ttu-id="18603-104">La chiusura degli oggetti forza un oggetto incorporato o collegato nello stato passivo.</span><span class="sxs-lookup"><span data-stu-id="18603-104">Object closure forces an embedded or linked object into the passive state.</span></span> <span data-ttu-id="18603-105">Viene in genere avviato dall'interfaccia utente dell'applicazione server OLE, ad esempio quando l'utente seleziona il comando file Close.</span><span class="sxs-lookup"><span data-stu-id="18603-105">It is typically initiated from the OLE server application's user interface, such as when the user selects the File Close command.</span></span> <span data-ttu-id="18603-106">In questo caso, l'applicazione server OLE invia una notifica al contenitore, che rilascia il conteggio dei riferimenti nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="18603-106">In this case, the OLE server application notifies the container, which releases its reference count on the object.</span></span> <span data-ttu-id="18603-107">Quando tutti i riferimenti all'oggetto sono stati rilasciati, l'oggetto può essere liberato.</span><span class="sxs-lookup"><span data-stu-id="18603-107">When all references to the object have been released, the object can be freed.</span></span> <span data-ttu-id="18603-108">Quando tutti gli oggetti sono stati liberati, l'applicazione server OLE può terminare in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="18603-108">When all objects have been freed, the OLE server application can safely terminate.</span></span>

<span data-ttu-id="18603-109">Un'applicazione contenitore può anche avviare la chiusura degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="18603-109">A container application can also initiate object closure.</span></span> <span data-ttu-id="18603-110">Per chiudere un oggetto, il contenitore rilascia il conteggio dei riferimenti dopo aver completato un'operazione di salvataggio facoltativa.</span><span class="sxs-lookup"><span data-stu-id="18603-110">To close an object, the container releases its reference count after completing an optional save operation.</span></span> <span data-ttu-id="18603-111">È possibile progettare contenitori per rilasciare oggetti quando vengono disattivati dopo una sessione di attivazione sul posto, consentendo all'utente di fare clic all'esterno dell'oggetto senza perdere la sessione di modifica attiva.</span><span class="sxs-lookup"><span data-stu-id="18603-111">You can design containers to release objects when they are deactivating after an in-place activation session, allowing the user to click outside the object without losing the active editing session.</span></span>

 

 




