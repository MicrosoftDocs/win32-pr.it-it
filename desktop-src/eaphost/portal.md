---
title: Host del protocollo di autenticazione estendibile
description: Informazioni sull'host EAP (Extensible Authentication Protocol). Vedere requisiti della fase di esecuzione e visualizzare altre risorse disponibili.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104118702"
---
# <a name="extensible-authentication-protocol-host"></a><span data-ttu-id="ee553-104">Host del protocollo di autenticazione estendibile</span><span class="sxs-lookup"><span data-stu-id="ee553-104">Extensible Authentication Protocol Host</span></span>

## <a name="purpose"></a><span data-ttu-id="ee553-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="ee553-105">Purpose</span></span>


<span data-ttu-id="ee553-106">EAPHost è un componente di rete di Microsoft Windows che fornisce un'infrastruttura EAP (Extensible Authentication Protocol) per l'autenticazione di implementazioni del protocollo "supplicant", ad esempio [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) e [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span><span class="sxs-lookup"><span data-stu-id="ee553-106">EAPHost is a Microsoft Windows Networking component that provides an Extensible Authentication Protocol (EAP) infrastructure for the authentication of "supplicant" protocol implementations such as [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) and [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span></span> <span data-ttu-id="ee553-107">Consente inoltre di eseguire l'autenticazione con le tecnologie "Authenticator", ad esempio il server dei criteri di rete Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ee553-107">It also allows for authentication with "authenticator" technologies such as the Microsoft network policy server (NPS).</span></span> <span data-ttu-id="ee553-108">A differenza del server IAS precedente ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS supporta [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span><span class="sxs-lookup"><span data-stu-id="ee553-108">Unlike the previous IAS Server ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS supports [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span></span>


<span data-ttu-id="ee553-109">Le API EAPHost consentono alle applicazioni di eseguire l'autenticazione usando il servizio EAPHost e forniscono un modello per lo sviluppo di metodi di autenticazione conformi per l'uso con EAPHost.</span><span class="sxs-lookup"><span data-stu-id="ee553-109">The EAPHost APIs enable applications to authenticate using the EAPHost service, and provide a template for the development of conformant authentication methods for use with EAPHost.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ee553-110">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="ee553-110">Run-time requirements</span></span>

<span data-ttu-id="ee553-111">Le API EAPHost sono supportate solo in Windows Vista e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="ee553-111">The EAPHost APIs are supported only in Windows Vista and later operating systems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee553-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee553-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee553-113">Informazioni su EAPHost</span><span class="sxs-lookup"><span data-stu-id="ee553-113">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="ee553-114">Uso di EAPHost</span><span class="sxs-lookup"><span data-stu-id="ee553-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="ee553-115">Informazioni di riferimento sulle API EAPHost</span><span class="sxs-lookup"><span data-stu-id="ee553-115">EAPHost API Reference</span></span>](eaphost-api-reference.md)
</dt> </dl>

 

 