---
description: Un dispositivo può generare un numero elevato di eventi e ogni evento può essere gestito da uno dei diversi gestori.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Come registrare un gestore eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979522"
---
# <a name="how-to-register-an-event-handler"></a><span data-ttu-id="36aea-103">Come registrare un gestore eventi</span><span class="sxs-lookup"><span data-stu-id="36aea-103">How to Register an Event Handler</span></span>

<span data-ttu-id="36aea-104">Un dispositivo può generare un numero elevato di eventi e ogni evento può essere gestito da uno dei diversi gestori.</span><span class="sxs-lookup"><span data-stu-id="36aea-104">A device can potentially generate many events, and each event has the option of being handled by one of a number of different handlers.</span></span> <span data-ttu-id="36aea-105">In Windows XP vengono definiti gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="36aea-105">In Windows XP, the following events are defined:</span></span>

-   <span data-ttu-id="36aea-106">DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-106">DeviceArrival</span></span>
-   <span data-ttu-id="36aea-107">DeviceRemoval</span><span class="sxs-lookup"><span data-stu-id="36aea-107">DeviceRemoval</span></span>
-   <span data-ttu-id="36aea-108">MediaArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-108">MediaArrival</span></span>
-   <span data-ttu-id="36aea-109">MediaRemoval</span><span class="sxs-lookup"><span data-stu-id="36aea-109">MediaRemoval</span></span>

## <a name="instructions"></a><span data-ttu-id="36aea-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="36aea-110">Instructions</span></span>


<span data-ttu-id="36aea-111">I gestori eventi sono definiti sotto la chiave **EventHandlers** .</span><span class="sxs-lookup"><span data-stu-id="36aea-111">Event handlers are defined under the **EventHandlers** key.</span></span> <span data-ttu-id="36aea-112">I valori di una chiave del gestore eventi sono i nomi di ogni gestore da cui l'utente deve scegliere quando viene rilevato l'evento.</span><span class="sxs-lookup"><span data-stu-id="36aea-112">An event handler key's values are the names of each handler that the user must choose from when the event is detected.</span></span> <span data-ttu-id="36aea-113">Nessun valore di dati associato a queste voci.</span><span class="sxs-lookup"><span data-stu-id="36aea-113">There is no data value associated with these entries.</span></span> <span data-ttu-id="36aea-114">Di seguito è riportata una definizione di esempio per un gestore eventi personalizzato denominato **MyNewRemovalEventHandler**, che presenta le possibilità di gestione per l'utente:</span><span class="sxs-lookup"><span data-stu-id="36aea-114">Following is an example definition for a custom event handler called **MyNewRemovalEventHandler**, which presents these handler possibilities to the user:</span></span>

-   <span data-ttu-id="36aea-115">Gestore da usare se l'evento viene rilevato in un dispositivo creato dalla società denominata Contoso, Inc.</span><span class="sxs-lookup"><span data-stu-id="36aea-115">A handler to use if the event is detected on a device made by the company named Contoso, Inc.</span></span>
-   <span data-ttu-id="36aea-116">Gestore da usare se l'evento viene rilevato in un dispositivo creato dalla società denominata Fabrikam, Inc.</span><span class="sxs-lookup"><span data-stu-id="36aea-116">A handler to use if the event is detected on a device made by the company named Fabrikam, Inc.</span></span>
-   <span data-ttu-id="36aea-117">Gestore da utilizzare in tutti gli altri casi.</span><span class="sxs-lookup"><span data-stu-id="36aea-117">A handler to use in all other cases.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

<span data-ttu-id="36aea-118">Dopo aver definito un gestore eventi, è necessario registrarlo con un gestore di dispositivo per una delle possibilità di evento: DeviceArrival, DeviceRemoval, MediaArrival o MediaRemoval.</span><span class="sxs-lookup"><span data-stu-id="36aea-118">After an event handler is defined, it must be registered with a device handler for one of the event possibilities: DeviceArrival, DeviceRemoval, MediaArrival, or MediaRemoval.</span></span> <span data-ttu-id="36aea-119">MyNewRemovalEventHandler, definito in precedenza, viene usato per DeviceRemoval in un gestore di dispositivo personalizzato denominato MyDeviceHandler e viene definito a tale scopo nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="36aea-119">MyNewRemovalEventHandler, defined earlier, is used for DeviceRemoval under a custom device handler named MyDeviceHandler and is defined for that purpose in the following example.</span></span> <span data-ttu-id="36aea-120">Anche in questo caso il valore del registro di sistema non ha alcun componente dati.</span><span class="sxs-lookup"><span data-stu-id="36aea-120">Again, the registry value has no data component.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

