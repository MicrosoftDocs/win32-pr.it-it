---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ae8d161035d23149759345e8eb139dd3fb7a48
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321131"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="16660-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="16660-104">PageColorManagement</span></span>

<span data-ttu-id="16660-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="16660-105">This topic is not current.</span></span> <span data-ttu-id="16660-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="16660-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="16660-107">Configura la gestione dei colori per la pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="16660-107">Configures color management for the current page.</span></span> <span data-ttu-id="16660-108">Questa operazione viene considerata automatica in SHIM-DM \_ ICMMethod Add System.</span><span class="sxs-lookup"><span data-stu-id="16660-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="16660-109">Descrive il componente che deve eseguire la gestione dei colori, ad esempio il driver.</span><span class="sxs-lookup"><span data-stu-id="16660-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="16660-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="16660-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="16660-111">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="16660-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="16660-112">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="16660-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="16660-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="16660-113">Element Information</span></span>



| <span data-ttu-id="16660-114">Nome</span><span class="sxs-lookup"><span data-stu-id="16660-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="16660-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="16660-115">Element Type</span></span> <br/>   | <span data-ttu-id="16660-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="16660-116">Feature</span></span><br/> |
| <span data-ttu-id="16660-117">Prefisso ambito</span><span class="sxs-lookup"><span data-stu-id="16660-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="16660-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="16660-118">Page</span></span><br/>    |
| <span data-ttu-id="16660-119">Note</span><span class="sxs-lookup"><span data-stu-id="16660-119">Notes</span></span> <br/>          | <span data-ttu-id="16660-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="16660-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="16660-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="16660-121">Structural Content</span></span>

<span data-ttu-id="16660-122">La struttura XML di questo elemento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="16660-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="16660-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="16660-123">Structure Variables</span></span>

<span data-ttu-id="16660-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="16660-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="16660-125">Nome</span><span class="sxs-lookup"><span data-stu-id="16660-125">Name</span></span>                               | <span data-ttu-id="16660-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="16660-126">Data type</span></span>         | <span data-ttu-id="16660-127">Unità</span><span class="sxs-lookup"><span data-stu-id="16660-127">Unit</span></span>                  | <span data-ttu-id="16660-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="16660-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="16660-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="16660-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="16660-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="16660-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="16660-131">string</span><span class="sxs-lookup"><span data-stu-id="16660-131">string</span></span><br/> | <span data-ttu-id="16660-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="16660-132">characters</span></span><br/> | <span data-ttu-id="16660-133">Nome completo valido definito dagli [spazi dei nomi in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="16660-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="16660-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="16660-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="16660-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="16660-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="16660-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="16660-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="16660-137">string</span><span class="sxs-lookup"><span data-stu-id="16660-137">string</span></span><br/> | <span data-ttu-id="16660-138">n/d</span><span class="sxs-lookup"><span data-stu-id="16660-138">n/a</span></span><br/>        | <span data-ttu-id="16660-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="16660-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="16660-140">Definisce un'opzione che, quando selezionata, Disabilita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="16660-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="16660-141">Contenuto Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="16660-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="16660-142">Le parole chiave dello schema di stampa pubbliche sono definite nello https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="16660-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="16660-143">Il contenuto del Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="16660-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="16660-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16660-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16660-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="16660-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




