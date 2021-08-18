---
title: Glossario su creazione di pacchetti, distribuzione e query
description: Fornisce le definizioni per i termini relativi alla creazione di pacchetti, alla distribuzione e alle query per Windows app.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a273b82806a724e50c7f29c512d19e1723283582abb3aa8b97f49f6293182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130273"
---
# <a name="packaging-deployment-and-query-glossary"></a>Glossario su creazione di pacchetti, distribuzione e query

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID modello utente applicazione**
</dt> <dd>

L'ID modello utente applicazione identifica in modo univoco un'app nel sistema operativo in modo che il sistema operativo possa inviare notifiche e così via all'app.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**mappa a blocchi**
</dt> <dd>

Definisce gli indici e gli hash crittografici per i blocchi di codice eseguibile e i dati archiviati nei file di un pacchetto dell'app. È BlockMap.xml file di configurazione per ogni pacchetto dell'app.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**pacchetto di dipendenze**
</dt> <dd>

Pacchetto da cui dipende un altro pacchetto. La dipendenza viene dichiarata nel manifesto del pacchetto dipendente e non nel manifesto del pacchetto di dipendenza.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**pacchetto dipendente**
</dt> <dd>

Pacchetto che accetta una dipendenza da un altro pacchetto. La dipendenza viene dichiarata nel manifesto del pacchetto dipendente.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**file di footprint**
</dt> <dd>

File all'interno di un pacchetto dell'app che non fanno parte dell'app da distribuire. Questi file forniscono metadati relativi al pacchetto. I file footprint standard includono il manifesto, la mappa a blocchi, la mappa di flusso e la firma digitale. I file di footprint vengono creati come parte del processo di compilazione del pacchetto. Inoltre, in base alla specifica OPC, i tipi di contenuto.xml e i file i cui nomi corrispondono al modello \[ \_ \] \* \\ \_ "rels \\ \* .rels" sono file di footprint.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**Manifesto**
</dt> <dd>

File XML che descrive il contenuto e i metadati associati a un pacchetto, incluso l'ID pacchetto. Per ogni pacchetto dell'app è necessario un file XML manifesto.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**Opc**
</dt> <dd>

Open Packaging Conventions (OPC) descrive una tecnologia di file contenitore documentata negli standard ISO/IEC 29500 ed ECMA 376. I pacchetti dell'app sono conformi a OPC.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**Pacchetto**
</dt> <dd>

Unità del software di distribuzione, gestione e manutenzione associato al modello di creazione pacchetti dell'app. Un pacchetto contiene i file che costituiscono l'app, insieme a un file manifesto che descrive il software da Windows.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nome della famiglia di pacchetti**
</dt> <dd>

Forma serializzata dell'ID pacchetto che rappresenta in modo univoco la famiglia di pacchetti nel computer. È adatto per la denominazione di oggetti quali file e cartelle. Il nome della famiglia di pacchetti è simile al nome completo del pacchetto, ma include solo il nome e l'editore. Poiché esclude le informazioni che cambiano con la manutenzione (informazioni su versione, architettura e risorsa), è utile per i riferimenti indipendenti dalla versione al pacchetto.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nome completo del pacchetto**
</dt> <dd>

Formato serializzato dell'ID pacchetto che rappresenta in modo univoco questa versione del pacchetto nel computer. È adatto per la denominazione di oggetti quali file e cartelle.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**ID pacchetto**
</dt> <dd>

Identificatore univoco globale per un pacchetto. È costituito da una tupla di attributi per il pacchetto, tra cui nome, editore, architettura supportata, informazioni sulle risorse e versione. Vedere nome completo del pacchetto e nome della famiglia di pacchetti per i formati serializzati dell'ID pacchetto.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**ID applicazione relativo del pacchetto**
</dt> <dd>

Attributo **Id** nell'elemento [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) all'interno del manifesto del pacchetto, noto anche come PRAID. Questa stringa identifica in modo univoco un'app all'interno di un pacchetto. Questo attributo è obbligatorio per **l'elemento Application.**

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**file di payload**
</dt> <dd>

File all'interno di un pacchetto dell'app che fanno parte dell'app da distribuire. Questi file vengono estratti e inseriti nella cartella di installazione dell'utente.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**ID risorsa**
</dt> <dd>

Parte facoltativa di un ID pacchetto utilizzata per differenziare le risorse nel pacchetto. È ad esempio possibile usare un ID risorsa per specificare la lingua o le impostazioni locali.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Directory centrale ZIP**
</dt> <dd>

Sequenze di byte in un file ZIP che archiviano i metadati relativi all'archivio ZIP e al relativo contenuto, inclusi il nome, le dimensioni, le impostazioni di compressione e la posizione all'interno dell'archivio.

</dd> </dl>

 

 