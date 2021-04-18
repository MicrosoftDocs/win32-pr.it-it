---
description: L' \_ \_ opzione socket del livello di protezione IPv6 consente agli sviluppatori di inserire restrizioni di accesso sui socket IPv6.
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306938"
---
# <a name="ipv6_protection_level"></a>\_Livello di protezione IPv6 \_

L' \_ \_ opzione socket del livello di protezione IPv6 consente agli sviluppatori di inserire restrizioni di accesso sui socket IPv6. Tali restrizioni consentono a un'applicazione in esecuzione su una LAN privata di proteggersi in modo semplice e affidabile da attacchi esterni. L' \_ \_ opzione socket del livello di protezione IPv6 allarga o restringe l'ambito di un socket in ascolto, abilitando l'accesso illimitato da parte di utenti pubblici e privati, quando appropriato, o limitando l'accesso solo allo stesso sito, in base alle esigenze.

Il \_ livello di protezione IPv6 \_ dispone attualmente di tre livelli di protezione definiti.



| Livello di protezione                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>livello di protezione \_ \_ senza restrizioni<br/>       | Usato dalle applicazioni progettate per operare su Internet, incluse le applicazioni che sfruttano le funzionalità di attraversamento NAT IPv6 incorporate in Windows (ad esempio, Teredo). Tali applicazioni possono aggirare i firewall IPv4 e pertanto le applicazioni devono essere protette contro gli attacchi provenienti da Internet diretti alla porta aperta.<br/> |
| <span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>livello di protezione \_ \_ EDGERESTRICTED<br/> | Utilizzato dalle applicazioni progettate per operare in Internet. Questa impostazione non consente l'attraversamento NAT tramite l'implementazione di Windows Teredo. Tali applicazioni possono aggirare i firewall IPv4 e pertanto le applicazioni devono essere protette contro gli attacchi provenienti da Internet diretti alla porta aperta.<br/>                                   |
| <span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>livello di protezione \_ \_ limitato<br/>             | Utilizzato dalle applicazioni Intranet che non implementano scenari Internet. Queste applicazioni non sono in genere testate o protette da attacchi analoghi a quelli provenienti da Internet.<br/> Questa impostazione limiterà il traffico ricevuto solo a quello locale rispetto al collegamento.<br/>                                                                             |



 

Nell'esempio di codice seguente vengono forniti i valori definiti per ogni:

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

Questi valori si escludono reciprocamente e non possono essere combinati in una singola chiamata di funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) . Gli altri valori per questa opzione socket sono riservati. I livelli di protezione sono validi solo per le connessioni in ingresso. L'impostazione di questa opzione socket non ha alcun effetto sui pacchetti o le connessioni in uscita.

In Windows 7 e Windows Server 2008 R2, il valore predefinito per il \_ livello di protezione IPv6 non \_ è specificato e il **livello di protezione \_ \_ predefinito** è impostato su-1, un valore non valido per il \_ livello di protezione IPv6 \_ .

In Windows Vista e Windows Server 2008, il valore predefinito per il \_ livello di protezione IPv6 \_ è **\_ \_ senza restrizioni** e **il \_ livello \_ di protezione predefinito** è impostato su-1, un valore non valido per il \_ livello di protezione IPv6 \_ .

In Windows Server 2003 e Windows XP, il valore predefinito per il livello di protezione IPV6 è il livello \_ \_ di protezione **\_ \_ EDGERESTRICTED** e il **livello di protezione \_ \_ predefinito** è definito come **\_ \_ EDGERESTRICTED** del livello di protezione.

> [!Note]  
> \_ \_ È necessario impostare l'opzione socket del livello di protezione IPv6 prima che il socket venga associato. In caso contrario, i pacchetti ricevuti tra le chiamate [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) saranno conformi al **livello di protezione \_ \_ EDGERESTRICTED** e possono essere recapitati all'applicazione.

 

Nella tabella seguente viene descritto l'effetto dell'applicazione di ogni livello di protezione a un socket in ascolto.

Livello di protezione

Traffico in ingresso consentito

Stesso sito

Esterno

Attraversamento NAT (Teredo)

livello di protezione \_ \_ limitato

Sì

No

No

livello di protezione \_ \_ EDGERESTRICTED

Sì

Sì

No

