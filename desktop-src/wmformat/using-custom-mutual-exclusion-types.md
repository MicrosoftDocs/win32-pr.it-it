---
title: Utilizzo di tipi di esclusione reciproca personalizzati
description: Utilizzo di tipi di esclusione reciproca personalizzati
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- esclusione reciproca, interfaccia IWMMutualExclusion
- esclusione reciproca, tipi personalizzati
- profili, tipi di esclusione reciproca personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117371"
---
# <a name="using-custom-mutual-exclusion-types"></a><span data-ttu-id="0183f-107">Utilizzo di tipi di esclusione reciproca personalizzati</span><span class="sxs-lookup"><span data-stu-id="0183f-107">Using Custom Mutual Exclusion Types</span></span>

<span data-ttu-id="0183f-108">È possibile utilizzare gli oggetti di esclusione reciproca in un profilo per soddisfare le esigenze di scenari personalizzati.</span><span class="sxs-lookup"><span data-stu-id="0183f-108">You can use mutual exclusion objects in a profile to meet the needs of custom scenarios.</span></span> <span data-ttu-id="0183f-109">Passando il valore GUID CLSID \_ WMMUTEX \_ Unknown a [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), si informa l'oggetto di esclusione reciproca che si sta usando uno scenario personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0183f-109">By passing the GUID value CLSID\_WMMUTEX\_Unknown to [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), you inform the mutual exclusion object that you are using a custom scenario.</span></span>

<span data-ttu-id="0183f-110">È necessario controllare manualmente la selezione del flusso quando si legge un file con un valore di esclusione reciproca personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0183f-110">You must manually control stream selection when you read a file with a custom mutual exclusion value.</span></span> <span data-ttu-id="0183f-111">L'oggetto Reader utilizzerà il primo flusso aggiunto all'esclusione reciproca come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0183f-111">The reader object will use the first stream you add to the mutual exclusion as the default.</span></span>

<span data-ttu-id="0183f-112">Usare la procedura seguente per creare un oggetto di esclusione reciproca personalizzata e aggiungerlo a un profilo:</span><span class="sxs-lookup"><span data-stu-id="0183f-112">Use the following steps to create a custom mutual exclusion object and add it to a profile:</span></span>

1.  <span data-ttu-id="0183f-113">Creare una gestione profili chiamando la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="0183f-113">Create a profile manager by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="0183f-114">È possibile iniziare con un profilo esistente o crearne uno completamente nuovo.</span><span class="sxs-lookup"><span data-stu-id="0183f-114">Either start with an existing profile, or create an entirely new one.</span></span>
    -   <span data-ttu-id="0183f-115">Se si usa un profilo esistente, chiamare uno dei metodi Load dell'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="0183f-115">If you are using an existing profile, call one of the load methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="0183f-116">Quindi andare al passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="0183f-116">Then skip to step 4.</span></span>
    -   <span data-ttu-id="0183f-117">Se si sta creando un profilo completamente nuovo, chiamare [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="0183f-117">If you are creating an entirely new profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span>
3.  <span data-ttu-id="0183f-118">Aggiungere i flussi al nuovo profilo chiamando [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span><span class="sxs-lookup"><span data-stu-id="0183f-118">Add streams to the new profile by calling [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span></span> <span data-ttu-id="0183f-119">Configurare i flussi in base alle esigenze usando i metodi di [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="0183f-119">Configure the streams as needed using the methods of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span> <span data-ttu-id="0183f-120">È anche possibile chiamare **QueryInterface** per accedere ad altre interfacce nell'oggetto di configurazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="0183f-120">You can also call **QueryInterface** to access other interfaces in the stream configuration object.</span></span>

    <span data-ttu-id="0183f-121">**CreateNewStream** crea solo un oggetto di configurazione del flusso e non influisce sul profilo.</span><span class="sxs-lookup"><span data-stu-id="0183f-121">**CreateNewStream** creates only a stream configuration object, and does not affect the profile.</span></span> <span data-ttu-id="0183f-122">Dopo aver configurato correttamente un flusso, è necessario chiamare [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) per aggiungere il flusso al profilo.</span><span class="sxs-lookup"><span data-stu-id="0183f-122">After a stream is configured properly, you must call [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add the stream to the profile.</span></span>

4.  <span data-ttu-id="0183f-123">Creare un oggetto di esclusione reciproca chiamando [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="0183f-123">Create a mutual exclusion object by calling [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span></span>
5.  <span data-ttu-id="0183f-124">Aggiungere i flussi desiderati all'oggetto di esclusione reciproca chiamando [**IWMStreamList:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponibile direttamente da [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), che eredita da [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span><span class="sxs-lookup"><span data-stu-id="0183f-124">Add the desired streams to the mutual exclusion object by calling [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (available directly from [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), which inherits from [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span></span>
6.  <span data-ttu-id="0183f-125">Impostare il tipo di esclusione reciproca su Custom chiamando [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="0183f-125">Set the type of mutual exclusion to custom by calling [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span> <span data-ttu-id="0183f-126">Passare il CLSID \_ WMMUTEX \_ sconosciuto come GUID del tipo.</span><span class="sxs-lookup"><span data-stu-id="0183f-126">Pass the CLSID\_WMMUTEX\_Unknown as the type GUID.</span></span>
7.  <span data-ttu-id="0183f-127">Aggiungere l'oggetto di esclusione reciproca configurato al profilo chiamando [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="0183f-127">Add the configured mutual exclusion object to the profile by calling [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0183f-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0183f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0183f-129">**Interfaccia IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="0183f-129">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="0183f-130">**Interfaccia IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="0183f-130">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="0183f-131">**Interfaccia IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="0183f-131">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="0183f-132">**Interfaccia IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="0183f-132">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="0183f-133">**Interfaccia IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="0183f-133">**IWMStreamList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[<span data-ttu-id="0183f-134">**Uso dell'esclusione reciproca**</span><span class="sxs-lookup"><span data-stu-id="0183f-134">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="0183f-135">**WMCreateProfileManager**</span><span class="sxs-lookup"><span data-stu-id="0183f-135">**WMCreateProfileManager**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




