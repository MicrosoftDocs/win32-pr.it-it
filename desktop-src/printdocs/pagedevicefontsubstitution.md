---
description: Esaminare l'elemento PageDeviceFontSubstitution configurabile dall'utente. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: PageDeviceFontSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc5650c687a4c96e6c54ef7ea0631e77407e874
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549199"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="6fe22-105">PageDeviceFontSubstitution</span><span class="sxs-lookup"><span data-stu-id="6fe22-105">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="6fe22-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="6fe22-106">This topic is not current.</span></span> <span data-ttu-id="6fe22-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6fe22-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6fe22-108">Descrive lo stato abilitato/disabilitato della sostituzione dei tipi di carattere del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fe22-108">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="6fe22-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6fe22-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6fe22-110">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6fe22-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6fe22-111">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6fe22-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6fe22-112">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6fe22-112">Element Information</span></span>



| <span data-ttu-id="6fe22-113">Nome</span><span class="sxs-lookup"><span data-stu-id="6fe22-113">Name</span></span> | <span data-ttu-id="6fe22-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6fe22-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="6fe22-115">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="6fe22-115">Element Type</span></span> <br/>   | <span data-ttu-id="6fe22-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="6fe22-116">Feature</span></span><br/> |
| <span data-ttu-id="6fe22-117">Prefisso di ambito</span><span class="sxs-lookup"><span data-stu-id="6fe22-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6fe22-118">Pagina</span><span class="sxs-lookup"><span data-stu-id="6fe22-118">Page</span></span><br/>    |
| <span data-ttu-id="6fe22-119">Note</span><span class="sxs-lookup"><span data-stu-id="6fe22-119">Notes</span></span> <br/>          | <span data-ttu-id="6fe22-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="6fe22-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6fe22-121">Contenuto strutturale</span><span class="sxs-lookup"><span data-stu-id="6fe22-121">Structural Content</span></span>

<span data-ttu-id="6fe22-122">La struttura XML di questo elemento è:</span><span class="sxs-lookup"><span data-stu-id="6fe22-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
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

## <a name="structure-variables"></a><span data-ttu-id="6fe22-123">Variabili di struttura</span><span class="sxs-lookup"><span data-stu-id="6fe22-123">Structure Variables</span></span>

<span data-ttu-id="6fe22-124">Nella tabella seguente vengono descritte le caratteristiche delle variabili definite nella struttura XML.</span><span class="sxs-lookup"><span data-stu-id="6fe22-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6fe22-125">Nome</span><span class="sxs-lookup"><span data-stu-id="6fe22-125">Name</span></span>                               | <span data-ttu-id="6fe22-126">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6fe22-126">Data type</span></span>         | <span data-ttu-id="6fe22-127">Unità</span><span class="sxs-lookup"><span data-stu-id="6fe22-127">Unit</span></span>                  | <span data-ttu-id="6fe22-128">Valori supportati</span><span class="sxs-lookup"><span data-stu-id="6fe22-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6fe22-129">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6fe22-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6fe22-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6fe22-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6fe22-131">string</span><span class="sxs-lookup"><span data-stu-id="6fe22-131">string</span></span><br/> | <span data-ttu-id="6fe22-132">caratteri</span><span class="sxs-lookup"><span data-stu-id="6fe22-132">characters</span></span><br/> | <span data-ttu-id="6fe22-133">Nome completo valido definito da Spazi [dei nomi in XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="6fe22-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6fe22-134">Se non viene specificato alcuno spazio dei nomi, viene utilizzato lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="6fe22-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6fe22-135">Nome dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="6fe22-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6fe22-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6fe22-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6fe22-137">string</span><span class="sxs-lookup"><span data-stu-id="6fe22-137">string</span></span><br/> | <span data-ttu-id="6fe22-138">n/d</span><span class="sxs-lookup"><span data-stu-id="6fe22-138">n/a</span></span><br/>        | <span data-ttu-id="6fe22-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="6fe22-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6fe22-140">Definisce un'opzione che, se selezionata, disabilita questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6fe22-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6fe22-141">Extensible Markup Language (XML) Content</span><span class="sxs-lookup"><span data-stu-id="6fe22-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6fe22-142">Le parole chiave dello schema di stampa pubblico sono definite nello spazio dei https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nomi .</span><span class="sxs-lookup"><span data-stu-id="6fe22-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6fe22-143">Il contenuto Extensible Markup Language pubblico (XML) per questa parola chiave è definito di seguito:</span><span class="sxs-lookup"><span data-stu-id="6fe22-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Page device font substitution is off -->
  <psf:Option name="psk:Off" />
  <!--Page device font substitution is on -->
  <psf:Option name="psk:On" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="6fe22-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fe22-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fe22-145">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="6fe22-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




