---
title: EAPHost e schema legacy
description: Descrive lo schema EAPHost e lo schema legacy per la creazione di XML di configurazione e delle credenziali XML.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398344"
---
# <a name="eaphost-and-legacy-schema"></a><span data-ttu-id="fb742-103">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="fb742-103">EAPHost and Legacy Schema</span></span>

<span data-ttu-id="fb742-104">Questo argomento descrive lo schema EAPHost e lo schema legacy per la creazione di XML di configurazione e delle credenziali XML.</span><span class="sxs-lookup"><span data-stu-id="fb742-104">This topic describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span>

## <a name="about-eaphost-and-legacy-schema"></a><span data-ttu-id="fb742-105">Informazioni su EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="fb742-105">About EAPHost and Legacy Schema</span></span>

<span data-ttu-id="fb742-106">La creazione di XML di configurazione inizia con lo schema [eaphostconfig](eaphostconfigschema-schema.md) . la creazione di credenziali XML inizia con lo schema [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="fb742-106">Creating configuration XML commences with the [eaphostconfig](eaphostconfigschema-schema.md) schema; creating credential XML commences with the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) schema.</span></span>

<span data-ttu-id="fb742-107">Molti degli schemi nativi e Legacy contengono elementi dello schema comune.</span><span class="sxs-lookup"><span data-stu-id="fb742-107">Several of the native and legacy schema contain common schema elements.</span></span> <span data-ttu-id="fb742-108">Gli elementi comuni utilizzati nella configurazione del metodo e le credenziali dei metodi sono estratti in un unico file di schema, denominato "schema comune".</span><span class="sxs-lookup"><span data-stu-id="fb742-108">Common elements used in method configuration and method credentials are abstracted into a single schema file, referred to as the "common schema".</span></span>

<span data-ttu-id="fb742-109">I termini "configurazione del metodo" e "proprietà di connessione" vengono usati in modo interscambiabile.</span><span class="sxs-lookup"><span data-stu-id="fb742-109">The terms "method configuration" and "connection properties" are used interchangeably.</span></span> <span data-ttu-id="fb742-110">Analogamente, i termini "credenziali metodo" e "proprietà utente" vengono usati anche in modo interscambiabile.</span><span class="sxs-lookup"><span data-stu-id="fb742-110">Likewise, the terms "method credentials" and "user properties" are also used interchangeably.</span></span>

## <a name="eaphost-schema"></a><span data-ttu-id="fb742-111">Schema EAPHost</span><span class="sxs-lookup"><span data-stu-id="fb742-111">EAPHost Schema</span></span>



| <span data-ttu-id="fb742-112">SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fb742-112">Schema</span></span>                                                                        | <span data-ttu-id="fb742-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb742-113">Description</span></span>                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="fb742-114">baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="fb742-114">baseeapmethodconfig</span></span>](baseeapmethodconfigschema-schema.md)                   | <span data-ttu-id="fb742-115">Contiene elementi dello schema di configurazione comuni.</span><span class="sxs-lookup"><span data-stu-id="fb742-115">Contains common configuration schema elements.</span></span>     |
| [<span data-ttu-id="fb742-116">baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="fb742-116">baseeapmethodusercredentials</span></span>](baseeapmethodusercredentialsschema-schema.md) | <span data-ttu-id="fb742-117">Contiene gli elementi comuni dello schema delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fb742-117">Contains common credential schema elements.</span></span>        |
| [<span data-ttu-id="fb742-118">eapcommon</span><span class="sxs-lookup"><span data-stu-id="fb742-118">eapcommon</span></span>](eapcommonschema-schema.md)                                       | <span data-ttu-id="fb742-119">Contiene la definizione dell'elemento **EapMethodType** .</span><span class="sxs-lookup"><span data-stu-id="fb742-119">Contains the **EapMethodType** element definition.</span></span> |
| [<span data-ttu-id="fb742-120">eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="fb742-120">eaphostconfig</span></span>](eaphostconfigschema-schema.md)                               | <span data-ttu-id="fb742-121">Contiene lo schema di configurazione EAPHost.</span><span class="sxs-lookup"><span data-stu-id="fb742-121">Contains EAPHost configuration schema.</span></span>             |
| [<span data-ttu-id="fb742-122">eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="fb742-122">eaphostusercredentials</span></span>](eaphostusercredentialsschema-schema.md)             | <span data-ttu-id="fb742-123">Contiene lo schema delle credenziali EAPHost.</span><span class="sxs-lookup"><span data-stu-id="fb742-123">Contains EAPHost credential schema.</span></span>                |



 

