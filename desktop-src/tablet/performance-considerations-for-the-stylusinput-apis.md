---
description: Descrizione dei modi per migliorare le prestazioni quando si usano le API (Application Programming Interface) di StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Considerazioni sulle prestazioni per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759806"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a><span data-ttu-id="35340-103">Considerazioni sulle prestazioni per l'API StylusInput</span><span class="sxs-lookup"><span data-stu-id="35340-103">Performance Considerations for the StylusInput API</span></span>

<span data-ttu-id="35340-104">Nell'elenco seguente vengono descritti alcuni modi in cui migliorare le prestazioni delle applicazioni che utilizzano le API StylusInput.</span><span class="sxs-lookup"><span data-stu-id="35340-104">The following list describes some ways in which to improve the performance of applications that use the StylusInput APIs.</span></span>

-   <span data-ttu-id="35340-105">Usare la proprietà [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) per sottoscrivere solo i dati rilevanti per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="35340-105">Use the [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) property to subscribe only to the data that is relevant to your plug-in.</span></span> <span data-ttu-id="35340-106">In questo modo si riduce il numero complessivo di chiamate al metodo eseguite dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) , riducendo inoltre la complessità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="35340-106">This reduces the overall number of method calls the [**RealTimeStylus**](realtimestylus-class.md) object makes and also reduces the complexity of your plug-in.</span></span> <span data-ttu-id="35340-107">L'oggetto **RealTimeStylus** controlla solo la proprietà DataInterest quando viene collegato il plug-in.</span><span class="sxs-lookup"><span data-stu-id="35340-107">The **RealTimeStylus** object only checks the DataInterest property when the plug-in is attached.</span></span>
-   <span data-ttu-id="35340-108">Ridurre al minimo la complessità dei plug-in sincroni. Plug-in sincroni generalmente chiamati dal thread dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e possono contribuire a ritardi nella raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="35340-108">Minimize the complexity of synchronous plug-ins. Synchronous plug-ins generally called by the [**RealTimeStylus**](realtimestylus-class.md) object's thread and may contribute to delays in ink collection.</span></span>
-   <span data-ttu-id="35340-109">Prendere in considerazione la possibilità di rendere il plug-in asincrono.</span><span class="sxs-lookup"><span data-stu-id="35340-109">Consider making your plug-in asynchronous.</span></span> <span data-ttu-id="35340-110">Se il plug-in è complesso ed è necessario aggiungere dati personalizzati alla coda dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) , prendere in considerazione l'uso di un modello **RealTimeStylus** a cascata e l'aggiunta del plug-in alla raccolta di plug-in sincrona dell'oggetto **RealTimeStylus** secondario.</span><span class="sxs-lookup"><span data-stu-id="35340-110">If your plug-in is complex and needs to add custom data to the [**RealTimeStylus**](realtimestylus-class.md) object's queue, consider using a cascaded **RealTimeStylus** model and adding the plug-in to the secondary **RealTimeStylus** object's synchronous plug-in collection.</span></span> <span data-ttu-id="35340-111">Per ulteriori informazioni sul modello **RealTimeStylus** a cascata, vedere [il modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="35340-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

 

 
