---
title: Flag di priorità
description: Il flag Priority apre un oggetto di archiviazione in modalità Priority.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Flag di priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045397"
---
# <a name="priority-flags"></a><span data-ttu-id="441ab-104">Flag di priorità</span><span class="sxs-lookup"><span data-stu-id="441ab-104">Priority Flags</span></span>

<span data-ttu-id="441ab-105">Il flag Priority apre un oggetto di archiviazione in modalità Priority.</span><span class="sxs-lookup"><span data-stu-id="441ab-105">The priority flag opens a storage object in priority mode.</span></span> <span data-ttu-id="441ab-106">Quando viene aperto un oggetto, un'applicazione funziona in genere da una copia snapshot, perché anche altre applicazioni possono utilizzare l'oggetto contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="441ab-106">When it opens an object, an application usually works from a snapshot copy because other applications may also be using the object at the same time.</span></span> <span data-ttu-id="441ab-107">Quando si apre un oggetto di archiviazione in modalità di priorità, l'applicazione dispone tuttavia dei diritti esclusivi per eseguire il commit delle modifiche apportate all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="441ab-107">When opening a storage object in priority mode, however, the application has exclusive rights to commit changes to the object.</span></span>

<span data-ttu-id="441ab-108">La modalità di priorità consente a un'applicazione di leggere alcuni flussi dallo spazio di archiviazione prima di aprire l'oggetto in una modalità che richiederebbe al sistema di creare una copia snapshot.</span><span class="sxs-lookup"><span data-stu-id="441ab-108">Priority mode enables an application to read some streams from storage before opening the object in a mode that would require the system to make a snapshot copy.</span></span> <span data-ttu-id="441ab-109">Poiché l'applicazione dispone di accesso esclusivo, non è necessario creare una copia snapshot dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="441ab-109">Because the application has exclusive access, it does not have to make a snapshot copy of the object.</span></span> <span data-ttu-id="441ab-110">Quando l'applicazione apre successivamente l'oggetto in una modalità in cui è necessaria una copia snapshot, l'applicazione può escludere i flussi che ha già letto dallo snapshot, riducendo così il sovraccarico di apertura dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="441ab-110">When the application subsequently opens the object in a mode where a snapshot copy is required, the application can exclude the streams it has already read from the snapshot, thereby reducing the overhead of opening the object.</span></span>

<span data-ttu-id="441ab-111">Poiché altre applicazioni non possono eseguire il commit delle modifiche in un oggetto mentre è aperto in modalità di priorità, le applicazioni devono tenere l'oggetto in tale modalità per il minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="441ab-111">Because other applications cannot commit changes to an object while it is open in priority mode, applications should keep the object in that mode for as short a time as possible.</span></span>

 

 




