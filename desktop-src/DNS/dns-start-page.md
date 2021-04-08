---
title: Domain Name System
description: Domain Name System (DNS), un servizio di localizzazione in Microsoft Windows, è un protocollo standard del settore che individua i computer in una rete basata su IP.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS (vedere Domain Name System)
- Domain Name System
- Domain Name System, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104058578"
---
# <a name="domain-name-system"></a>Domain Name System

## <a name="purpose"></a>Scopo

Domain Name System (DNS), un servizio di localizzazione in Microsoft Windows, è un protocollo standard del settore che individua i computer in una rete basata su IP. Le reti IP, ad esempio le reti Internet e Windows, si basano su indirizzi numerici per elaborare i dati. Gli utenti, tuttavia, possono ricordare più facilmente gli indirizzi dei nomi, pertanto è necessario convertire i nomi descrittivi (ad esempio `www.microsoft.com` ) in indirizzi che la rete è in grado di riconoscere (ad esempio 207.46.131.137).

## <a name="where-applicable"></a>Se applicabile

Windows e Active Directory utilizzano DNS. DNS è il servizio localizzatore primario per Internet e Active Directory e pertanto DNS è considerato un servizio di base per Windows e Active Directory.

## <a name="developer-audience"></a>Sviluppatori

Windows fornisce funzioni che consentono ai programmatori di applicazioni di usare DNS, ad esempio query DNS a livello di codice, confronto tra record e ricerca nome.

I componenti DNS programmabili sono progettati per l'uso da programmatori C/C++. È necessaria una certa familiarità con le funzionalità di rete e DNS. I programmatori devono conoscere la suite di protocolli IP, nonché il protocollo DNS e le operazioni DNS.

## <a name="run-time-requirements"></a>Requisiti di runtime

DNS viene usato in tutte le reti IP che richiedono un servizio localizzatore compatibile con Internet. Tuttavia, l'API DNS richiede Windows 2000 o versione successiva.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                             | Descrizione                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Documenti standard DNS](dns-standards-documents.md)<br/> | Collegamenti ai documenti degli standard DNS pubblici.<br/>                                  |
| [Informazioni su DNS](about-dns.md)<br/>                             | Informazioni generali sul DNS.<br/>                                            |
| [Riferimento DNS](dns-reference.md)<br/>                     | Documentazione di riferimento per DNS.<br/>                                          |
| [Provider WMI DNS](dns-wmi-provider.md)<br/>               | Informazioni generali e documentazione di riferimento per il provider WMI DNS.<br/> |
| [Glossario](glossary-gly.md)<br/>                           | Glossario dei termini e delle definizioni DNS.<br/>                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Helper protocollo Internet](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

[Servizi directory](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)
</dt> </dl>

 

