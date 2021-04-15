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
# <a name="components-of-eaphost"></a><span data-ttu-id="9c2ba-104">Componenti di EAPHost</span><span class="sxs-lookup"><span data-stu-id="9c2ba-104">Components of EAPHost</span></span>

<span data-ttu-id="9c2ba-105">In questo argomento vengono descritti i tre componenti dell'autenticazione EAPHost.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-105">This topic describes the three components of EAPHost authentication.</span></span>

## <a name="eaphost-components"></a><span data-ttu-id="9c2ba-106">Componenti EAPHost</span><span class="sxs-lookup"><span data-stu-id="9c2ba-106">EAPHost Components</span></span>

<span data-ttu-id="9c2ba-107">L'autenticazione EAPHost dispone dei tre componenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-107">EAPHost authentication has the following three components.</span></span>

-   <span data-ttu-id="9c2ba-108">Supplicant, che esegue le richieste di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-108">The supplicant, which makes the authentication requests.</span></span>
-   <span data-ttu-id="9c2ba-109">Metodi EAP peer (o client), che implementano i metodi EAP specifici e gestiscono la sessione di autenticazione sul lato client.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-109">The peer (or client) EAP methods, which implement the specific EAP methods and manage the authentication session on the client side.</span></span>
-   <span data-ttu-id="9c2ba-110">Metodi EAP dell'autenticatore (o server), che implementano il lato server del protocollo EAP.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-110">The authenticator (or server) EAP methods, which implement the server side of the EAP protocol.</span></span>

<span data-ttu-id="9c2ba-111">Le API supplicant vengono chiamate direttamente da un'applicazione che desidera eseguire l'autenticazione tramite EAPHost.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-111">The supplicant APIs are called directly from an application that wants to authenticate via EAPHost.</span></span> <span data-ttu-id="9c2ba-112">Le API del metodo peer e del metodo di autenticazione, tuttavia, sono prototipi di funzione che devono essere implementati per un tipo di metodo di autenticazione EAP specifico, ad esempio Microsoft Challenge Handshake Authentication Protocol versione 2,0 (MS-CHAPv2).</span><span class="sxs-lookup"><span data-stu-id="9c2ba-112">The peer method and authenticator method APIs, however, are function prototypes that must be implemented for a specific EAP authentication method type - such as the Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2).</span></span>

<span data-ttu-id="9c2ba-113">Se si sta creando un'applicazione che userà EAPHost per l'autenticazione, fare riferimento alle informazioni di [riferimento sull'API per i supplicant EAPHost](eap-host-supplicant-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9c2ba-113">If you are authoring an application that will use EAPHost for authentication, please refer to the [EAPHost Supplicant API Reference](eap-host-supplicant-api-reference.md).</span></span>

<span data-ttu-id="9c2ba-114">Se si sta creando un nuovo metodo di autenticazione EAP che verrà gestito da EAPHost, vedere le informazioni di [riferimento sull'API del metodo peer EAPHost](eap-host-peer-method-api-reference.md) e le [API del metodo](eaphost-authenticator-method-apis.md)di autenticazione EAPHost.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-114">If you are authoring a new EAP authentication method to be managed by EAPHost, please refer to the [EAPHost Peer Method API Reference](eap-host-peer-method-api-reference.md) and the [EAPHost Authenticator Method APIs](eaphost-authenticator-method-apis.md).</span></span> <span data-ttu-id="9c2ba-115">Si noti che verranno create implementazioni di queste API esposte in una nuova DLL caricata da EAPHost, anziché chiamarli direttamente.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-115">Note that you will be creating implementations of these APIs exposed in a new DLL that EAPHost loads, rather than calling them directly.</span></span>

 

 




