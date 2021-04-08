---
title: GUID di coerenza
description: I GUID di coerenza sono una strategia di rilevamento che consente a un'applicazione di rilevare gli aggiornamenti parziali.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044008"
---
# <a name="consistency-guids"></a><span data-ttu-id="e914a-103">GUID di coerenza</span><span class="sxs-lookup"><span data-stu-id="e914a-103">Consistency GUIDs</span></span>

<span data-ttu-id="e914a-104">I GUID di coerenza sono una strategia di rilevamento che consente a un'applicazione di rilevare gli aggiornamenti parziali.</span><span class="sxs-lookup"><span data-stu-id="e914a-104">Consistency GUIDs are a detection strategy that allows an application to detect partial updates.</span></span> <span data-ttu-id="e914a-105">Un GUID di coerenza (identificatore univoco globale) viene applicato a ogni oggetto in un set correlato.</span><span class="sxs-lookup"><span data-stu-id="e914a-105">A consistency GUID (Globally Unique IDentifier) is applied to each object in a related set.</span></span> <span data-ttu-id="e914a-106">Nell'implementazione, un'applicazione di origine genera un nuovo GUID e lo applica a ogni oggetto aggiornato nel set di oggetti correlati.</span><span class="sxs-lookup"><span data-stu-id="e914a-106">In implementation, a source application generates a new GUID and applies it to each object it updates in the set of related objects.</span></span> <span data-ttu-id="e914a-107">Applica quindi il nuovo GUID al resto degli oggetti nel set e termina applicando il nuovo GUID all'oggetto "Master".</span><span class="sxs-lookup"><span data-stu-id="e914a-107">It then applies the new GUID to the rest of the objects in the set, and finishes by applying the new GUID to the "master" object.</span></span> <span data-ttu-id="e914a-108">In genere, l'oggetto "Master" sarà un contenitore padre degli altri oggetti nel set.</span><span class="sxs-lookup"><span data-stu-id="e914a-108">Typically, the "master" object will be a container that is the parent of the other objects in the set.</span></span>

<span data-ttu-id="e914a-109">Alcune considerazioni importanti:</span><span class="sxs-lookup"><span data-stu-id="e914a-109">Some important considerations:</span></span>

-   <span data-ttu-id="e914a-110">I GUID di coerenza combinati con conteggi di oggetti o checksum sono più efficaci dei soli GUID di coerenza, perché l'applicazione che legge gli oggetti potrebbe non essere in grado di stabilire quanti oggetti con il GUID devono essere presenti.</span><span class="sxs-lookup"><span data-stu-id="e914a-110">Consistency GUIDs combined with object counts or checksums are more effective than consistency GUIDs alone, because the application reading the objects may not know how many objects with the GUID should be present.</span></span>
-   <span data-ttu-id="e914a-111">Le applicazioni devono generare i propri GUID (un'API Microsoft Win32, UuidCreate, fornisce questa funzione) e non usare i GUID generati dal sistema presenti nell'attributo **objectGUID** di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="e914a-111">Applications must generate their own GUIDs (a Microsoft Win32 API, UuidCreate, provides this function), and not use the system-generated GUIDs found in an object's **objectGUID** attribute.</span></span> <span data-ttu-id="e914a-112">Questo perché un GUID di coerenza deve cambiare ogni volta che viene aggiornato il set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="e914a-112">This is because a consistency GUID needs to change each time the set of objects is updated.</span></span> <span data-ttu-id="e914a-113">I GUID di identità degli oggetti trovati in **objectGUID** non cambiano mai dopo la creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e914a-113">Object identity GUIDs found in **objectGUID** never change after the object has been created.</span></span>
-   <span data-ttu-id="e914a-114">I GUID di coerenza presuppongono che nessun oggetto venga condiviso tra set, quindi ogni set può avere un GUID di coerenza univoco.</span><span class="sxs-lookup"><span data-stu-id="e914a-114">Consistency GUIDs assume that no object is shared among sets, so each set can have a unique consistency GUID.</span></span>

 

 




