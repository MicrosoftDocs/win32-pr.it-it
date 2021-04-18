---
title: Interfaccia IWMProfile
description: L'interfaccia IWMProfile è l'interfaccia principale per un oggetto profilo.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Formato Windows Media Interface IWMProfile
- Interfaccia IWMProfile-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "106300672"
---
# <a name="iwmprofile-interface"></a><span data-ttu-id="96ff0-105">Interfaccia IWMProfile</span><span class="sxs-lookup"><span data-stu-id="96ff0-105">IWMProfile interface</span></span>

<span data-ttu-id="96ff0-106">L'interfaccia **IWMProfile** è l'interfaccia principale per un oggetto [*profilo*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="96ff0-106">The **IWMProfile** interface is the primary interface for a [*profile*](wmformat-glossary.md) object.</span></span> <span data-ttu-id="96ff0-107">Un oggetto profilo viene usato per configurare i profili personalizzati.</span><span class="sxs-lookup"><span data-stu-id="96ff0-107">A profile object is used to configure custom profiles.</span></span> <span data-ttu-id="96ff0-108">È possibile usare **IWMProfile** per creare, eliminare o modificare oggetti di configurazione del flusso e oggetti di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="96ff0-108">You can use **IWMProfile** to create, delete, or modify stream configuration objects and mutual exclusion objects.</span></span> <span data-ttu-id="96ff0-109">È inoltre possibile impostare e recuperare informazioni generali sul profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-109">You can also set and retrieve general information about the profile.</span></span> <span data-ttu-id="96ff0-110">Per accedere a tutte le funzionalità dell'oggetto profilo, è necessario usare [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), che eredita da **IWMProfile** e [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span><span class="sxs-lookup"><span data-stu-id="96ff0-110">To access all the features of the profile object, you should use [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), which inherits from **IWMProfile** and [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span></span>

<span data-ttu-id="96ff0-111">**IWMProfile** è accessibile anche tramite l'oggetto Reader, in cui è possibile usarlo per ottenere informazioni sui flussi di un file caricato nel lettore.</span><span class="sxs-lookup"><span data-stu-id="96ff0-111">**IWMProfile** is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader.</span></span> <span data-ttu-id="96ff0-112">Quando si accede a **IWMProfile** dal lettore, è possibile apportare modifiche al profilo, ma nessuna delle modifiche può essere salvata nel file.</span><span class="sxs-lookup"><span data-stu-id="96ff0-112">When accessing **IWMProfile** from the reader, you can make changes to the profile, but none of the changes can be saved to the file.</span></span> <span data-ttu-id="96ff0-113">Spesso è utile usare il profilo di un file esistente come base di un nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-113">It is often handy to use the profile of an existing file as the foundation of a new profile.</span></span> <span data-ttu-id="96ff0-114">Il lettore sincrono supporta **IWMProfile** in modo analogo al lettore.</span><span class="sxs-lookup"><span data-stu-id="96ff0-114">The synchronous reader supports **IWMProfile** in the same way as the reader.</span></span>

<span data-ttu-id="96ff0-115">Le informazioni sul profilo ottenute tramite il Reader o il lettore sincrono non provengono da un file con estensione prx.</span><span class="sxs-lookup"><span data-stu-id="96ff0-115">The profile information obtained through the reader or synchronous reader does not come from a .prx file.</span></span> <span data-ttu-id="96ff0-116">Il lettore utilizza le informazioni nel file ASF per assemblare le configurazioni di flusso.</span><span class="sxs-lookup"><span data-stu-id="96ff0-116">The reader uses the information in the ASF file to assemble the stream configurations.</span></span> <span data-ttu-id="96ff0-117">Pertanto, alcune informazioni sul profilo, come il nome e la descrizione, non sono disponibili tramite il lettore.</span><span class="sxs-lookup"><span data-stu-id="96ff0-117">Thus certain profile information, like the name and description, are not available through the reader.</span></span>

<span data-ttu-id="96ff0-118">Esistono diversi modi per ottenere un puntatore a un'interfaccia **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="96ff0-118">There are several ways to obtain a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="96ff0-119">Gestione profili dispone di metodi per creare un nuovo profilo e per accedere ai profili esistenti.</span><span class="sxs-lookup"><span data-stu-id="96ff0-119">The profile manager has methods to create a new profile and to access existing profiles.</span></span> <span data-ttu-id="96ff0-120">Tutti questi metodi impostano un puntatore **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="96ff0-120">All of these methods set an **IWMProfile** pointer.</span></span> <span data-ttu-id="96ff0-121">Quando si legge un file, è possibile ottenere un puntatore a **IWMProfile** chiamando il metodo **QueryInterface** di qualsiasi interfaccia Reader.</span><span class="sxs-lookup"><span data-stu-id="96ff0-121">When reading a file, a pointer to **IWMProfile** can be obtained by calling the **QueryInterface** method of any reader interface.</span></span> <span data-ttu-id="96ff0-122">Analogamente, qualsiasi interfaccia dell'oggetto Reader sincrono può ottenere un puntatore con una chiamata a **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span><span class="sxs-lookup"><span data-stu-id="96ff0-122">Likewise, any interface of the synchronous reader object can obtain a pointer with a call to **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span></span>

## <a name="members"></a><span data-ttu-id="96ff0-123">Membri</span><span class="sxs-lookup"><span data-stu-id="96ff0-123">Members</span></span>

<span data-ttu-id="96ff0-124">L'interfaccia **IWMProfile** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="96ff0-124">The **IWMProfile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="96ff0-125">**IWMProfile** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="96ff0-125">**IWMProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="96ff0-126">Metodi</span><span class="sxs-lookup"><span data-stu-id="96ff0-126">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="96ff0-127">Metodi</span><span class="sxs-lookup"><span data-stu-id="96ff0-127">Methods</span></span>

<span data-ttu-id="96ff0-128">L'interfaccia **IWMProfile** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="96ff0-128">The **IWMProfile** interface has these methods.</span></span>



| <span data-ttu-id="96ff0-129">Metodo</span><span class="sxs-lookup"><span data-stu-id="96ff0-129">Method</span></span>                                                                  | <span data-ttu-id="96ff0-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96ff0-130">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96ff0-131">**AddMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="96ff0-131">**AddMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | <span data-ttu-id="96ff0-132">Aggiunge un oggetto di esclusione reciproca al profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-132">Adds a mutual exclusion object to the profile.</span></span><br/>                                   |
| [<span data-ttu-id="96ff0-133">**AddStream**</span><span class="sxs-lookup"><span data-stu-id="96ff0-133">**AddStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | <span data-ttu-id="96ff0-134">Aggiunge un flusso al profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-134">Adds a stream to the profile.</span></span><br/>                                                    |
| [<span data-ttu-id="96ff0-135">**CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="96ff0-135">**CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="96ff0-136">Crea un oggetto di esclusione reciproca per il profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-136">Creates a mutual exclusion object for the profile.</span></span><br/>                               |
| [<span data-ttu-id="96ff0-137">**CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="96ff0-137">**CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | <span data-ttu-id="96ff0-138">Crea un oggetto di configurazione del flusso per il profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-138">Creates a stream configuration object for the profile.</span></span><br/>                           |
| [<span data-ttu-id="96ff0-139">**GetDescription**</span><span class="sxs-lookup"><span data-stu-id="96ff0-139">**GetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | <span data-ttu-id="96ff0-140">Recupera la descrizione del profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-140">Retrieves the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="96ff0-141">**GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="96ff0-141">**GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="96ff0-142">Recupera un oggetto di esclusione reciproca dal profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-142">Retrieves a mutual exclusion object from the profile.</span></span><br/>                            |
| [<span data-ttu-id="96ff0-143">**GetMutualExclusionCount**</span><span class="sxs-lookup"><span data-stu-id="96ff0-143">**GetMutualExclusionCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | <span data-ttu-id="96ff0-144">Recupera il numero di oggetti di esclusione reciproca nel profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-144">Retrieves the number of mutual exclusion objects in the profile.</span></span><br/>                 |
| [<span data-ttu-id="96ff0-145">**GetName**</span><span class="sxs-lookup"><span data-stu-id="96ff0-145">**GetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | <span data-ttu-id="96ff0-146">Recupera il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-146">Retrieves the name of the profile.</span></span><br/>                                               |
| [<span data-ttu-id="96ff0-147">**GetStream**</span><span class="sxs-lookup"><span data-stu-id="96ff0-147">**GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | <span data-ttu-id="96ff0-148">Recupera un flusso, usando un numero di indice, dal profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-148">Retrieves a stream, using an index number, from the profile.</span></span><br/>                     |
| [<span data-ttu-id="96ff0-149">**GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="96ff0-149">**GetStreamByNumber**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | <span data-ttu-id="96ff0-150">Recupera un flusso, usando il numero del flusso, dal profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-150">Retrieves a stream, using the number of the stream, from the profile.</span></span><br/>            |
| [<span data-ttu-id="96ff0-151">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="96ff0-151">**GetStreamCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | <span data-ttu-id="96ff0-152">Recupera il numero di flussi nel profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-152">Retrieves the number of streams in the profile.</span></span><br/>                                  |
| [<span data-ttu-id="96ff0-153">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="96ff0-153">**GetVersion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | <span data-ttu-id="96ff0-154">Recupera il numero di versione di servizi multimediali di Microsoft Windows nel profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-154">Retrieves the version number of Microsoft Windows Media Services in the profile.</span></span><br/> |
| [<span data-ttu-id="96ff0-155">**ReconfigStream**</span><span class="sxs-lookup"><span data-stu-id="96ff0-155">**ReconfigStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | <span data-ttu-id="96ff0-156">Consente di includere nel profilo le modifiche apportate a una configurazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="96ff0-156">Enables changes made to a stream configuration to be included in the profile.</span></span><br/>    |
| [<span data-ttu-id="96ff0-157">**RemoveMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="96ff0-157">**RemoveMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | <span data-ttu-id="96ff0-158">Rimuove un oggetto di esclusione reciproca dal profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-158">Removes a mutual exclusion object from the profile.</span></span><br/>                              |
| [<span data-ttu-id="96ff0-159">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="96ff0-159">**RemoveStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | <span data-ttu-id="96ff0-160">Rimuove un flusso dal profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-160">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="96ff0-161">**RemoveStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="96ff0-161">**RemoveStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | <span data-ttu-id="96ff0-162">Rimuove un flusso dal profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-162">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="96ff0-163">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="96ff0-163">**SetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | <span data-ttu-id="96ff0-164">Specifica la descrizione del profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-164">Specifies the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="96ff0-165">**SetName**</span><span class="sxs-lookup"><span data-stu-id="96ff0-165">**SetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | <span data-ttu-id="96ff0-166">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="96ff0-166">Specifies the name of the profile.</span></span><br/>                                               |



 

<span data-ttu-id="96ff0-167">Per informazioni sulle interfacce che è possibile ottenere usando il metodo QueryInterface di questa interfaccia, vedere l'argomento relativo all'oggetto su cui è implementata questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="96ff0-167">For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.</span></span>

## <a name="see-also"></a><span data-ttu-id="96ff0-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96ff0-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ff0-169">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="96ff0-169">**Interfaces**</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="96ff0-170">**Interfaccia IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="96ff0-170">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="96ff0-171">**Oggetto Gestione profili**</span><span class="sxs-lookup"><span data-stu-id="96ff0-171">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="96ff0-172">**Oggetto Lettore**</span><span class="sxs-lookup"><span data-stu-id="96ff0-172">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="96ff0-173">**Oggetto lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="96ff0-173">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="96ff0-174">**Utilizzo dei profili**</span><span class="sxs-lookup"><span data-stu-id="96ff0-174">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

