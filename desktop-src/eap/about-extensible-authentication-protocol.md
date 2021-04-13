---
title: Informazioni su EAP
description: Extensible Authentication Protocol (EAP), uno standard supportato da molti componenti di rete Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocollo di autenticazione estendibile, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399841"
---
# <a name="about-eap"></a><span data-ttu-id="8044e-104">Informazioni su EAP</span><span class="sxs-lookup"><span data-stu-id="8044e-104">About EAP</span></span>

<span data-ttu-id="8044e-105">In questo argomento viene descritto il protocollo EAP (Extensible Authentication Protocol), uno standard supportato da molti componenti di rete Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8044e-105">This topic describes Extensible Authentication Protocol (EAP), a standard supported by many Microsoft networking components.</span></span>

## <a name="eap-components"></a><span data-ttu-id="8044e-106">Componenti EAP</span><span class="sxs-lookup"><span data-stu-id="8044e-106">EAP Components</span></span>

<span data-ttu-id="8044e-107">Il protocollo EAP è essenziale per la protezione della sicurezza di reti LAN wireless (802.1 X), LAN cablate e connessioni remote e VPN (Virtual Private Network).</span><span class="sxs-lookup"><span data-stu-id="8044e-107">EAP is crucial for protecting the security of wireless (802.1X) LANs, wired LANs, and dial-up and Virtual Private Networks (VPNs).</span></span>

<span data-ttu-id="8044e-108">I componenti seguenti supportano il protocollo EAP.</span><span class="sxs-lookup"><span data-stu-id="8044e-108">The following components support the EAP protocol.</span></span>

-   <span data-ttu-id="8044e-109">I client e i server di accesso remoto Microsoft per la connessione remota e la VPN (PPTP e L2TP/IPSec) implementano EAP come estensione di PPP.</span><span class="sxs-lookup"><span data-stu-id="8044e-109">Microsoft Remote Access Clients and Servers for both dial-up and VPN (PPTP and L2TP/IPSec) implement EAP as an extension to PPP.</span></span> <span data-ttu-id="8044e-110">Per ulteriori informazioni, vedere [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span><span class="sxs-lookup"><span data-stu-id="8044e-110">For more information, see [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span></span>
-   <span data-ttu-id="8044e-111">I client LAN wireless e cablati compatibili con Microsoft IEEE 802.1 X implementano EAP come definito nello standard Draft IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="8044e-111">Microsoft IEEE 802.1X compatible wireless and wired LAN clients implement EAP as defined in the IEEE 802.1X draft standard.</span></span>
-   <span data-ttu-id="8044e-112">Server RADIUS Microsoft, denominato servizio di autenticazione Internet (IAS), implementa EAP come definito nella [specifica RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span><span class="sxs-lookup"><span data-stu-id="8044e-112">Microsoft RADIUS server, called Internet Authentication Service (IAS) implement EAP as defined in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span></span>

<span data-ttu-id="8044e-113">Tutti i componenti precedenti supportano questa architettura estendibile tramite il Software Development Kit (SDK) di Microsoft Windows, rendendo possibile l'integrazione dei moduli di autenticazione di terze parti.</span><span class="sxs-lookup"><span data-stu-id="8044e-113">All of the above components support this extensible architecture through the Microsoft Windows Software Development Kit (SDK), making it possible to integrate third-party authentication modules.</span></span> <span data-ttu-id="8044e-114">Questo meccanismo estensibile può essere utilizzato per supportare schede token, Kerberos, chiave pubblica e protocolli di autenticazione S/chiave.</span><span class="sxs-lookup"><span data-stu-id="8044e-114">This extensible mechanism can be used to support token cards, Kerberos, Public Key, and S/Key authentication protocols.</span></span>

## <a name="protected-extensible-authentication-protocol"></a><span data-ttu-id="8044e-115">Protocollo di autenticazione estensibile protetto</span><span class="sxs-lookup"><span data-stu-id="8044e-115">Protected Extensible Authentication Protocol</span></span>

<span data-ttu-id="8044e-116">Oltre a EAP, l'implementazione wireless (802.1 X) e il server RADIUS supportano anche uno standard emergente denominato PEAP (Protected EAP).</span><span class="sxs-lookup"><span data-stu-id="8044e-116">In addition to EAP, the wireless (802.1X) implementation and RADIUS server also support an emerging standard called Protected EAP (PEAP).</span></span>

<span data-ttu-id="8044e-117">PEAP offre diversi servizi chiave per altri protocolli di autenticazione EAP, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8044e-117">PEAP provides several key services to other EAP authentication protocols, as follows.</span></span>

-   <span data-ttu-id="8044e-118">PEAP crittografa i pacchetti EAP di altri protocolli di autenticazione EAP utilizzando Transport Layer Security (TLS), una tecnologia basata su SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="8044e-118">PEAP encrypts EAP packets of other EAP authentication protocols using Transport Layer Security (TLS), a Secure Socket Layer (SSL) based technology.</span></span> <span data-ttu-id="8044e-119">Per ulteriori informazioni, vedere [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span><span class="sxs-lookup"><span data-stu-id="8044e-119">For more information, see [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span></span>
-   <span data-ttu-id="8044e-120">PEAP autentica il lato server usando un certificato del server, con il server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="8044e-120">PEAP authenticates the server-side using a Server Certificate, with RADIUS server.</span></span>
-   <span data-ttu-id="8044e-121">PEAP offre funzionalità di riautenticazione rapida che supportano il roaming efficiente tra dispositivi wireless.</span><span class="sxs-lookup"><span data-stu-id="8044e-121">PEAP offers fast re-authentication capability that supports efficient roaming between wireless devices.</span></span>
-   <span data-ttu-id="8044e-122">PEAP gestisce la frammentazione e il riassemblaggio dei pacchetti EAP.</span><span class="sxs-lookup"><span data-stu-id="8044e-122">PEAP manages the fragmentation and re-assembly of EAP packets.</span></span>
-   <span data-ttu-id="8044e-123">PEAP genera le chiavi usate per crittografare il traffico wireless.</span><span class="sxs-lookup"><span data-stu-id="8044e-123">PEAP generates keys used for encrypting wireless traffic.</span></span>

<span data-ttu-id="8044e-124">PEAP rende molto più semplice scrivere un protocollo EAP perché il programmatore non deve più risolvere questi problemi.</span><span class="sxs-lookup"><span data-stu-id="8044e-124">PEAP makes it much easier to write an EAP protocol because the programmer no longer has to address these issues.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8044e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8044e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8044e-126">Informazioni su EAP e EAPHost</span><span class="sxs-lookup"><span data-stu-id="8044e-126">About EAP and EAPHost</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




