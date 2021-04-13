---
title: Informazioni di riferimento sulle API EAPHost
description: Informazioni sulle API EAPHost e sui relativi componenti. Vedere informazioni di riferimento per vari argomenti sulle API, ad esempio EAPHost XML Schema.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399707"
---
# <a name="eaphost-api-reference"></a>Informazioni di riferimento sulle API EAPHost

Le API EAPHost sono divise in tre componenti: le API supplicant, che possono essere richiamate direttamente da un'applicazione abilitata per EAP. API del metodo peer EAP, che gestiscono le richieste dei supplicant per uno specifico tipo di autenticazione EAP e generano elementi interattivi nel client. e le API di autenticazione EAP, che eseguono l'autenticazione sul lato server di un supplicant.

Gli ultimi due componenti API, ovvero il metodo peer EAP e le API del metodo di autenticazione EAP, richiedono un'implementazione personalizzata e conforme nelle DLL che li espongono al servizio EAPHost. Non possono essere chiamate direttamente dal codice dell'applicazione. vengono invece chiamati da EAPHost (sul lato client per i metodi peer EAP e sul lato server per i metodi di autenticazione EAP) se l'implementazione corrisponde alle firme dell'API specificate nella documentazione corrispondente. In ogni pagina di riferimento alle funzioni vengono fornite informazioni specifiche sull'implementazione dell'API.

## <a name="eaphost-registry-settings"></a>Impostazioni del registro di sistema EAPHost



| Argomento                                                      | Descrizione                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [Impostazioni del registro di sistema EAPHost](eaphost-registry-settings.md) | Descrive le chiavi del registro di sistema utilizzate da EAPHost. |



 

## <a name="eaphost-xml-schema"></a>XML Schema EAPHost



| Argomento                                            | Descrizione                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [EAPHost e schema legacy](eaphost-schemas.md) | Descrive lo schema EAPHost e lo schema legacy per la creazione di XML di configurazione e delle credenziali XML. |



 

## <a name="common-eaphost-api-reference"></a>Informazioni di riferimento sulle API EAPHost comuni



| Argomento                                                                   | Descrizione                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [Enumerazioni API EAPHost comuni](common-eap-host-api-enumerations.md) | Elenca le costanti comuni a tutte le API EAPHost.  |
| [Strutture API EAPHost comuni](common-eap-host-api-structures.md)     | Elenca le strutture comuni a tutte le API EAPHost. |
| [Costanti API EAPHost comuni](common-eap-host-error-constants.md)     | Elenca le costanti comuni a tutte le API EAPHost.  |



 

## <a name="eaphost-api-reference"></a>Informazioni di riferimento sulle API EAPHost



| Argomento                                                                       | Descrizione                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni di riferimento sull'API del richiedente EAPHost](eap-host-supplicant-api-reference.md)   | Vengono descritti gli elementi dell'API disponibili per abilitare le chiamate di supplicant a EAPHost.                                                                      |
| [Riferimento all'API del metodo peer EAPHost](eap-host-peer-method-api-reference.md) | Vengono descritti gli elementi API che devono essere implementati per creare una DLL del metodo peer EAP che può essere caricata e chiamata da un client EAPHost.          |
| [API del metodo di autenticazione EAPHost](eaphost-authenticator-method-apis.md)  | Vengono descritti gli elementi API che devono essere implementati per creare una DLL del metodo di autenticazione EAP che può essere caricata e chiamata da un server EAPHost. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su EAPHost](about-eap-host.md)
</dt> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> </dl>

 

 




