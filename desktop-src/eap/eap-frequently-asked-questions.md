---
title: Domande frequenti sul protocollo EAP
description: Trovare le risposte alle domande frequenti sulle API EAP, ad esempio "Qual è la durata di un'autenticazione EAP?".
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08713b17491d4b0bd76540c09b9d4588116256f
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "103963616"
---
# <a name="eap-frequently-asked-questions"></a>Domande frequenti sul protocollo EAP

Nell'argomento seguente vengono fornite le risposte alle domande frequenti sulle API EAP.



| Domanda                                                                                        | Risposta                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Qual è la durata di un'autenticazione EAP?                                                  | In una situazione tipica l'autenticazione è costituita da tutto ciò che si verifica tra la chiamata delle funzioni [**RapEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) e [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) . Quando un utente sceglie di configurare un provider EAP nello snap-in RRAS, un'autenticazione è costituita da tutto ciò che si verifica tra la chiamata dei metodi [**Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) e [**Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize) .<br/> |
| Che cos'è "criteri di gruppo"?                                                                         | Per una descrizione dei criteri di gruppo, vedere [criteri di gruppo Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).                                                                                                                                                                                                                                                                                                                                                    |
| Le funzioni EAP possono eseguire l'override dei criteri di configurazione specificati da criteri di gruppo?                      | No, mai. Se criteri di gruppo è in uso, le impostazioni di criteri di gruppo eseguiranno sempre l'override delle impostazioni di configurazione EAP.                                                                                                                                                                                                                                                                                                                                                         |
| È necessario avvisare gli utenti dei tentativi di PIN non validi. È possibile acquisire un codice PIN non valido? | Quando l'utente immette il PIN errato, Extensible Authentication Protocol-Transport Layer Security (EAP-TLS) invierà un codice di errore al supplicant VPN. Quando viene restituito un codice di errore, il richiedente può implementare la logica di ripetizione dei tentativi preferita.                                                                                                                                                                                                                    |
| Che cos'è la sicurezza a livello di EAP-Transport (EAP-TLS)?                                                 | EAP-TLS è un protocollo client-server in cui i profili certificato distinti vengono in genere usati per il client e il server. Per ulteriori informazioni, vedere [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Extensible Authentication Protocol](using-extenstible-authentication-protocol.md)
</dt> </dl>