---
title: Creazione di pacchetti, distribuzione ed esecuzione di query sul glossario
description: Fornisce le definizioni per i termini correlati alla creazione di pacchetti, alla distribuzione e alle query per le app di Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2112b593e2d2a5aaf4f06525160e2d799bad1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104398843"
---
# <a name="packaging-deployment-and-query-glossary"></a><span data-ttu-id="34ef4-103">Creazione di pacchetti, distribuzione ed esecuzione di query sul glossario</span><span class="sxs-lookup"><span data-stu-id="34ef4-103">Packaging, deployment, and query glossary</span></span>

<dl> <dt>

<span data-ttu-id="34ef4-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID modello utente applicazione**</span><span class="sxs-lookup"><span data-stu-id="34ef4-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**application user model ID**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-105">L'ID modello utente dell'applicazione identifica in modo univoco un'app nel sistema operativo, in modo che il sistema operativo possa inviare notifiche e così via all'app.</span><span class="sxs-lookup"><span data-stu-id="34ef4-105">The application user model ID uniquely identifies an app on the operating system so the operating system can send notifications and so on to the app.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**blocca mappa**</span><span class="sxs-lookup"><span data-stu-id="34ef4-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**block map**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-107">Definisce gli indici e gli hash crittografici per i blocchi di codice eseguibile e i dati archiviati nei file di un pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="34ef4-107">Defines the indices and cryptographic hashes for blocks of executable code and data that are stored in the files of an app package.</span></span> <span data-ttu-id="34ef4-108">Per ogni pacchetto dell'app è necessario un file di BlockMap.xml.</span><span class="sxs-lookup"><span data-stu-id="34ef4-108">A BlockMap.xml file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**pacchetto di dipendenze**</span><span class="sxs-lookup"><span data-stu-id="34ef4-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**dependency package**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-110">Pacchetto da cui dipende un altro pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-110">A package on which another package depends.</span></span> <span data-ttu-id="34ef4-111">La dipendenza viene dichiarata nel manifesto del pacchetto dipendente e non nel manifesto del pacchetto di dipendenze.</span><span class="sxs-lookup"><span data-stu-id="34ef4-111">The dependency is declared in the dependent package's manifest and not in the dependency package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**pacchetto dipendente**</span><span class="sxs-lookup"><span data-stu-id="34ef4-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**dependent package**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-113">Pacchetto che accetta una dipendenza da un altro pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-113">A package that takes a dependency on another package.</span></span> <span data-ttu-id="34ef4-114">La dipendenza viene dichiarata nel manifesto del pacchetto dipendente.</span><span class="sxs-lookup"><span data-stu-id="34ef4-114">The dependency is declared in the dependent package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**file footprint**</span><span class="sxs-lookup"><span data-stu-id="34ef4-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**footprint files**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-116">File all'interno di un pacchetto dell'app che non fanno parte dell'app da distribuire.</span><span class="sxs-lookup"><span data-stu-id="34ef4-116">Files within an app package that are not part of the app to be deployed.</span></span> <span data-ttu-id="34ef4-117">Questi file forniscono i metadati relativi al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-117">These files provide metadata pertaining to the package.</span></span> <span data-ttu-id="34ef4-118">I file footprint standard includono il manifesto, la mappa a blocchi, la mappa di flusso e la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="34ef4-118">Standard footprint files include the manifest, block map, stream map, and digital signature.</span></span> <span data-ttu-id="34ef4-119">I file footprint vengono creati come parte del processo di compilazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-119">Footprint files are created as part of the package build process.</span></span> <span data-ttu-id="34ef4-120">Inoltre, in base alla specifica OPC, i \[ tipi di contenuto \_ \] . XML e i file i cui nomi corrispondono al \* \\ \_ modello "rels \\ \* . rels" sono file footprint.</span><span class="sxs-lookup"><span data-stu-id="34ef4-120">In addition per the OPC specification, \[Content\_Types\].xml and files whose names match the "\*\\\_rels\\\*.rels" pattern are footprint files.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifesto**</span><span class="sxs-lookup"><span data-stu-id="34ef4-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifest**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-122">Un file XML che descrive il contenuto e i metadati associati a un pacchetto, incluso l'ID del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-122">An XML file that describes the contents and metadata associated with a package including the package ID.</span></span> <span data-ttu-id="34ef4-123">Un file XML manifesto è obbligatorio per ogni pacchetto dell'app.</span><span class="sxs-lookup"><span data-stu-id="34ef4-123">A manifest XML file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span><span class="sxs-lookup"><span data-stu-id="34ef4-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-125">Open Packaging Conventions (OPC) descrive una tecnologia di file contenitore documentata negli standard ISO/IEC 29500 ed ECMA 376.</span><span class="sxs-lookup"><span data-stu-id="34ef4-125">Open Packaging Conventions (OPC) describes a container-file technology that is documented in the ISO/IEC 29500 and ECMA 376 standards.</span></span> <span data-ttu-id="34ef4-126">I pacchetti dell'app sono conformi a OPC.</span><span class="sxs-lookup"><span data-stu-id="34ef4-126">App packages are OPC-compliant.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**pacchetto**</span><span class="sxs-lookup"><span data-stu-id="34ef4-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-128">Unità di distribuzione, gestione e software di manutenzione associati al modello di creazione di pacchetti di app.</span><span class="sxs-lookup"><span data-stu-id="34ef4-128">The unit of deployment, management, and servicing software associated with the app packaging model.</span></span> <span data-ttu-id="34ef4-129">Un pacchetto contiene i file che costituiscono l'app, insieme a un file manifesto che descrive il software per Windows.</span><span class="sxs-lookup"><span data-stu-id="34ef4-129">A package contains the files that constitute the app, along with a manifest file that describes the software to Windows.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nome della famiglia di pacchetti**</span><span class="sxs-lookup"><span data-stu-id="34ef4-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**package family name**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-131">Formato serializzato dell'ID del pacchetto che rappresenta in modo univoco la famiglia di pacchetti nel computer.</span><span class="sxs-lookup"><span data-stu-id="34ef4-131">A serialized form of the package ID that uniquely represents the package family on the computer.</span></span> <span data-ttu-id="34ef4-132">È adatto per la denominazione di oggetti, ad esempio file e cartelle.</span><span class="sxs-lookup"><span data-stu-id="34ef4-132">It is suitable for naming objects such as files and folders.</span></span> <span data-ttu-id="34ef4-133">Il nome della famiglia di pacchetti è simile al nome completo del pacchetto, ma include solo il nome e il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="34ef4-133">The package family name is similar to the package full name, but includes only the name and publisher.</span></span> <span data-ttu-id="34ef4-134">Poiché esclude le informazioni che cambiano con la manutenzione (versione, architettura e informazioni sulle risorse), è utile per i riferimenti indipendenti dalla versione al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-134">Because it excludes info that changes with servicing (version, architecture, and resource info), it is useful for version-independent references to the package.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nome completo pacchetto**</span><span class="sxs-lookup"><span data-stu-id="34ef4-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**package full name**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-136">Formato serializzato dell'ID del pacchetto che rappresenta in modo univoco questa versione del pacchetto nel computer.</span><span class="sxs-lookup"><span data-stu-id="34ef4-136">A serialized form of the package ID that uniquely represents this version of the package on the computer.</span></span> <span data-ttu-id="34ef4-137">È adatto per la denominazione di oggetti, ad esempio file e cartelle.</span><span class="sxs-lookup"><span data-stu-id="34ef4-137">It is suitable for naming objects such as files and folders.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**ID pacchetto**</span><span class="sxs-lookup"><span data-stu-id="34ef4-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**package ID**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-139">Identificatore univoco globale per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-139">A globally unique identifier for a package.</span></span> <span data-ttu-id="34ef4-140">È costituito da una tupla di attributi per il pacchetto, inclusi nome, server di pubblicazione, architettura supportata, informazioni sulle risorse e versione.</span><span class="sxs-lookup"><span data-stu-id="34ef4-140">It is composed of a tuple of attributes for the package including name, publisher, supported architecture, resource info, and version.</span></span> <span data-ttu-id="34ef4-141">Vedere il nome completo del pacchetto e il nome della famiglia di pacchetti per le forme serializzate dell'ID pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-141">See package full name and package family name for serialized forms of the package ID.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**ID applicazione relativa del pacchetto**</span><span class="sxs-lookup"><span data-stu-id="34ef4-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**package relative application ID**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-143">Attributo **ID** dell'elemento [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) nel manifesto del pacchetto, noto anche come Praid.</span><span class="sxs-lookup"><span data-stu-id="34ef4-143">The **Id** attribute on the [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) element within the package manifest, which is also known as PRAID.</span></span> <span data-ttu-id="34ef4-144">Questa stringa identifica in modo univoco un'app all'interno di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-144">This string uniquely identifies an app within a package.</span></span> <span data-ttu-id="34ef4-145">Questo attributo è obbligatorio per l'elemento **Application** .</span><span class="sxs-lookup"><span data-stu-id="34ef4-145">This attribute is required for the **Application** element.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**file di payload**</span><span class="sxs-lookup"><span data-stu-id="34ef4-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**payload files**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-147">I file all'interno di un pacchetto dell'app che fanno parte dell'app da distribuire.</span><span class="sxs-lookup"><span data-stu-id="34ef4-147">The files within an app package that are part of the app to be deployed.</span></span> <span data-ttu-id="34ef4-148">Questi file vengono estratti e inseriti nella cartella di installazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="34ef4-148">These files are extracted and placed in the user's installation folder.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**ID risorsa**</span><span class="sxs-lookup"><span data-stu-id="34ef4-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**resource ID**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-150">Parte facoltativa di un ID pacchetto usato per distinguere le risorse nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34ef4-150">An optional part of a package ID that is used to differentiate the resources in the package.</span></span> <span data-ttu-id="34ef4-151">È ad esempio possibile usare un ID di risorsa per specificare la lingua o le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="34ef4-151">For example, a resource ID can be used to specify the language or locale.</span></span>

</dd> <dt>

<span data-ttu-id="34ef4-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Directory centrale ZIP**</span><span class="sxs-lookup"><span data-stu-id="34ef4-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central directory**</span></span>
</dt> <dd>

<span data-ttu-id="34ef4-153">Sequenza di byte in un file ZIP che archivia i metadati sull'archivio ZIP e il relativo contenuto, inclusi nome, dimensioni, impostazioni di compressione e posizione all'interno dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="34ef4-153">The byte sequences in a ZIP file that store metadata about the ZIP archive and its contents including name, size, compression settings, and location within the archive.</span></span>

</dd> </dl>

 

 