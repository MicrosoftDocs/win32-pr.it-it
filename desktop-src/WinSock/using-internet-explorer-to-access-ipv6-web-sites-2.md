---
description: "Microsoft Internet Explorer supporta l'utilizzo di IPv6 per la connessione e l'accesso ai siti abilitati per IPv6 (ad esempio server Web e server FTP) quando vengono soddisfatte le seguenti circostanze: il computer host che esegue Internet Explorer deve avere IPv6 installato e abilitato. Quando ci si connette a un host esterno alla subnet locale, per l'interfaccia che fornisce la connettività deve essere assegnato un indirizzo IPv6 instradabile. Quando ci si connette all'indirizzo di loopback IPv6 (:: 1) o a una destinazione locale del collegamento, non è necessario un indirizzo IPv6 instradabile. Se l'URL richiesto contiene un nome (ad esempio, www.contoso.com), la query Domain Name System (DNS) per tale nome deve restituire uno o più indirizzi IPv6. Se l'URL richiesto contiene un indirizzo IPv6 (ad esempio: 1), l'indirizzo IPv6 deve essere racchiuso tra parentesi quadre (https:// \\[ :: 1 \\] ). Gli ID ambito, a volte detti indici di zona, sono supportati come parte dell'indirizzo IPv6. L'ID ambito viene utilizzato per determinare l'interfaccia di rete da utilizzare per l'invio della richiesta nei computer con più interfacce di rete. L'ID ambito viene specificato con il carattere '%' dopo l'indirizzo IPv6 principale (ad esempio, FE80:: 1% 11). Tuttavia, il carattere '%' deve essere preceduto da un carattere di escape nell'URL utilizzato con Internet Explorer. Ad esempio, l'ambito con ID 11 in un indirizzo locale del collegamento viene specificato come https:// \\[ FE80:: 1% 2511 \\] quando si utilizza Internet Explorer. La possibilità di utilizzare indirizzi IPv6 in un URL è supportata in Internet Explorer 7 e versioni successive."
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Utilizzo di Internet Explorer per accedere ai siti Web IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d11e7b207de132441d2152a4e0593b20bc00d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316601"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Utilizzo di Internet Explorer per accedere ai siti Web IPv6

Microsoft Internet Explorer supporta l'utilizzo di IPv6 per la connessione e l'accesso ai siti abilitati per IPv6 (ad esempio, server Web e server FTP) quando vengono soddisfatte le seguenti circostanze:

-   Nel computer host che esegue Internet Explorer deve essere installato e abilitato IPv6.
    -   Quando ci si connette a un host esterno alla subnet locale, per l'interfaccia che fornisce la connettività deve essere assegnato un indirizzo IPv6 instradabile.
    -   Quando ci si connette all'indirizzo di loopback IPv6 (:: 1) o a una destinazione locale del collegamento, non è necessario un indirizzo IPv6 instradabile.
-   Se l'URL richiesto contiene un nome (ad esempio, www.contoso.com), la query Domain Name System (DNS) per tale nome deve restituire uno o più indirizzi IPv6.
-   Se l'URL richiesto contiene un indirizzo IPv6 (ad esempio: 1), l'indirizzo IPv6 deve essere racchiuso tra parentesi quadre (https:// \[ :: 1 \] ). Gli ID ambito, a volte detti indici di zona, sono supportati come parte dell'indirizzo IPv6. L'ID ambito viene utilizzato per determinare l'interfaccia di rete da utilizzare per l'invio della richiesta nei computer con più interfacce di rete. L'ID ambito viene specificato con il carattere '%' dopo l'indirizzo IPv6 principale (ad esempio, FE80:: 1% 11). Tuttavia, il carattere '%' deve essere preceduto da un carattere di escape nell'URL utilizzato con Internet Explorer. Ad esempio, l'ambito con ID 11 in un indirizzo locale del collegamento viene specificato come https:// \[ FE80:: 1% 2511 \] quando si utilizza Internet Explorer. La possibilità di utilizzare indirizzi IPv6 in un URL è supportata in Internet Explorer 7 e versioni successive.

> [!Note]  
> Se Internet Explorer è configurato per l'utilizzo di un server proxy, il server proxy deve disporre di un indirizzo IPv6 assegnato e il server proxy deve essere in grado di eseguire il proxy degli indirizzi IPv6. Il server proxy verrà usato per connettersi a un host esterno tramite IPv6. Il server proxy viene normalmente ignorato per l'indirizzo di loopback IPv6 e per gli indirizzi IPv6 locali al collegamento.

 

 

 



