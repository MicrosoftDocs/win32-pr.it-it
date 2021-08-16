---
description: "Microsoft Internet Explorer supporta l'uso di IPv6 per connettersi e accedere a siti abilitati per IPv6 (ad esempio server Web e server FTP) quando si verificano le circostanze seguenti: nel computer host che esegue Internet Explorer deve essere installato e abilitato IPv6. Quando ci si connette a un host esterno alla subnet locale, all'interfaccia che fornisce la connettività deve essere assegnato un indirizzo IPv6 instradabile. Quando ci si connette all'indirizzo di loopback IPv6 (::1) o a una destinazione locale del collegamento, non è necessario un indirizzo IPv6 instradabile. Se l'URL richiesto contiene un nome (www.contoso.com, ad esempio), la query Domain Name System (DNS) per tale nome deve restituire uno o più indirizzi IPv6. Se l'URL richiesto contiene un indirizzo IPv6 (ad esempio::1), l'indirizzo IPv6 deve essere racchiuso tra parentesi quadre (https:// \\[ ::1 \\] ). Gli ID ambito, talvolta denominati indici di zona, sono supportati come parte dell'indirizzo IPv6. L'ID ambito viene usato per determinare l'interfaccia di rete da usare quando si invia la richiesta nei computer con più interfacce di rete. L'ID ambito viene specificato usando il carattere '%' dopo l'indirizzo IPv6 principale ,ad esempio fe80::1%11. Tuttavia, il carattere '%' deve essere preceduto da un carattere di escape nell'URL usato con Internet Explorer. Ad esempio, l'ID di ambito 11 in un indirizzo locale del collegamento viene specificato come https:// \\[ fe80::1%2511 quando si usa \\] Internet Explorer. Questa possibilità di usare indirizzi IPv6 in un URL è supportata in Internet Explorer 7 e versioni successive."
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Uso di Internet Explorer per accedere ai siti Web IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48a9f18e80e0e163ad6fe4ccda0aaef43826edd4becb28e294aad5eca7085c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559272"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Uso di Internet Explorer per accedere ai siti Web IPv6

Microsoft Internet Explorer supporta l'uso di IPv6 per connettersi e accedere a siti abilitati per IPv6 (ad esempio server Web e server FTP) quando si verificano le circostanze seguenti:

-   Nel computer host che esegue Internet Explorer deve essere installato e abilitato IPv6.
    -   Quando ci si connette a un host esterno alla subnet locale, all'interfaccia che fornisce la connettività deve essere assegnato un indirizzo IPv6 instradabile.
    -   Quando ci si connette all'indirizzo di loopback IPv6 (::1) o a una destinazione locale del collegamento, non è necessario un indirizzo IPv6 instradabile.
-   Se l'URL richiesto contiene un nome (ad esempio www.contoso.com), la query Domain Name System (DNS) per tale nome deve restituire uno o più indirizzi IPv6.
-   Se l'URL richiesto contiene un indirizzo IPv6 (ad esempio::1), l'indirizzo IPv6 deve essere racchiuso tra parentesi quadre (https:// \[ ::1 \] ). Gli ID ambito, talvolta denominati indici di zona, sono supportati come parte dell'indirizzo IPv6. L'ID ambito viene usato per determinare l'interfaccia di rete da usare quando si invia la richiesta nei computer con più interfacce di rete. L'ID ambito viene specificato usando il carattere '%' dopo l'indirizzo IPv6 principale ,ad esempio fe80::1%11. Tuttavia, il carattere '%' deve essere preceduto da un carattere di escape nell'URL usato con Internet Explorer. Ad esempio, l'ID di ambito 11 in un indirizzo locale del collegamento viene specificato come https:// \[ fe80::1%2511 quando si usa \] Internet Explorer. Questa possibilità di usare indirizzi IPv6 in un URL è supportata in Internet Explorer 7 e versioni successive.

> [!Note]  
> Se Internet Explorer è configurato per l'uso di un server proxy, è necessario che al server proxy sia assegnato un indirizzo IPv6 e che il server proxy sia in grado di eseguire il proxy degli indirizzi IPv6. Il server proxy verrà usato per connettersi a un host esterno tramite IPv6. Il server proxy verrebbe in genere ignorato per l'indirizzo di loopback IPv6 e gli indirizzi locali del collegamento IPv6.

 

 

 