<span data-ttu-id="36aea-121">Windows XP predefinisce il seguente set di EventHandlers.</span><span class="sxs-lookup"><span data-stu-id="36aea-121">Windows XP predefines the following set of EventHandlers.</span></span> 

| <span data-ttu-id="36aea-122">Chiave EventHandlers</span><span class="sxs-lookup"><span data-stu-id="36aea-122">EventHandlers key</span></span>        | <span data-ttu-id="36aea-123">Media o tipo di file</span><span class="sxs-lookup"><span data-stu-id="36aea-123">Media or file type</span></span>                             |
|--------------------------|------------------------------------------------|
| <span data-ttu-id="36aea-124">HandleCDBurningOnArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-124">HandleCDBurningOnArrival</span></span> | <span data-ttu-id="36aea-125">CD-R/CD-RW vuoti</span><span class="sxs-lookup"><span data-stu-id="36aea-125">Blank CD-R/CD-RW</span></span>                               |
| <span data-ttu-id="36aea-126">ShowPicturesOnArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-126">ShowPicturesOnArrival</span></span>    | <span data-ttu-id="36aea-127">File immagine</span><span class="sxs-lookup"><span data-stu-id="36aea-127">Picture files</span></span>                                  |
| <span data-ttu-id="36aea-128">PlayMusicFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-128">PlayMusicFilesOnArrival</span></span>  | <span data-ttu-id="36aea-129">File musicali</span><span class="sxs-lookup"><span data-stu-id="36aea-129">Music files</span></span>                                    |
| <span data-ttu-id="36aea-130">PlayVideoFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-130">PlayVideoFilesOnArrival</span></span>  | <span data-ttu-id="36aea-131">File video</span><span class="sxs-lookup"><span data-stu-id="36aea-131">Video files</span></span>                                    |
| <span data-ttu-id="36aea-132">PlayCDAudioOnArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-132">PlayCDAudioOnArrival</span></span>     | <span data-ttu-id="36aea-133">CD audio (CD di formato REDBOOK con tracce audio)</span><span class="sxs-lookup"><span data-stu-id="36aea-133">Audio CD (REDBOOK format CD with Audio tracks)</span></span> |
| <span data-ttu-id="36aea-134">PlayDVDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-134">PlayDVDMovieOnArrival</span></span>    | <span data-ttu-id="36aea-135">Film DVD</span><span class="sxs-lookup"><span data-stu-id="36aea-135">DVD movies</span></span>                                     |



 

<span data-ttu-id="36aea-136">Windows Vista predefinisce il seguente set di EventHandlers, oltre a quelli descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="36aea-136">Windows Vista predefines the following set of EventHandlers in addition to those above.</span></span> 

| <span data-ttu-id="36aea-137">Chiave EventHandlers</span><span class="sxs-lookup"><span data-stu-id="36aea-137">EventHandlers key</span></span>              | <span data-ttu-id="36aea-138">Media o tipo di file</span><span class="sxs-lookup"><span data-stu-id="36aea-138">Media or file type</span></span>   |
|--------------------------------|----------------------|
| <span data-ttu-id="36aea-139">PlaySuperVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-139">PlaySuperVideoCDMovieOnArrival</span></span> | <span data-ttu-id="36aea-140">Film di Super VideoCD</span><span class="sxs-lookup"><span data-stu-id="36aea-140">Super VideoCD movies</span></span> |
| <span data-ttu-id="36aea-141">PlayVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="36aea-141">PlayVideoCDMovieOnArrival</span></span>      | <span data-ttu-id="36aea-142">Film VideoCD</span><span class="sxs-lookup"><span data-stu-id="36aea-142">VideoCD movies</span></span>       |



 

 

 



