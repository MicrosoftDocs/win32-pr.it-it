---
description: È possibile aggiornare i valori delle proprietà colonne delle istanze della classe di visualizzazione Union. Le modifiche apportate all'istanza della classe di visualizzazione verranno propagate alle istanze della classe di origine che formano la classe di visualizzazione Unione.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Aggiornamento di una visualizzazione Unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130959"
---
# <a name="updating-a-union-view"></a><span data-ttu-id="600b9-104">Aggiornamento di una visualizzazione Unione</span><span class="sxs-lookup"><span data-stu-id="600b9-104">Updating a Union View</span></span>

<span data-ttu-id="600b9-105">È possibile aggiornare i valori delle proprietà colonne delle istanze della classe di visualizzazione Union.</span><span class="sxs-lookup"><span data-stu-id="600b9-105">You can update the values of nonkey properties of union view class instances.</span></span> <span data-ttu-id="600b9-106">Le modifiche apportate all'istanza della classe di visualizzazione verranno propagate alle istanze della classe di origine che formano la classe di visualizzazione Unione.</span><span class="sxs-lookup"><span data-stu-id="600b9-106">The changes you make to the view class instance will be propagated back to the source class instances that form the union view class.</span></span>

<span data-ttu-id="600b9-107">Le restrizioni seguenti si applicano alle modifiche apportate alle istanze della classe di visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="600b9-107">The following restrictions apply to changes to view class instances:</span></span>

-   <span data-ttu-id="600b9-108">Non è possibile creare nuove istanze delle classi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="600b9-108">You cannot create new instances of view classes.</span></span>
-   <span data-ttu-id="600b9-109">Solo le classi Union supportano gli aggiornamenti. le viste join e Association creano istanze di visualizzazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="600b9-109">Only union classes support updates; join and association views create read-only view instances.</span></span>
-   <span data-ttu-id="600b9-110">Il completamento di un aggiornamento varia a seconda che un'istanza di origine sia aggiornabile.</span><span class="sxs-lookup"><span data-stu-id="600b9-110">Success of an update depends on whether a source instance is updateable.</span></span> <span data-ttu-id="600b9-111">Se una proprietà di un'istanza di visualizzazione è mappata a una proprietà di sola lettura di un'istanza di origine, i tentativi di modificare la proprietà di visualizzazione hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="600b9-111">If a view instance property maps to a read-only property of a source instance, attempts to modify the view property fail.</span></span>

 

 



