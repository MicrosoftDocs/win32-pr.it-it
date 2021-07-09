---
description: Informazioni sull'elemento configurabile dall'utente PageColorManagement. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685794f1c9bb64c8bb3e966c4ec03bcac8821369
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549229"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="a6736-105">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="a6736-105">PageColorManagement</span></span>

<span data-ttu-id="a6736-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="a6736-106">This topic is not current.</span></span> <span data-ttu-id="a6736-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a6736-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a6736-108">Configura la gestione dei colori per la pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="a6736-108">Configures color management for the current page.</span></span> <span data-ttu-id="a6736-109">Questo è considerato automatico in SHIM - DM \_ ICMMethod Add System.</span><span class="sxs-lookup"><span data-stu-id="a6736-109">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="a6736-110">Descrive il componente che deve eseguire la gestione dei colori,ad esempio Driver.</span><span class="sxs-lookup"><span data-stu-id="a6736-110">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="a6736-111">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a6736-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a6736-112">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a6736-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a6736-113">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a6736-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a6736-114">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a6736-114">Element Information</span></span>



| <span data-ttu-id="a6736-115">Nome</span><span class="sxs-lookup"><span data-stu-id="a6736-115">Name</span></span> | <span data-ttu-id="a6736-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a6736-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="a6736-117">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a6736-117">Element Type</span></span> <br/>   | <span data-ttu-id="a6736-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="a6736-118">Feature</span></span><br/> |
| <span data-ttu-id="a6736-119">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="a6736-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a6736-120">Pagina</span><span class="sxs-lookup"><span data-stu-id="a6736-120">Page</span></span><br/>    |
| <span data-ttu-id="a6736-121">Note</span><span class="sxs-lookup"><span data-stu-id="a6736-121">Notes</span></span> <br/>          | <span data-ttu-id="a6736-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="a6736-122">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="a6736-123">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="a6736-123">Structural Content</span></span>

<span data-ttu-id="a6736-124">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="a6736-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="a6736-125">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="a6736-125">Structure Variables</span></span>

<span data-ttu-id="a6736-126">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="a6736-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a6736-127">Nome</span><span class="sxs-lookup"><span data-stu-id="a6736-127">Name</span></span>                               | <span data-ttu-id="a6736-128">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a6736-128">Data type</span></span>         | <span data-ttu-id="a6736-129">Unità</span><span class="sxs-lookup"><span data-stu-id="a6736-129">Unit</span></span>                  | <span data-ttu-id="a6736-130">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="a6736-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a6736-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a6736-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a6736-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a6736-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a6736-133">string</span><span class="sxs-lookup"><span data-stu-id="a6736-133">string</span></span><br/> | <span data-ttu-id="a6736-134">caratteri</span><span class="sxs-lookup"><span data-stu-id="a6736-134">characters</span></span><br/> | <span data-ttu-id="a6736-135">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a6736-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a6736-136">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="a6736-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a6736-137">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="a6736-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a6736-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a6736-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a6736-139">string</span><span class="sxs-lookup"><span data-stu-id="a6736-139">string</span></span><br/> | <span data-ttu-id="a6736-140">n/d</span><span class="sxs-lookup"><span data-stu-id="a6736-140">n/a</span></span><br/>        | <span data-ttu-id="a6736-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="a6736-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a6736-142">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a6736-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a6736-143">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="a6736-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a6736-144">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="a6736-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a6736-145">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="a6736-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Application has performed color management to the destination profile. -->
  <psf:Option name="psk:None" />
  <!--  Application has not performed color management and the device determines color management.-->
  <psf:Option name="psk:Device" />
  <!--  Application has not performed color management and the driver determines color management.-->
  <psf:Option name="psk:Driver" />
  <!--Color management is performed by the system. Not to be used when printing to XPSDrv print drivers -->
  <psf:Option name="psk:System" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a6736-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6736-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6736-147">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="a6736-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




