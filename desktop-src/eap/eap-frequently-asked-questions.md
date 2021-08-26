---
title: Domande frequenti su EAP
description: Risposte alle domande frequenti sulle API EAP, ad esempio "Qual è la durata di un'autenticazione EAP?".
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a8b424ed195d30621c67007fc8e7d1a0882bae6ce676c70a1ca0dc93e8b846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978531"
---
# <a name="eap-frequently-asked-questions"></a>Domande frequenti su EAP

L'argomento seguente fornisce le risposte alle domande frequenti sulle API EAP.



| Domanda                                                                                        | Risposta                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Qual è la durata di un'autenticazione EAP?                                                  | In una situazione tipica l'autenticazione è costituita da tutto ciò che si verifica tra la chiamata [**delle funzioni RapEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) [**e RasEapEnd.**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) Quando un utente sceglie di configurare un provider EAP nello snap-in RRAS, un'autenticazione è costituita da tutto ciò che si verifica tra la chiamata dei metodi [**Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) e [**Uninitialize.**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize)<br/> |
| Che cos'è "Criteri di gruppo"?                                                                         | Per una descrizione dei criteri di gruppo, [vedere Criteri di gruppo Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).                                                                                                                                                                                                                                                                                                                                                    |
| Le funzioni EAP possono eseguire l'override dei criteri di configurazione specificati da Criteri di gruppo?                      | No, mai. Se i criteri di gruppo sono in uso, le impostazioni di Criteri di gruppo eseguiranno sempre l'override delle impostazioni di configurazione EAP.                                                                                                                                                                                                                                                                                                                                                         |
| È necessario avvisare gli utenti dei tentativi di PIN non validi. È possibile acquisire un codice PIN non valido? | Quando l'utente immette il PIN errato, Extensible Authentication Protocol-Transport Layer Security (EAP-TLS) invierà un codice di errore al supplicant VPN. Una volta restituito un codice di errore, il supplicante può implementare la logica di ripetizione dei tentativi preferita.                                                                                                                                                                                                                    |
| Che cos'EAP-Transport livello di sicurezza (EAP-TLS)?                                                 | EAP-TLS è un protocollo client-server in cui profili certificato distinti vengono in genere usati per il client e il server. Per altre informazioni, vedere [IETF RTC 2716.](/previous-versions/windows/embedded/ms885336(v=msdn.10))<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Extensible Authentication Protocol](using-extenstible-authentication-protocol.md)
</dt> </dl>