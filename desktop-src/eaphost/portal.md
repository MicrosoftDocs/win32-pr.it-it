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
# <a name="extensible-authentication-protocol-host"></a>Host del protocollo di autenticazione estendibile

## <a name="purpose"></a>Scopo


EAPHost è un componente di rete di Microsoft Windows che fornisce un'infrastruttura EAP (Extensible Authentication Protocol) per l'autenticazione di implementazioni del protocollo "supplicant", ad esempio [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) e [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP). Consente inoltre di eseguire l'autenticazione con le tecnologie "Authenticator", ad esempio il server dei criteri di rete Microsoft. A differenza del server IAS precedente ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS supporta [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP).


Le API EAPHost consentono alle applicazioni di eseguire l'autenticazione usando il servizio EAPHost e forniscono un modello per lo sviluppo di metodi di autenticazione conformi per l'uso con EAPHost.

## <a name="run-time-requirements"></a>Requisiti di runtime

Le API EAPHost sono supportate solo in Windows Vista e nei sistemi operativi successivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su EAPHost](about-eap-host.md)
</dt> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> <dt>

[Informazioni di riferimento sulle API EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 