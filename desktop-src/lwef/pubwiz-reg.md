---
title: Registrazione di un servizio
description: Per aggiungere il servizio all'elenco dei provider tramite la pubblicazione guidata sul Web o la procedura guidata per l'ordine di stampa online, è necessario aggiungere la chiave e i relativi valori appropriati al registro di sistema di Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registrazione, servizi
- Pubblicazione guidata sul Web, registrazione
- Procedura guidata per l'ordine di stampa online, registrazione
- registrazione, pubblicazione guidata sul Web
- registrazione, ordinamento guidato stampa online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234911"
---
# <a name="registering-a-service"></a><span data-ttu-id="4fb14-108">Registrazione di un servizio</span><span class="sxs-lookup"><span data-stu-id="4fb14-108">Registering a Service</span></span>

<span data-ttu-id="4fb14-109">Per aggiungere il servizio all'elenco dei provider tramite la pubblicazione guidata sul Web o la procedura guidata per l'ordine di stampa online, è necessario aggiungere la chiave e i relativi valori appropriati al registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="4fb14-109">To add your service to the list of providers in either the Web Publishing Wizard or the Online Print Ordering Wizard, you must add the appropriate key and its values to the Windows registry.</span></span>

## <a name="required-keys-and-values"></a><span data-ttu-id="4fb14-110">Chiavi e valori obbligatori</span><span class="sxs-lookup"><span data-stu-id="4fb14-110">Required Keys and Values</span></span>

<span data-ttu-id="4fb14-111">Per aggiungere il servizio all'elenco dei provider per la pubblicazione guidata sul Web, aggiungere una chiave come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4fb14-111">To add your service to the list of providers for the Web Publishing Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="4fb14-112">Per aggiungere il servizio all'elenco dei provider per la procedura guidata per l'ordine di stampa online, aggiungere una chiave come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="4fb14-112">To add your service to the list of providers for the Online Print Ordering Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="4fb14-113">Ognuno dei valori è una stringa di tipo REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="4fb14-113">Each of the values is a string of type REG\_SZ.</span></span> <span data-ttu-id="4fb14-114">Fornire i dati come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4fb14-114">Provide its data as explained in the following table.</span></span> 

| <span data-ttu-id="4fb14-115">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="4fb14-115">Value Name</span></span>     | <span data-ttu-id="4fb14-116">Spiegazione</span><span class="sxs-lookup"><span data-stu-id="4fb14-116">Explanation</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb14-117">IconPath</span><span class="sxs-lookup"><span data-stu-id="4fb14-117">IconPath</span></span>       | <span data-ttu-id="4fb14-118">Percorso completo del file di icona, incluso il nome del file.</span><span class="sxs-lookup"><span data-stu-id="4fb14-118">The full path to the icon file, including the file name.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="4fb14-119">DisplayName</span><span class="sxs-lookup"><span data-stu-id="4fb14-119">DisplayName</span></span>    | <span data-ttu-id="4fb14-120">Nome visualizzato per il servizio nell'elenco dei provider della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="4fb14-120">The name displayed for your service in the wizard's providers list.</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4fb14-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb14-121">Description</span></span>    | <span data-ttu-id="4fb14-122">Breve descrizione del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fb14-122">A short description for your service.</span></span> <span data-ttu-id="4fb14-123">Questa descrizione viene visualizzata anche nell'elenco dei provider della procedura guidata direttamente sotto il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fb14-123">This description also displays in the wizard's providers list directly below the name of your service.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="4fb14-124">HREF</span><span class="sxs-lookup"><span data-stu-id="4fb14-124">HREF</span></span>           | <span data-ttu-id="4fb14-125">URL della prima pagina del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fb14-125">The URL of the first page of your service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4fb14-126">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="4fb14-126">SupportedTypes</span></span> | <span data-ttu-id="4fb14-127">Tipi di file supportati dal servizio.</span><span class="sxs-lookup"><span data-stu-id="4fb14-127">The file types supported by your service.</span></span> <span data-ttu-id="4fb14-128">Ad esempio, *\* jpg*.</span><span class="sxs-lookup"><span data-stu-id="4fb14-128">For instance, *\*.jpg*.</span></span> <span data-ttu-id="4fb14-129">Specificando solo determinati tipi di file, il servizio viene visualizzato solo quando questi tipi di file sono stati selezionati.</span><span class="sxs-lookup"><span data-stu-id="4fb14-129">By specifying only certain file types, your service only appears when those file types have been selected.</span></span> <span data-ttu-id="4fb14-130">Se è stato selezionato più di un tipo di file, il servizio viene visualizzato se uno di questi tipi di file è supportato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="4fb14-130">If more than one file type has been selected, your service appears if any of those file types are supported by your service.</span></span> <span data-ttu-id="4fb14-131">Se si desidera specificare più tipi di file, separarli nell'elenco con un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="4fb14-131">If you want to specify multiple file types, separate them in the list with semicolons.</span></span> <span data-ttu-id="4fb14-132">Ad esempio, *\* . jpg; \* . BMP*.</span><span class="sxs-lookup"><span data-stu-id="4fb14-132">For example, *\*.jpg; \*.bmp*.</span></span> |



 

<span data-ttu-id="4fb14-133">Di seguito è riportato un esempio completo per un servizio di elaborazione foto denominato "provider".</span><span class="sxs-lookup"><span data-stu-id="4fb14-133">The following is a complete example for a photo processing service entitled "MyProvider."</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

<span data-ttu-id="4fb14-134">Quando viene chiamato l'URL del servizio, vengono aggiunti due valori alla fine dell'URL, ovvero LCID e langid.</span><span class="sxs-lookup"><span data-stu-id="4fb14-134">When the URL of your service is called, two values are added to the end of the URL—lcid and langid.</span></span> <span data-ttu-id="4fb14-135">Ad esempio, la stringa URL per l'esempio precedente potrebbe essere https: \/ /www.MyProvider.com/Intro.htm? LCID = 1033&LangID = 1033.</span><span class="sxs-lookup"><span data-stu-id="4fb14-135">For example, the URL string for the example above might be https:\//www.MyProvider.com/Intro.htm?lcid=1033&langid=1033.</span></span> <span data-ttu-id="4fb14-136">Queste variabili vengono usate per le informazioni relative alla lingua e alla localizzazione.</span><span class="sxs-lookup"><span data-stu-id="4fb14-136">These variables are used for language and localization information.</span></span>

-   <span data-ttu-id="4fb14-137">**LCID** viene usato per informare il server delle impostazioni relative al paese e alla lingua del client.</span><span class="sxs-lookup"><span data-stu-id="4fb14-137">**lcid** is used to inform the server of the client's country/region and language settings.</span></span> <span data-ttu-id="4fb14-138">Non viene usato per determinare la lingua dell'interfaccia utente del client, ma viene usato per determinare il formato corretto per valuta, data e ora e altri dati specifici dell'area.</span><span class="sxs-lookup"><span data-stu-id="4fb14-138">It is not used to determine the language of the client's UI, but is used to determine the proper format for currency, date and time, and other region-specific data.</span></span>
-   <span data-ttu-id="4fb14-139">**LangID** viene usato per informare il server dell'impostazione della lingua predefinita del client in modo da poter usare la lingua corretta nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4fb14-139">**langid** is used to inform the server of the client's default language setting so that it can use the proper language in the UI.</span></span>

 

 




