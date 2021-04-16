---
description: La libreria di amministrazione MTS fornita con le interfacce di amministrazione COM+ fornisce compatibilità con le versioni precedenti della libreria di amministrazione MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Libreria di amministrazione MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523538"
---
# <a name="mts-administration-library"></a><span data-ttu-id="f2937-103">Libreria di amministrazione MTS</span><span class="sxs-lookup"><span data-stu-id="f2937-103">MTS Administration Library</span></span>

<span data-ttu-id="f2937-104">La libreria di amministrazione MTS fornita con le interfacce di amministrazione COM+ fornisce compatibilità con le versioni precedenti della libreria di amministrazione MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="f2937-104">The MTS Administration Library shipped with the COM+ Administration interfaces provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="f2937-105">La maggior parte del codice di amministrazione MTS 2,0 esistente continuerà a funzionare con la libreria MTSAdmin fornita. Tuttavia, alcune funzionalità sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="f2937-105">Most existing MTS 2.0 administration code will still work with the MTSAdmin Library that is provided; however, some functionality has changed.</span></span>

<span data-ttu-id="f2937-106">Per sfruttare i vantaggi delle nuove funzionalità o se si scrive il codice di amministrazione per la prima volta, è necessario usare la libreria COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="f2937-106">To take advantage of new functionality or if you are writing administration code for the first time, you should use the COMAdmin Library.</span></span>

<span data-ttu-id="f2937-107">Gli elementi seguenti nella libreria di amministrazione MTS corrente sono stati modificati dalla libreria di amministrazione MTS 2,0:</span><span class="sxs-lookup"><span data-stu-id="f2937-107">The following elements in the current MTS Administration Library are changed from the MTS 2.0 Administration Library:</span></span>

-   <span data-ttu-id="f2937-108">L'interfaccia **IRemoteComponentUtil** non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f2937-108">The **IRemoteComponentUtil** interface is no longer available.</span></span>
-   <span data-ttu-id="f2937-109">La raccolta **RemoteComponents** non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f2937-109">The **RemoteComponents** collection is no longer available.</span></span>
-   <span data-ttu-id="f2937-110">La proprietà RoleID non è più disponibile. il nome del ruolo viene ora usato come chiave per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f2937-110">The RoleID property is no longer available, the Role Name is now used as the key for this.</span></span>
-   <span data-ttu-id="f2937-111">Il metodo **ExportPackage** non esporta più un client.exe.</span><span class="sxs-lookup"><span data-stu-id="f2937-111">The **ExportPackage** method no longer exports a client.exe.</span></span>
-   <span data-ttu-id="f2937-112">La proprietà RemoteComponentInstallPath non è più esposta nella raccolta [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="f2937-112">The RemoteComponentInstallPath property is no longer exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="f2937-113">La proprietà ApplicationInstallPath non verrà più esposta nella raccolta [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="f2937-113">The ApplicationInstallPath property will no longer be exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="f2937-114">Il pacchetto di sistema è ora denominato applicazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="f2937-114">The System package is now named System Application.</span></span>
-   <span data-ttu-id="f2937-115">Il pacchetto Utilities è ora denominato utilità COM+.</span><span class="sxs-lookup"><span data-stu-id="f2937-115">The Utilities package is now named COM+ Utilities.</span></span>
-   <span data-ttu-id="f2937-116">La proprietà IsSynchronized è presente nella raccolta [**Components**](components.md) in MTSAdmin, ma restituirà "NotImpl" quando è selezionata e non verrà salvata se impostata.</span><span class="sxs-lookup"><span data-stu-id="f2937-116">The IsSystem property exists in the [**Components**](components.md) collection in MTSAdmin but will return "NotImpl" when checked and will not be saved if set.</span></span>
-   <span data-ttu-id="f2937-117">La proprietà PackageName non è più supportata dalla raccolta [**Components**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="f2937-117">The PackageName property is no longer supported by the [**Components**](components.md) collection.</span></span> <span data-ttu-id="f2937-118">Per determinare il nome del pacchetto, è ora necessario ottenere il PackageID e quindi trovare il pacchetto corrispondente nella raccolta di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f2937-118">To figure out the package's name, you will now need to get the PackageID and then find the matching package in the Packages collection.</span></span>
-   <span data-ttu-id="f2937-119">Le proprietà seguenti non esistono più nella raccolta [**InterfacesForComponent**](interfacesforcomponent.md) :</span><span class="sxs-lookup"><span data-stu-id="f2937-119">The following properties no longer exist on the [**InterfacesForComponent**](interfacesforcomponent.md) collection:</span></span>
    -   <span data-ttu-id="f2937-120">**ProxyCLSID**</span><span class="sxs-lookup"><span data-stu-id="f2937-120">**ProxyCLSID**</span></span>
    -   <span data-ttu-id="f2937-121">**ProxyDLL**</span><span class="sxs-lookup"><span data-stu-id="f2937-121">**ProxyDLL**</span></span>
    -   <span data-ttu-id="f2937-122">**ProxyThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="f2937-122">**ProxyThreadingModel**</span></span>
    -   <span data-ttu-id="f2937-123">**Filelibreriatipi**</span><span class="sxs-lookup"><span data-stu-id="f2937-123">**TypeLibFile**</span></span>
    -   <span data-ttu-id="f2937-124">**TypeLibID**</span><span class="sxs-lookup"><span data-stu-id="f2937-124">**TypeLibID**</span></span>
    -   <span data-ttu-id="f2937-125">**TypeLibLangID**</span><span class="sxs-lookup"><span data-stu-id="f2937-125">**TypeLibLangID**</span></span>
    -   <span data-ttu-id="f2937-126">**TypeLibPlatform**</span><span class="sxs-lookup"><span data-stu-id="f2937-126">**TypeLibPlatform**</span></span>
    -   <span data-ttu-id="f2937-127">**TypeLibVersion**</span><span class="sxs-lookup"><span data-stu-id="f2937-127">**TypeLibVersion**</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2937-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2937-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2937-129">Conversione automatica da MTS</span><span class="sxs-lookup"><span data-stu-id="f2937-129">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="f2937-130">Risultati e problemi di conversione COM+</span><span class="sxs-lookup"><span data-stu-id="f2937-130">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="f2937-131">Conversione manuale da MTS</span><span class="sxs-lookup"><span data-stu-id="f2937-131">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> </dl>

 

 



