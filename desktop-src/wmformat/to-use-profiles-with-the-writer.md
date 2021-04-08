---
title: Per utilizzare profili con il writer
description: Per utilizzare profili con il writer
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK, scrittura di file ASF
- Windows Media Format SDK, creazione di file ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Formato di sistemi avanzati (ASF), scrittura di file
- ASF (Advanced Systems Format), scrittura di file
- ASF (Advanced Systems Format), creazione di file
- ASF (Advanced Systems Format), creazione di file
- profili, creazione di file ASF
- profili, scrittura di file ASF
- profili, creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046429"
---
# <a name="to-use-profiles-with-the-writer"></a><span data-ttu-id="6e67b-113">Per utilizzare profili con il writer</span><span class="sxs-lookup"><span data-stu-id="6e67b-113">To Use Profiles with the Writer</span></span>

<span data-ttu-id="6e67b-114">Il writer usa i dati di profilo per creare file ASF.</span><span class="sxs-lookup"><span data-stu-id="6e67b-114">The writer uses profile data to create ASF files.</span></span> <span data-ttu-id="6e67b-115">È necessario specificare un profilo da usare prima di eseguire altre operazioni con il writer.</span><span class="sxs-lookup"><span data-stu-id="6e67b-115">You must specify a profile for use before doing anything else with the writer.</span></span>

<span data-ttu-id="6e67b-116">È possibile impostare un profilo di sistema da usare con il writer passando l'ID del profilo al metodo [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .</span><span class="sxs-lookup"><span data-stu-id="6e67b-116">You can set a system profile for use with the writer by passing the profile ID to the [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) method.</span></span>

<span data-ttu-id="6e67b-117">Per specificare un profilo personalizzato da usare con il writer, è necessario ottenere un'interfaccia [**IWMProfile**](iwmprofile.md) per un oggetto contenente i dati del profilo desiderato.</span><span class="sxs-lookup"><span data-stu-id="6e67b-117">To specify a custom profile for use with the writer, you must obtain an [**IWMProfile**](iwmprofile.md) interface to an object containing the desired profile data.</span></span> <span data-ttu-id="6e67b-118">Per eseguire questa operazione, è possibile utilizzare uno dei metodi di caricamento dell'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="6e67b-118">You can use one of the loading methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface to accomplish this.</span></span> <span data-ttu-id="6e67b-119">Quando si dispone di un'interfaccia **IWMProfile** valida, è possibile passare un puntatore al metodo [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) .</span><span class="sxs-lookup"><span data-stu-id="6e67b-119">After you have a valid **IWMProfile** interface, you can pass a pointer to it to the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method.</span></span> <span data-ttu-id="6e67b-120">Per ulteriori informazioni sulle impostazioni del profilo, vedere [utilizzo dei profili](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6e67b-120">For more information about profile settings, see [Working with Profiles](working-with-profiles.md).</span></span>

<span data-ttu-id="6e67b-121">Se si apportano modifiche all'oggetto profilo utilizzando l'interfaccia **IWMProfile** dopo aver impostato il profilo nel writer, è **necessario chiamare di nuovo il profilo,** altrimenti le modifiche non verranno riflesse nel writer.</span><span class="sxs-lookup"><span data-stu-id="6e67b-121">If you make changes to the profile object by using the **IWMProfile** interface after setting the profile in the writer, you must call **SetProfile** again, or else the changes will not be reflected in the writer.</span></span> <span data-ttu-id="6e67b-122">Tuttavia, la chiamata a **seprofile** Reimposta tutti gli attributi di intestazione, pertanto assicurarsi di impostare gli attributi di intestazione obbligatori dopo la chiamata a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6e67b-122">However, calling **SetProfile** will reset all header attributes, so be sure to set any required header attributes after calling this method.</span></span>

<span data-ttu-id="6e67b-123">La funzione di esempio seguente imposta il profilo su "Windows Media Video 8 per i modem di connessione remota (56 Kbps)":</span><span class="sxs-lookup"><span data-stu-id="6e67b-123">The following example function sets the profile to "Windows Media Video 8 for Dial-up Modems (56 Kbps)":</span></span>


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> <span data-ttu-id="6e67b-124">Non esistono profili di sistema predefiniti che usano i codec della serie Windows Media Audio e video 9.</span><span class="sxs-lookup"><span data-stu-id="6e67b-124">There are no predefined system profiles that use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="6e67b-125">Per ulteriori informazioni, vedere [riutilizzo delle configurazioni di flusso](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="6e67b-125">For more information, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6e67b-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e67b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e67b-127">**IWMWriter::SetProfileByID**</span><span class="sxs-lookup"><span data-stu-id="6e67b-127">**IWMWriter::SetProfileByID**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[<span data-ttu-id="6e67b-128">**Utilizzo dei profili**</span><span class="sxs-lookup"><span data-stu-id="6e67b-128">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="6e67b-129">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="6e67b-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




