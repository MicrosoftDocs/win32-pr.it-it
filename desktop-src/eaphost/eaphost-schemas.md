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
# <a name="eaphost-and-legacy-schema"></a>EAPHost e schema legacy

Questo argomento descrive lo schema EAPHost e lo schema legacy per la creazione di XML di configurazione e delle credenziali XML.

## <a name="about-eaphost-and-legacy-schema"></a>Informazioni su EAPHost e schema legacy

La creazione di XML di configurazione inizia con lo schema [eaphostconfig](eaphostconfigschema-schema.md) . la creazione di credenziali XML inizia con lo schema [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .

Molti degli schemi nativi e Legacy contengono elementi dello schema comune. Gli elementi comuni utilizzati nella configurazione del metodo e le credenziali dei metodi sono estratti in un unico file di schema, denominato "schema comune".

I termini "configurazione del metodo" e "proprietà di connessione" vengono usati in modo interscambiabile. Analogamente, i termini "credenziali metodo" e "proprietà utente" vengono usati anche in modo interscambiabile.

## <a name="eaphost-schema"></a>Schema EAPHost



| SCHEMA                                                                        | Descrizione                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | Contiene elementi dello schema di configurazione comuni.     |
| [baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md) | Contiene gli elementi comuni dello schema delle credenziali.        |
| [eapcommon](eapcommonschema-schema.md)                                       | Contiene la definizione dell'elemento **EapMethodType** . |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | Contiene lo schema di configurazione EAPHost.             |
| [eaphostusercredentials](eaphostusercredentialsschema-schema.md)             | Contiene lo schema delle credenziali EAPHost.                |



 

## <a name="legacy-schema"></a>Schema legacy



| SCHEMA                                                                            | Descrizione                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Contiene elementi dello schema di configurazione comuni.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Contiene gli elementi comuni dello schema delle credenziali.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Contiene elementi dello schema di configurazione comuni.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Contiene gli elementi comuni dello schema delle credenziali.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | Viene usato con EAP-TLS per descrivere i dati di configurazione dell'autenticazione.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | Viene usato con EAP-TLS per descrivere i dati di configurazione dell'autenticazione a partire da Windows 7. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | Viene usato con EAP-TLS per descrivere le credenziali di autenticazione e le opzioni delle credenziali.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | Viene usato con MS-CHAPv2 per descrivere i dati di configurazione dell'autenticazione.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | Viene usato con MS-CHAPv2 per descrivere le credenziali di autenticazione e le opzioni delle credenziali.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | Viene usato con PEAPv0 per descrivere i dati di configurazione dell'autenticazione.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | Viene usato con PEAPv0 per descrivere i dati di configurazione dell'autenticazione a partire da Windows 7.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | Viene usato con PEAPv0 per descrivere le credenziali di autenticazione e le opzioni delle credenziali.           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Revisione degli esempi di schema EAPHost e Legacy](eaphost-schemas.md)
</dt> </dl>

 

 




