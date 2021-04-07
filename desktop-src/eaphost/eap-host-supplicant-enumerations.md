---
title: Enumerazioni di supplicant EAPHost
description: Informazioni sulle enumerazioni dell'API del supplicant EAPHost, ad esempio EapHostPeerMethodResultReason e \_ lo stato di isolamento.
ms.assetid: ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e214682a9b94c98db5981a0df8c2b8619814f1e5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872942"
---
# <a name="eaphost-supplicant-enumerations"></a><span data-ttu-id="16ce5-103">Enumerazioni di supplicant EAPHost</span><span class="sxs-lookup"><span data-stu-id="16ce5-103">EAPHost Supplicant Enumerations</span></span>

<span data-ttu-id="16ce5-104">Di seguito sono riportate le enumerazioni dell'API supplicant EAPHost.</span><span class="sxs-lookup"><span data-stu-id="16ce5-104">The EAPHost Supplicant API enumerations are as follows.</span></span>



| <span data-ttu-id="16ce5-105">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="16ce5-105">Enumeration</span></span>                                                                  | <span data-ttu-id="16ce5-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16ce5-106">Description</span></span>                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16ce5-107">**\_tipo di \_ dati dell'interfaccia utente interattiva EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="16ce5-107">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)     | <span data-ttu-id="16ce5-108">Specifica il set di tipi di dati di contesto dell'interfaccia utente interattiva forniti a determinate chiamate API supplicant.</span><span class="sxs-lookup"><span data-stu-id="16ce5-108">Specifies the set of types of interactive user interface context data supplied to certain supplicant API calls.</span></span>    |
| [<span data-ttu-id="16ce5-109">**\_tipo di \_ proprietà del metodo EAP \_**</span><span class="sxs-lookup"><span data-stu-id="16ce5-109">**EAP\_METHOD\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_type)              | <span data-ttu-id="16ce5-110">Windows 7 o versioni successive: specifica il tipo di proprietà Method.</span><span class="sxs-lookup"><span data-stu-id="16ce5-110">Windows 7 or later: Specifies the method property type.</span></span>                                                            |
| [<span data-ttu-id="16ce5-111">**\_tipo di \_ valore della proprietà del metodo EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="16ce5-111">**EAP\_METHOD\_PROPERTY\_VALUE\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_value_type) | <span data-ttu-id="16ce5-112">Windows 7 o versioni successive: specifica il tipo di dati del valore della proprietà di un metodo.</span><span class="sxs-lookup"><span data-stu-id="16ce5-112">Windows 7 or later: Specifies the data type of a method property value.</span></span>                                            |
| [<span data-ttu-id="16ce5-113">**\_stato di autenticazione EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="16ce5-113">**EAPHOST\_AUTH\_STATUS**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphost_auth_status)                         | <span data-ttu-id="16ce5-114">Definisce il set di possibili valori di stato della sessione di autenticazione EAP.</span><span class="sxs-lookup"><span data-stu-id="16ce5-114">Defines the set of possible EAP authentication session status values.</span></span>                                              |
| [<span data-ttu-id="16ce5-115">**EapHostPeerAuthParams**</span><span class="sxs-lookup"><span data-stu-id="16ce5-115">**EapHostPeerAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)                       | <span data-ttu-id="16ce5-116">Definisce il set di possibili valori di parametro di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="16ce5-116">Defines the set of possible authentication parameter values.</span></span>                                                       |
| [<span data-ttu-id="16ce5-117">**EapHostPeerMethodResultReason**</span><span class="sxs-lookup"><span data-stu-id="16ce5-117">**EapHostPeerMethodResultReason**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)       | <span data-ttu-id="16ce5-118">Definisce il set di possibili motivi che descrivono i risultati restituiti da un metodo EAP a un supplicant.</span><span class="sxs-lookup"><span data-stu-id="16ce5-118">Defines the set of possible reasons that describe the results returned by an EAP method to a supplicant.</span></span>           |
| [<span data-ttu-id="16ce5-119">**EapHostPeerResponseAction**</span><span class="sxs-lookup"><span data-stu-id="16ce5-119">**EapHostPeerResponseAction**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)               | <span data-ttu-id="16ce5-120">Definisce il set di azioni che un autenticatore EAP o un metodo peer può indicare a un supplicant durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="16ce5-120">Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.</span></span> |
| [<span data-ttu-id="16ce5-121">**stato di isolamento \_**</span><span class="sxs-lookup"><span data-stu-id="16ce5-121">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)                                  | <span data-ttu-id="16ce5-122">Definisce il set di possibili valori di stato di isolamento di un computer.</span><span class="sxs-lookup"><span data-stu-id="16ce5-122">Defines the set of possible isolation status values of a machine.</span></span>                                                  |



 

 

 