## <a name="legacy-schema"></a><span data-ttu-id="fb742-124">Schema legacy</span><span class="sxs-lookup"><span data-stu-id="fb742-124">Legacy Schema</span></span>



| <span data-ttu-id="fb742-125">SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fb742-125">Schema</span></span>                                                                            | <span data-ttu-id="fb742-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb742-126">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb742-127">baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-127">baseeapconnectionpropertiesv1</span></span>](baseeapconnectionpropertiesv1schema-schema.md)   | <span data-ttu-id="fb742-128">Contiene elementi dello schema di configurazione comuni.</span><span class="sxs-lookup"><span data-stu-id="fb742-128">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="fb742-129">baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-129">baseeapuserpropertiesv1</span></span>](baseeapuserpropertiesv1schema-schema.md)               | <span data-ttu-id="fb742-130">Contiene gli elementi comuni dello schema delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fb742-130">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="fb742-131">eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-131">eapconnectionpropertiesv1</span></span>](eapconnectionpropertiesv1schema-schema.md)           | <span data-ttu-id="fb742-132">Contiene elementi dello schema di configurazione comuni.</span><span class="sxs-lookup"><span data-stu-id="fb742-132">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="fb742-133">eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-133">eapuserpropertiesv1</span></span>](eapuserpropertiesv1schema-schema.md)                       | <span data-ttu-id="fb742-134">Contiene gli elementi comuni dello schema delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fb742-134">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="fb742-135">eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-135">eaptlsconnectionpropertiesv1</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="fb742-136">Viene usato con EAP-TLS per descrivere i dati di configurazione dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fb742-136">Is used with EAP-TLS to describe authentication configuration data.</span></span>                          |
| [<span data-ttu-id="fb742-137">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="fb742-137">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="fb742-138">Viene usato con EAP-TLS per descrivere i dati di configurazione dell'autenticazione a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb742-138">Is used with EAP-TLS to describe authentication configuration data beginning with Windows 7.</span></span> |
| [<span data-ttu-id="fb742-139">eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-139">eaptlsuserpropertiesv1</span></span>](eaptlsuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="fb742-140">Viene usato con EAP-TLS per descrivere le credenziali di autenticazione e le opzioni delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fb742-140">Is used with EAP-TLS to describe authentication credentials and credential options.</span></span>          |
| [<span data-ttu-id="fb742-141">mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-141">mschapv2connectionpropertiesv1</span></span>](mschapv2connectionpropertiesv1schema-schema.md) | <span data-ttu-id="fb742-142">Viene usato con MS-CHAPv2 per descrivere i dati di configurazione dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fb742-142">Is used with MS-CHAPv2 to describe authentication configuration data.</span></span>                        |
| [<span data-ttu-id="fb742-143">mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-143">mschapv2userpropertiesv1</span></span>](mschapv2userpropertiesv1schema-schema.md)             | <span data-ttu-id="fb742-144">Viene usato con MS-CHAPv2 per descrivere le credenziali di autenticazione e le opzioni delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fb742-144">Is used with MS-CHAPv2 to describe authentication credentials and credential options.</span></span>        |
| [<span data-ttu-id="fb742-145">mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-145">mspeapconnectionpropertiesv1</span></span>](mspeapconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="fb742-146">Viene usato con PEAPv0 per descrivere i dati di configurazione dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fb742-146">Is used with PEAPv0 to describe authentication configuration data.</span></span>                           |
| [<span data-ttu-id="fb742-147">mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="fb742-147">mspeapconnectionpropertiesv2</span></span>](mspeapconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="fb742-148">Viene usato con PEAPv0 per descrivere i dati di configurazione dell'autenticazione a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb742-148">Is used with PEAPv0 to describe authentication configuration data beginning with Windows 7.</span></span>  |
| [<span data-ttu-id="fb742-149">mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fb742-149">mspeapuserpropertiesv1</span></span>](mspeapuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="fb742-150">Viene usato con PEAPv0 per descrivere le credenziali di autenticazione e le opzioni delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="fb742-150">Is used with PEAPv0 to describe authentication credentials and credential options.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="fb742-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb742-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb742-152">Revisione degli esempi di schema EAPHost e Legacy</span><span class="sxs-lookup"><span data-stu-id="fb742-152">Reviewing EAPHost and Legacy Schema Samples</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




