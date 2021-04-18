---
description: È l'elemento radice di un file di script XML del generatore di codice WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: elemento wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309736"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="b86b1-103">elemento wsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="b86b1-103">wsdCodeGen element</span></span>

<span data-ttu-id="b86b1-104">È l'elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="b86b1-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="b86b1-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b86b1-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="b86b1-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="b86b1-106">Attributes</span></span>



| <span data-ttu-id="b86b1-107">Attributo</span><span class="sxs-lookup"><span data-stu-id="b86b1-107">Attribute</span></span>                        | <span data-ttu-id="b86b1-108">Type</span><span class="sxs-lookup"><span data-stu-id="b86b1-108">Type</span></span>                             | <span data-ttu-id="b86b1-109">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b86b1-109">Required</span></span>       | <span data-ttu-id="b86b1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b86b1-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b86b1-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="b86b1-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="b86b1-112">Qualsiasi stringa di caratteri.</span><span class="sxs-lookup"><span data-stu-id="b86b1-112">Any character string.</span></span><br/> | <span data-ttu-id="b86b1-113">Sì</span><span class="sxs-lookup"><span data-stu-id="b86b1-113">Yes</span></span><br/> | <span data-ttu-id="b86b1-114">Versione del file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b86b1-114">The version of the configuration file.</span></span> <span data-ttu-id="b86b1-115">L'unico valore valido è "1,0".</span><span class="sxs-lookup"><span data-stu-id="b86b1-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b86b1-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b86b1-116">Child elements</span></span>



| <span data-ttu-id="b86b1-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="b86b1-117">Element</span></span>                                                         | <span data-ttu-id="b86b1-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b86b1-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b86b1-119">**autoStatic**</span><span class="sxs-lookup"><span data-stu-id="b86b1-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="b86b1-120">Indica se WsdCodeGen deve provare a contrassegnare automaticamente determinati campi generati come statici.</span><span class="sxs-lookup"><span data-stu-id="b86b1-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="b86b1-121">Questa opzione è abilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b86b1-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="b86b1-122">**file**</span><span class="sxs-lookup"><span data-stu-id="b86b1-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="b86b1-123">Indica al generatore di codice di generare un file.</span><span class="sxs-lookup"><span data-stu-id="b86b1-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="b86b1-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="b86b1-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="b86b1-125">Metadati di hosting per il dispositivo da implementare.</span><span class="sxs-lookup"><span data-stu-id="b86b1-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="b86b1-126">Questo elemento viene usato solo per le implementazioni dei dispositivi (host).</span><span class="sxs-lookup"><span data-stu-id="b86b1-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="b86b1-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="b86b1-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="b86b1-128">Numero del livello di codice da generare.</span><span class="sxs-lookup"><span data-stu-id="b86b1-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="b86b1-129">I numeri di livello vengono usati nelle tabelle di runtime per distinguere un livello di codice per un altro.</span><span class="sxs-lookup"><span data-stu-id="b86b1-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="b86b1-130">WSDAPI usa il codice generato con un numero di livello pari a 0.</span><span class="sxs-lookup"><span data-stu-id="b86b1-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="b86b1-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="b86b1-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="b86b1-132">Prefisso da utilizzare nel codice generato per assicurare l'univocità dei simboli generati.</span><span class="sxs-lookup"><span data-stu-id="b86b1-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="b86b1-133">WSDAPI usa il prefisso "WSD".</span><span class="sxs-lookup"><span data-stu-id="b86b1-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="b86b1-134">**macro**</span><span class="sxs-lookup"><span data-stu-id="b86b1-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="b86b1-135">Definisce il testo o CDATA da riutilizzare nell'elemento [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="b86b1-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="b86b1-136">**nameSpace**</span><span class="sxs-lookup"><span data-stu-id="b86b1-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="b86b1-137">Descrive uno spazio dei nomi da utilizzare per la generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="b86b1-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="b86b1-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="b86b1-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="b86b1-139">Descrive l'host e i metadati ospitati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b86b1-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="b86b1-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="b86b1-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="b86b1-141">Il produttore e i metadati del modello per il dispositivo da implementare.</span><span class="sxs-lookup"><span data-stu-id="b86b1-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="b86b1-142">Questo elemento viene usato solo per le implementazioni dei dispositivi (host).</span><span class="sxs-lookup"><span data-stu-id="b86b1-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="b86b1-143">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="b86b1-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="b86b1-144">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="b86b1-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="b86b1-145">**XSD**</span><span class="sxs-lookup"><span data-stu-id="b86b1-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="b86b1-146">Specifica un file XSD da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="b86b1-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="b86b1-147">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b86b1-147">Child element sequence</span></span>

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a><span data-ttu-id="b86b1-148">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b86b1-148">Parent elements</span></span>

<span data-ttu-id="b86b1-149">Non ci sono elementi padre.</span><span class="sxs-lookup"><span data-stu-id="b86b1-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86b1-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="b86b1-150">Remarks</span></span>

<span data-ttu-id="b86b1-151">In generale, gli elementi di [**file**](file.md) devono essere eseguiti per ultimi perché generano codice che usa i dati specificati dagli altri elementi.</span><span class="sxs-lookup"><span data-stu-id="b86b1-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="b86b1-152">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b86b1-152">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b86b1-153">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b86b1-153">Minimum supported system</span></span><br/> | <span data-ttu-id="b86b1-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b86b1-154">Windows Vista</span></span> |
| <span data-ttu-id="b86b1-155">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="b86b1-155">Can be empty</span></span>                        | <span data-ttu-id="b86b1-156">Sì</span><span class="sxs-lookup"><span data-stu-id="b86b1-156">Yes</span></span>           |



 

 




