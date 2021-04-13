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
# <a name="packaging-deployment-and-query-glossary"></a>Creazione di pacchetti, distribuzione ed esecuzione di query sul glossario

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID modello utente applicazione**
</dt> <dd>

L'ID modello utente dell'applicazione identifica in modo univoco un'app nel sistema operativo, in modo che il sistema operativo possa inviare notifiche e così via all'app.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**blocca mappa**
</dt> <dd>

Definisce gli indici e gli hash crittografici per i blocchi di codice eseguibile e i dati archiviati nei file di un pacchetto dell'applicazione. Per ogni pacchetto dell'app è necessario un file di BlockMap.xml.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**pacchetto di dipendenze**
</dt> <dd>

Pacchetto da cui dipende un altro pacchetto. La dipendenza viene dichiarata nel manifesto del pacchetto dipendente e non nel manifesto del pacchetto di dipendenze.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**pacchetto dipendente**
</dt> <dd>

Pacchetto che accetta una dipendenza da un altro pacchetto. La dipendenza viene dichiarata nel manifesto del pacchetto dipendente.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**file footprint**
</dt> <dd>

File all'interno di un pacchetto dell'app che non fanno parte dell'app da distribuire. Questi file forniscono i metadati relativi al pacchetto. I file footprint standard includono il manifesto, la mappa a blocchi, la mappa di flusso e la firma digitale. I file footprint vengono creati come parte del processo di compilazione del pacchetto. Inoltre, in base alla specifica OPC, i \[ tipi di contenuto \_ \] . XML e i file i cui nomi corrispondono al \* \\ \_ modello "rels \\ \* . rels" sono file footprint.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifesto**
</dt> <dd>

Un file XML che descrive il contenuto e i metadati associati a un pacchetto, incluso l'ID del pacchetto. Un file XML manifesto è obbligatorio per ogni pacchetto dell'app.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**
</dt> <dd>

Open Packaging Conventions (OPC) descrive una tecnologia di file contenitore documentata negli standard ISO/IEC 29500 ed ECMA 376. I pacchetti dell'app sono conformi a OPC.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**pacchetto**
</dt> <dd>

Unità di distribuzione, gestione e software di manutenzione associati al modello di creazione di pacchetti di app. Un pacchetto contiene i file che costituiscono l'app, insieme a un file manifesto che descrive il software per Windows.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nome della famiglia di pacchetti**
</dt> <dd>

Formato serializzato dell'ID del pacchetto che rappresenta in modo univoco la famiglia di pacchetti nel computer. È adatto per la denominazione di oggetti, ad esempio file e cartelle. Il nome della famiglia di pacchetti è simile al nome completo del pacchetto, ma include solo il nome e il server di pubblicazione. Poiché esclude le informazioni che cambiano con la manutenzione (versione, architettura e informazioni sulle risorse), è utile per i riferimenti indipendenti dalla versione al pacchetto.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nome completo pacchetto**
</dt> <dd>

Formato serializzato dell'ID del pacchetto che rappresenta in modo univoco questa versione del pacchetto nel computer. È adatto per la denominazione di oggetti, ad esempio file e cartelle.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**ID pacchetto**
</dt> <dd>

Identificatore univoco globale per un pacchetto. È costituito da una tupla di attributi per il pacchetto, inclusi nome, server di pubblicazione, architettura supportata, informazioni sulle risorse e versione. Vedere il nome completo del pacchetto e il nome della famiglia di pacchetti per le forme serializzate dell'ID pacchetto.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**ID applicazione relativa del pacchetto**
</dt> <dd>

Attributo **ID** dell'elemento [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) nel manifesto del pacchetto, noto anche come Praid. Questa stringa identifica in modo univoco un'app all'interno di un pacchetto. Questo attributo è obbligatorio per l'elemento **Application** .

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**file di payload**
</dt> <dd>

I file all'interno di un pacchetto dell'app che fanno parte dell'app da distribuire. Questi file vengono estratti e inseriti nella cartella di installazione dell'utente.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**ID risorsa**
</dt> <dd>

Parte facoltativa di un ID pacchetto usato per distinguere le risorse nel pacchetto. È ad esempio possibile usare un ID di risorsa per specificare la lingua o le impostazioni locali.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Directory centrale ZIP**
</dt> <dd>

Sequenza di byte in un file ZIP che archivia i metadati sull'archivio ZIP e il relativo contenuto, inclusi nome, dimensioni, impostazioni di compressione e posizione all'interno dell'archivio.

</dd> </dl>

 

 