---
description: Quando si utilizza il servizio eventi COM+, è possibile eseguire alcune operazioni per garantire che le informazioni riservate contenute in un evento non vengano compromesse.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Considerazioni sulla sicurezza degli eventi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966381"
---
# <a name="com-events-security-considerations"></a>Considerazioni sulla sicurezza degli eventi COM+

Quando si utilizza il servizio eventi COM+, è possibile eseguire alcune operazioni per garantire che le informazioni riservate contenute in un evento non vengano compromesse.

Gli autori di eventi devono tenere presente che tutte le parti in grado di scrivere nel catalogo COM+ possono sottoscrivere gli eventi. Se pertanto le informazioni contenute in un oggetto classe di evento sono sensibili, è necessario utilizzare lo strumento di amministrazione Servizi componenti per verificare che le comunicazioni con i sottoscrittori siano crittografate per l'applicazione che contiene i componenti della classe di evento. Nella scheda **sicurezza** della finestra delle proprietà dell'applicazione com+ selezionare **pacchetto privacy** come **livello di autenticazione per le chiamate** impostazione. Inoltre, è necessario utilizzare i [filtri eventi](filtering-events-in-com-.md) per garantire che gli eventi vengano recapitati solo ai sottoscrittori appropriati.

I sottoscrittori di eventi devono tenere presente che un utente malintenzionato con accesso alla rete e conoscere l'oggetto della classe di evento potrebbe creare falsi eventi. È quindi consigliabile usare la [sicurezza basata sui ruoli](role-based-security-administration.md) per garantire che i chiamanti dei metodi dell'oggetto della classe di evento dispongano delle credenziali appropriate per eseguire le azioni descritte dall'implementazione di.

Per proteggere sia i Publisher che i sottoscrittori, utilizzare il servizio eventi COM+ in una rete privata di host attendibili che è isolata da Internet da un firewall.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza COM+](com--security.md)
</dt> <dt>

[Filtro di eventi in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Oggetto della classe di evento COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



