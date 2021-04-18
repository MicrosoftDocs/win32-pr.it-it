---
title: Strutture del metodo peer EAPHost
description: Informazioni sulle strutture API del metodo peer EAPHost, ad esempio EapCertificateCredential e EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300468"
---
# <a name="eaphost-peer-method-structures"></a><span data-ttu-id="92bfc-103">Strutture del metodo peer EAPHost</span><span class="sxs-lookup"><span data-stu-id="92bfc-103">EAPHost Peer Method Structures</span></span>

<span data-ttu-id="92bfc-104">Di seguito sono riportate le strutture API del metodo peer EAPHost.</span><span class="sxs-lookup"><span data-stu-id="92bfc-104">The EAPHost Peer Method API structures are as follows.</span></span>



| <span data-ttu-id="92bfc-105">Struttura</span><span class="sxs-lookup"><span data-stu-id="92bfc-105">Structure</span></span>                                                              | <span data-ttu-id="92bfc-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92bfc-106">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92bfc-107">**EapCertificateCredential**</span><span class="sxs-lookup"><span data-stu-id="92bfc-107">**EapCertificateCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | <span data-ttu-id="92bfc-108">Contiene informazioni sul certificato utilizzato dal metodo EAP per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="92bfc-108">Contains information about the certificate that the EAP method uses for authentication.</span></span>                                                                                                            |
| [<span data-ttu-id="92bfc-109">**EapCredential**</span><span class="sxs-lookup"><span data-stu-id="92bfc-109">**EapCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | <span data-ttu-id="92bfc-110">Contiene informazioni sul tipo di credenziali e le credenziali appropriate.</span><span class="sxs-lookup"><span data-stu-id="92bfc-110">Contains information about the credentials type and the appropriate credentials.</span></span> <span data-ttu-id="92bfc-111">Viene passato come input per l'API [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) .</span><span class="sxs-lookup"><span data-stu-id="92bfc-111">This is passed as an input to the [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) API.</span></span> |
| [<span data-ttu-id="92bfc-112">**\_routine del \_ metodo \_ peer EAP**</span><span class="sxs-lookup"><span data-stu-id="92bfc-112">**EAP\_PEER\_METHOD\_ROUTINES**</span></span>](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | <span data-ttu-id="92bfc-113">Contiene un set di puntatori a funzione per le API del metodo peer EAPHost.</span><span class="sxs-lookup"><span data-stu-id="92bfc-113">Contains a set of function pointers to the EAPHost Peer Method APIs.</span></span>                                                                                                                               |
| [<span data-ttu-id="92bfc-114">**EapPeerMethodOutput**</span><span class="sxs-lookup"><span data-stu-id="92bfc-114">**EapPeerMethodOutput**</span></span>](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | <span data-ttu-id="92bfc-115">Contiene le informazioni sull'azione restituite da un metodo peer EAP.</span><span class="sxs-lookup"><span data-stu-id="92bfc-115">Contains the action information returned by an EAP peer method.</span></span>                                                                                                                                    |
| [<span data-ttu-id="92bfc-116">**EapPeerMethodResult**</span><span class="sxs-lookup"><span data-stu-id="92bfc-116">**EapPeerMethodResult**</span></span>](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | <span data-ttu-id="92bfc-117">Contiene i dati dei risultati generati da un metodo EAP durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="92bfc-117">Contains result data generated by an EAP method during authentication.</span></span>                                                                                                                             |
| [<span data-ttu-id="92bfc-118">**EapSimCredential**</span><span class="sxs-lookup"><span data-stu-id="92bfc-118">**EapSimCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | <span data-ttu-id="92bfc-119">Contiene informazioni sulla SIM utilizzata dal metodo EAP per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="92bfc-119">Contains information about the SIM that is used by the EAP method for authentication.</span></span>                                                                                                              |
| [<span data-ttu-id="92bfc-120">**EapUsernamePasswordCredential**</span><span class="sxs-lookup"><span data-stu-id="92bfc-120">**EapUsernamePasswordCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | <span data-ttu-id="92bfc-121">Contiene il nome utente e la password utilizzati dal metodo EAP per l'autenticazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="92bfc-121">Contains the username and password that is used by the EAP method for authenticating the user.</span></span>                                                                                                     |



 

 

 




