---
title: Componenti di EAPHost
description: Informazioni sui tre componenti dell'autenticazione EAPHost. Visualizzare le risorse aggiuntive disponibili per l'uso dell'autenticazione EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa86f09473b14df6dbcc8bbc667dc4a1cc1badf9e0b6dd67ac95f8d11f2bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086415"
---
# <a name="components-of-eaphost"></a>Componenti di EAPHost

In questo argomento vengono descritti i tre componenti dell'autenticazione EAPHost.

## <a name="eaphost-components"></a>Componenti EAPHost

L'autenticazione EAPHost include i tre componenti seguenti.

-   Supplicant, che effettua le richieste di autenticazione.
-   I metodi EAP peer (o client), che implementano i metodi EAP specifici e gestiscono la sessione di autenticazione sul lato client.
-   Metodi EAP dell'autenticatore (o server), che implementano il lato server del protocollo EAP.

Le API supplicant vengono chiamate direttamente da un'applicazione che vuole eseguire l'autenticazione tramite EAPHost. Il metodo peer e le API del metodo di autenticazione, tuttavia, sono prototipi di funzione che devono essere implementati per un tipo di metodo di autenticazione EAP specifico, ad esempio Microsoft Challenge Handshake Authentication Protocol versione 2.0 (MS-CHAPv2).

Se si crea un'applicazione che userà EAPHost per l'autenticazione, fare riferimento alle informazioni di riferimento [sull'API supplicante EAPHost.](eap-host-supplicant-api-reference.md)

Se si crea un nuovo metodo di autenticazione EAP che deve essere gestito da EAPHost, fare riferimento alle informazioni di riferimento sull'API del metodo peer [EAPHost](eap-host-peer-method-api-reference.md) e alle API del metodo di Authenticator [EAPHost](eaphost-authenticator-method-apis.md). Si noti che si creeranno implementazioni di queste API esposte in una nuova DLL caricata da EAPHost, anziché chiamarle direttamente.

 

 