livello di protezione \_ \_ senza restrizioni

Sì

Sì

Sì



 

Nella tabella precedente la stessa colonna del **sito** è una combinazione dei seguenti elementi:

-   Collega indirizzi locali
-   Indirizzi locali del sito
-   Indirizzi globali noti come appartenenti allo stesso sito (che corrisponde alla tabella del prefisso del sito)

In Windows 7 e Windows Server 2008 R2, il valore predefinito per il \_ livello di protezione IPv6 non \_ è specificato. Se sul computer locale non è installato alcun software firewall compatibile con l'attraversamento del perimetro (Windows Firewall è disabilitato o è installato un altro firewall che ignora il traffico Teredo), si riceverà il traffico Teredo solo se si imposta l' \_ opzione del socket del livello di protezione IPv6 sul \_ **livello di protezione \_ \_ senza restrizioni**. Tuttavia, Windows Firewall o qualsiasi criterio del firewall compatibile con attraversamento del perimetro potrebbe ignorare questa opzione in base alle impostazioni dei criteri per il firewall. Impostando questa opzione del socket **sul \_ livello di protezione \_ senza restrizioni**, l'applicazione comunica l'intento esplicito di ricevere il traffico attraversato da Edge dal firewall host installato nel computer locale. Quindi, se è installato un firewall host compatibile con l'attraversamento del perimetro, avrà la decisione finale sull'accettazione di un pacchetto. Per impostazione predefinita, senza set di opzioni socket:

-   o se Windows Firewall è abilitato (o se è installato un altro firewall host che supporta l'attraversamento del perimetro) nel computer locale, qualunque sia l'applicazione applicata verrà osservato. Il firewall host in grado di riconoscere il bordo tipico bloccherà il traffico Teredo per impostazione predefinita. Pertanto, le applicazioni osserveranno il valore predefinito come se si trattasse di un **livello di protezione \_ \_ EDGERESTRICTED**.
-   o se Windows Firewall non è abilitato e nessun altro firewall host compatibile con l'attraversamento del perimetro è installato nel sistema locale, il valore predefinito sarà il **livello di protezione \_ \_ EDGERESTRICTED**.

In Windows Vista e Windows Server 2008, il valore predefinito per il \_ livello di protezione IPv6 \_ è **\_ \_ Unrestricted Level Protection**. Tuttavia, il valore effettivo varia a seconda che Windows Firewall sia abilitato o meno. Windows Firewall è compatibile con l'attraversamento del perimetro (compatibile con Teredo), indipendentemente dal valore impostato per il livello di protezione IPV6 e ignora se il livello di protezione \_ \_ IPv6 \_ \_ è **\_ \_ senza restrizioni**. Il valore effettivo dipende quindi dal criterio del firewall. Quando Windows Firewall è disabilitato e nel computer locale non è installato altro firewall per l'attraversamento del perimetro, il valore predefinito per il \_ livello di protezione IPv6 \_ è senza **\_ \_ restrizioni**.

In Windows Server 2003 e Windows XP, il valore predefinito per il \_ livello di protezione IPv6 \_ è il livello di **protezione \_ \_ EDGERESTRICTED**. A meno che non sia stata impostata \_ l' \_ opzione socket del livello di protezione IPv6 sul **livello di protezione senza \_ \_ restrizioni**, non si riceverà alcun traffico Teredo.

A seconda del \_ \_ livello di protezione IPv6, un'applicazione che richiede traffico non richiesto da Internet potrebbe non essere in grado di ricevere traffico non richiesto. Tuttavia, questi requisiti non sono necessari per la ricezione di traffico richiesto sull'interfaccia Teredo di Windows. Per altri dettagli sull'interazione con Teredo, vedere [ricezione di traffico richiesto su Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).

Quando i pacchetti in ingresso o le connessioni vengono rifiutate a causa del livello di protezione impostato, il rifiuto viene gestito come se nessuna applicazione fosse in ascolto su tale socket.

> [!Note]
>
> L' \_ \_ opzione socket del livello di protezione IPv6 non pone necessariamente restrizioni di accesso sui socket IPv6 o limita l'attraversamento NAT usando un metodo diverso da Windows Teredo o persino usando un'altra implementazione di Teredo da parte di un altro fornitore.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[Ricezione di traffico richiesto su Teredo](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
