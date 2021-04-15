---
title: Componenti di EAPHost
description: Informazioni sui tre componenti dell'autenticazione EAPHost. Visualizzare altre risorse disponibili per l'uso dell'autenticazione EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474262"
---
# <a name="components-of-eaphost"></a>Componenti di EAPHost

In questo argomento vengono descritti i tre componenti dell'autenticazione EAPHost.

## <a name="eaphost-components"></a>Componenti EAPHost

L'autenticazione EAPHost dispone dei tre componenti seguenti.

-   Supplicant, che esegue le richieste di autenticazione.
-   Metodi EAP peer (o client), che implementano i metodi EAP specifici e gestiscono la sessione di autenticazione sul lato client.
-   Metodi EAP dell'autenticatore (o server), che implementano il lato server del protocollo EAP.

Le API supplicant vengono chiamate direttamente da un'applicazione che desidera eseguire l'autenticazione tramite EAPHost. Le API del metodo peer e del metodo di autenticazione, tuttavia, sono prototipi di funzione che devono essere implementati per un tipo di metodo di autenticazione EAP specifico, ad esempio Microsoft Challenge Handshake Authentication Protocol versione 2,0 (MS-CHAPv2).

Se si sta creando un'applicazione che userà EAPHost per l'autenticazione, fare riferimento alle informazioni di [riferimento sull'API per i supplicant EAPHost](eap-host-supplicant-api-reference.md).

Se si sta creando un nuovo metodo di autenticazione EAP che verrà gestito da EAPHost, vedere le informazioni di [riferimento sull'API del metodo peer EAPHost](eap-host-peer-method-api-reference.md) e le [API del metodo](eaphost-authenticator-method-apis.md)di autenticazione EAPHost. Si noti che verranno create implementazioni di queste API esposte in una nuova DLL caricata da EAPHost, anziché chiamarli direttamente.

 

 




