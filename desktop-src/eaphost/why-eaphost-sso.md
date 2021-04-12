---
title: Panoramica dello scenario EAPHost SSO
description: Contiene due scenari che illustrano i vantaggi di un supplicant abilitato per l'accesso Single Sign-on (SSO).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104117241"
---
# <a name="sso-eaphost-scenario-overview"></a><span data-ttu-id="50664-103">Panoramica dello scenario EAPHost SSO</span><span class="sxs-lookup"><span data-stu-id="50664-103">SSO EAPHost Scenario Overview</span></span>

<span data-ttu-id="50664-104">Nell'argomento seguente sono inclusi due scenari in cui vengono illustrati i vantaggi di un supplicant abilitato per l'accesso Single Sign-on (SSO).</span><span class="sxs-lookup"><span data-stu-id="50664-104">The following topic contains two scenarios that demonstrate the advantages of a Single-Sign-On (SSO) enabled supplicant.</span></span>

## <a name="about-the-scenarios"></a><span data-ttu-id="50664-105">Informazioni sugli scenari</span><span class="sxs-lookup"><span data-stu-id="50664-105">About the Scenarios</span></span>

<span data-ttu-id="50664-106">SSO fornisce funzionalità per conservare informazioni aggiuntive sulle credenziali utente rispetto a quelle tradizionalmente archiviate nel BLOB utente EAP.</span><span class="sxs-lookup"><span data-stu-id="50664-106">SSO provides functionality to retain additional user credential information than is traditionally stored in the EAP user BLOB.</span></span> <span data-ttu-id="50664-107">A differenza di altri processi di credenziali, i supplicant abilitati per SSO possono risolvere situazioni di accesso come il roaming di AP e la modifica della password senza l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="50664-107">Unlike other credential processes, SSO-enabled supplicants can resolve login situations like AP roaming, and password change without user intervention.</span></span>

## <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="50664-108">Comportamento della memorizzazione nella cache del PIN SSO EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="50664-108">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="50664-109">Un supplicant può tentare di eseguire l'autenticazione di rete usando un metodo EAP basato su smart card, ad esempio Extensible Authentication Protocol Transport Layer Security (EAP-TLS).</span><span class="sxs-lookup"><span data-stu-id="50664-109">A supplicant can attempt network authentication using a smartcard-based EAP method such as Extensible Authentication Protocol Transport Layer Security (EAP-TLS).</span></span> <span data-ttu-id="50664-110">In questo e in scenari simili, il supplicant ottiene il PIN della smart card dall'utente e recupera un certificato utente per l'autenticazione di rete seguito da una chiamata a WinLogin nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="50664-110">In this and similar scenarios, the supplicant obtains the smartcard PIN from the user and retrieves a user certificate for network authentication followed by a call to WinLogin on the local computer.</span></span> <span data-ttu-id="50664-111">Al termine dell'autenticazione, il richiedente memorizza nella cache il BLOB utente e non archivia le informazioni sul PIN dell'utente.</span><span class="sxs-lookup"><span data-stu-id="50664-111">After successful authentication the supplicant caches the user BLOB, and does not store user PIN information.</span></span>

<span data-ttu-id="50664-112">Quando l'utente si sposta in un percorso di ripresa della sessione diverso ed è necessario ripetere l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="50664-112">When the user roams to a different location session resumption and re-authentication must occur.</span></span> <span data-ttu-id="50664-113">Poiché non è possibile archiviare il certificato con pre-accesso, l'autenticazione utente avrà esito negativo e il richiedente Scarica il BLOB utente.</span><span class="sxs-lookup"><span data-stu-id="50664-113">Since the certificate cannot be stored pre-logon, the user authentication will fail and the supplicant flushes the user BLOB.</span></span> <span data-ttu-id="50664-114">A questo punto, il PIN dell'utente è necessario per recuperare il certificato utente dalla smart card per l'autenticazione di rete.</span><span class="sxs-lookup"><span data-stu-id="50664-114">At this point the user PIN is required to retrieve the user certificate from the smartcard for network authentication.</span></span> <span data-ttu-id="50664-115">Poiché SSO memorizza nella cache il PIN, il certificato può essere recuperato senza l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="50664-115">Because SSO caches the PIN, the certificate can be retrieved without user intervention.</span></span> <span data-ttu-id="50664-116">Senza SSO, EAP-TLS dovrebbe generare nuovamente un'interfaccia utente per la raccolta di PIN.</span><span class="sxs-lookup"><span data-stu-id="50664-116">Without SSO, EAP-TLS would have to raise a PIN collection UI again.</span></span>

<span data-ttu-id="50664-117">Per un approccio dettagliato, vedere comportamento di caching del [pin SSO EAP-TLS](sso-eap-tls-pin-caching-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="50664-117">For a step-by-step approach, see [SSO EAP-TLS PIN Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).</span></span>

## <a name="sso-password-change-behavior"></a><span data-ttu-id="50664-118">Comportamento di modifica della password SSO</span><span class="sxs-lookup"><span data-stu-id="50664-118">SSO Password Change Behavior</span></span>

<span data-ttu-id="50664-119">Un supplicant può tentare di eseguire l'autenticazione di rete usando un metodo EAP basato su password, ad esempio Microsoft Challenge Handshake Authentication Protocol versione 2,0 (MS-CHAPv2), configurato per usare le credenziali di WinLogin.</span><span class="sxs-lookup"><span data-stu-id="50664-119">A supplicant can attempt network authentication using a password-based EAP method such as Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2), configured to use WinLogin credentials.</span></span> <span data-ttu-id="50664-120">In questo scenario, il supplicant raccoglie le credenziali utente una volta e le fornisce a EAPHost per l'autenticazione di rete.</span><span class="sxs-lookup"><span data-stu-id="50664-120">In this scenario, the supplicant collects user credentials once and provides them to EAPHost for network authentication.</span></span> <span data-ttu-id="50664-121">Al termine dell'autenticazione di rete, il supplicant usa lo stesso set di credenziali per WinLogin.</span><span class="sxs-lookup"><span data-stu-id="50664-121">After successful network authentication the supplicant uses the same set of credentials for WinLogin.</span></span>

<span data-ttu-id="50664-122">Tuttavia, se le credenziali, ad esempio la password dell'utente sono state modificate durante l'autenticazione di rete senza un supplicant abilitato per SSO, la successiva chiamata a WinLogin provocherà un errore.</span><span class="sxs-lookup"><span data-stu-id="50664-122">However, if credentials such as the user password were changed during network authentication without an SSO-enabled supplicant, the subsequent WinLogin call will result in failure.</span></span> <span data-ttu-id="50664-123">SSO mantiene le nuove credenziali e consente un WinLogin riuscito senza ulteriori interventi da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="50664-123">SSO retains the new credentials and allows a successful WinLogin without additional user intervention.</span></span>

<span data-ttu-id="50664-124">Per un approccio dettagliato, vedere comportamento di modifica della [password SSO](sso-password-change-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="50664-124">For a step-by-step approach, see [SSO Password Change Behavior](sso-password-change-behavior-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="50664-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50664-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50664-126">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="50664-126">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




