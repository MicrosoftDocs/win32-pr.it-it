---
description: Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81a037b6b32ff71b53688dfd6fc8afd5f10bb69
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997658"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="1f8bc-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="1f8bc-104">PageColorManagement</span></span>

<span data-ttu-id="1f8bc-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-105">This topic is not current.</span></span> <span data-ttu-id="1f8bc-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1f8bc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1f8bc-107">Configura la gestione dei colori per la pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-107">Configures color management for the current page.</span></span> <span data-ttu-id="1f8bc-108">Questo è considerato automatico in SHIM - DM \_ ICMMethod Add System.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="1f8bc-109">Descrive il componente che deve eseguire la gestione del colore,ad esempio driver.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="1f8bc-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1f8bc-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1f8bc-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="1f8bc-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1f8bc-112">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1f8bc-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1f8bc-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1f8bc-113">Element Information</span></span>



| <span data-ttu-id="1f8bc-114">Nome</span><span class="sxs-lookup"><span data-stu-id="1f8bc-114">Name</span></span> | <span data-ttu-id="1f8bc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8bc-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1f8bc-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1f8bc-116">Element Type</span></span> <br/>   | <span data-ttu-id="1f8bc-117">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="1f8bc-117">Feature</span></span><br/> |
| <span data-ttu-id="1f8bc-118">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="1f8bc-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1f8bc-119">Pagina</span><span class="sxs-lookup"><span data-stu-id="1f8bc-119">Page</span></span><br/>    |
| <span data-ttu-id="1f8bc-120">Note</span><span class="sxs-lookup"><span data-stu-id="1f8bc-120">Notes</span></span> <br/>          | <span data-ttu-id="1f8bc-121">nessuno</span><span class="sxs-lookup"><span data-stu-id="1f8bc-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="1f8bc-122">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="1f8bc-122">Structural Content</span></span>

<span data-ttu-id="1f8bc-123">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="1f8bc-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="1f8bc-124">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="1f8bc-124">Structure Variables</span></span>

<span data-ttu-id="1f8bc-125">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1f8bc-126">Nome</span><span class="sxs-lookup"><span data-stu-id="1f8bc-126">Name</span></span>                               | <span data-ttu-id="1f8bc-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1f8bc-127">Data type</span></span>         | <span data-ttu-id="1f8bc-128">Unità</span><span class="sxs-lookup"><span data-stu-id="1f8bc-128">Unit</span></span>                  | <span data-ttu-id="1f8bc-129">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="1f8bc-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1f8bc-130">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="1f8bc-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1f8bc-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1f8bc-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1f8bc-132">string</span><span class="sxs-lookup"><span data-stu-id="1f8bc-132">string</span></span><br/> | <span data-ttu-id="1f8bc-133">caratteri</span><span class="sxs-lookup"><span data-stu-id="1f8bc-133">characters</span></span><br/> | <span data-ttu-id="1f8bc-134">Nome completo valido come definito da [Spazi dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="1f8bc-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1f8bc-135">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1f8bc-136">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="1f8bc-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1f8bc-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1f8bc-138">string</span><span class="sxs-lookup"><span data-stu-id="1f8bc-138">string</span></span><br/> | <span data-ttu-id="1f8bc-139">n/d</span><span class="sxs-lookup"><span data-stu-id="1f8bc-139">n/a</span></span><br/>        | <span data-ttu-id="1f8bc-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1f8bc-141">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1f8bc-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1f8bc-142">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="1f8bc-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1f8bc-143">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="1f8bc-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1f8bc-144">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="1f8bc-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1f8bc-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f8bc-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8bc-146">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1f8bc-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




