---
title: Schema EAPHost e legacy
description: Vengono descritti lo schema EAPHost e lo schema legacy per la creazione del file XML di configurazione e del file XML delle credenziali.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4eb9f09a0f1380ad0373ec1171b0b0ea9101af87335d25287969d9a5f7f2da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984231"
---
# <a name="eaphost-and-legacy-schema"></a>Schema EAPHost e legacy

In questo argomento vengono descritti lo schema EAPHost e lo schema legacy per la creazione del file XML di configurazione e del file XML delle credenziali.

## <a name="about-eaphost-and-legacy-schema"></a>Informazioni su EAPHost e sullo schema legacy

La creazione del codice XML di configurazione inizia con lo schema [eaphostconfig.](eaphostconfigschema-schema.md) la creazione del file XML delle credenziali inizia con lo schema [eaphostusercredentials.](eaphostusercredentialsschema-schema.md)

Molti schemi nativi e legacy contengono elementi dello schema comuni. Gli elementi comuni usati nella configurazione del metodo e nelle credenziali del metodo vengono astratti in un singolo file di schema, definito "schema comune".

I termini "configurazione del metodo" e "proprietà di connessione" vengono usati in modo intercambiabile. Analogamente, anche i termini "credenziali del metodo" e "proprietà utente" vengono usati in modo intercambiabile.

## <a name="eaphost-schema"></a>EAPHost Schema



| Schema                                                                        | Descrizione                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | Contiene elementi comuni dello schema di configurazione.     |
| [baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md) | Contiene elementi dello schema delle credenziali comuni.        |
| [eapcommon](eapcommonschema-schema.md)                                       | Contiene la **definizione dell'elemento EapMethodType.** |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | Contiene lo schema di configurazione EAPHost.             |
| [eaphostusercredentials](eaphostusercredentialsschema-schema.md)             | Contiene lo schema delle credenziali EAPHost.                |



 

## <a name="legacy-schema"></a>Legacy Schema



| Schema                                                                            | Descrizione                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Contiene elementi comuni dello schema di configurazione.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Contiene elementi dello schema delle credenziali comuni.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Contiene elementi comuni dello schema di configurazione.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Contiene elementi dello schema delle credenziali comuni.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | Viene usato con EAP-TLS per descrivere i dati di configurazione dell'autenticazione.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | Viene usato con EAP-TLS per descrivere i dati di configurazione dell'autenticazione a partire Windows 7. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | Viene usato con EAP-TLS per descrivere le credenziali di autenticazione e le opzioni delle credenziali.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | Viene usato con l'MS-CHAPv2 per descrivere i dati di configurazione dell'autenticazione.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | Viene usato con le MS-CHAPv2 per descrivere le credenziali di autenticazione e le opzioni delle credenziali.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | Viene utilizzato con PEAPv0 per descrivere i dati di configurazione dell'autenticazione.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | Viene utilizzato con PEAPv0 per descrivere i dati di configurazione dell'autenticazione a partire Windows 7.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | Viene utilizzato con PEAPv0 per descrivere le credenziali di autenticazione e le opzioni delle credenziali.           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Revisione degli esempi di schema EAPHost e legacy](eaphost-schemas.md)
</dt> </dl>

 

 




