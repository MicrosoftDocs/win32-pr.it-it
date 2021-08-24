---
title: Informazioni di riferimento sulle API EAPHost
description: Informazioni sulle API EAPHost e sui relativi componenti. Vedere le informazioni di riferimento per vari argomenti relativi alle API, ad esempio lo schema XML EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c522698999bcb58b4e33b8e1cb0d1bb74ae64fc3b709ce672b35e7db81e85ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739101"
---
# <a name="eaphost-api-reference"></a>Informazioni di riferimento sulle API EAPHost

Le API EAPHost sono suddivise in tre componenti: le API supplicabili, che possono essere chiamate direttamente da un'applicazione abilitata per EAP; le API del metodo peer EAP, che gestiscono richieste supplicanti per un tipo di autenticazione EAP specifico e generano elementi interattivi nel client; e le API di autenticazione EAP, che eseguono l'autenticazione lato server di un supplicante.

Gli ultimi due componenti dell'API, il metodo peer EAP e le API del metodo Authenticator EAP, richiedono un'implementazione personalizzata e conforme nelle DLL che le espongono al servizio EAPHost. Non possono essere chiamati direttamente dal codice dell'applicazione. vengono invece chiamati da EAPHost (sul lato client per i metodi peer EAP e sul lato server per i metodi di autenticazione EAP) se l'implementazione corrisponde alle firme API specificate nella documentazione corrispondente. Informazioni specifiche sull'implementazione dell'API vengono fornite in ogni pagina di riferimento della funzione.

## <a name="eaphost-registry-settings"></a>Registro di sistema EAPHost Impostazioni



| Argomento                                                      | Descrizione                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [Registro di sistema EAPHost Impostazioni](eaphost-registry-settings.md) | Descrive le chiavi del Registro di sistema utilizzate da EAPHost. |



 

## <a name="eaphost-xml-schema"></a>EAPHost XML Schema



| Argomento                                            | Descrizione                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Schema EAPHost e legacy](eaphost-schemas.md) | Vengono descritti lo schema EAPHost e lo schema legacy per la creazione del file XML di configurazione e del file XML delle credenziali. |



 

## <a name="common-eaphost-api-reference"></a>Informazioni di riferimento comuni sulle API EAPHost



| Argomento                                                                   | Descrizione                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [Enumerazioni comuni dell'API EAPHost](common-eap-host-api-enumerations.md) | Elenca le costanti comuni a tutte le API EAPHost.  |
| [Strutture comuni dell'API EAPHost](common-eap-host-api-structures.md)     | Elenca le strutture comuni a tutte le API EAPHost. |
| [Costanti comuni dell'API EAPHost](common-eap-host-error-constants.md)     | Elenca le costanti comuni a tutte le API EAPHost.  |



 

## <a name="eaphost-api-reference"></a>Informazioni di riferimento sulle API EAPHost



| Argomento                                                                       | Descrizione                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni di riferimento sulle API supplicant EAPHost](eap-host-supplicant-api-reference.md)   | Descrive gli elementi API disponibili per abilitare le chiamate supplicant a EAPHost.                                                                      |
| [Informazioni di riferimento sulle API del metodo peer EAPHost](eap-host-peer-method-api-reference.md) | Descrive gli elementi API che devono essere implementati per creare una DLL del metodo peer EAP che può essere caricata e chiamata da un client EAPHost.          |
| [API del metodo Authenticator EAPHost](eaphost-authenticator-method-apis.md)  | Descrive gli elementi API che devono essere implementati per creare una DLL del metodo di autenticazione EAP che può essere caricata e chiamata da un EAPHost del server. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su EAPHost](about-eap-host.md)
</dt> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> </dl>

 

 




