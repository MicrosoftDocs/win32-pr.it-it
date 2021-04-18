---
description: È possibile usare l'interfaccia IX500DistinguishedName per creare un nome soggetto da una stringa del nome distinto.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Creazione di un nome soggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525098"
---
# <a name="creating-a-subject-name"></a>Creazione di un nome soggetto

È possibile usare l'interfaccia [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) per creare un nome soggetto da una stringa del nome distinto. La stringa è costituita da nomi distinti relativi concatenati (RDNs). Le chiavi RDN seguenti sono supportate dall'API di registrazione del certificato.

| Chiave                               | OID                                             | Descrizione                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | \_nome del \_ paese \_ OID XCN<br/>              | Contiene un codice paese o area ISO 3166 di due lettere.<br/>                                  |
| CN<br/>                     | \_ \_ nome comune OID \_ XCN<br/>               | Contiene un nome comune.<br/>                                                                 |
| E<br/> Posta elettronica<br/>     | \_OID XCN \_ RSA \_ emailAddr<br/>             | Contiene un indirizzo di posta elettronica.<br/>                                                              |
| DC<br/>                     | \_componente di \_ dominio \_ OID XCN<br/>          | Contiene una parte di un nome di Domain Name System (DNS).<br/>                                   |
| G<br/> GivenName<br/> | \_nome OID \_ XCN \_<br/>                | Contiene la parte del nome di una persona che non è un cognome.<br/>                             |
| I<br/>                      | \_iniziali OID \_ XCN<br/>                   | Contiene le iniziali di una persona.<br/>                                                           |
| L<br/>                      | nome della località di XCN \_ OID \_ \_<br/>             | Contiene il nome della località che identifica una città, un paese o un'altra area geografica.<br/> |
| O<br/>                      | \_ \_ nome organizzazione OID \_ XCN<br/>         | Contiene il nome di un'organizzazione.<br/>                                                   |
| OU<br/>                     | \_ \_ \_ nome unità organizzativa OID \_ XCN<br/> | Contiene il nome di una suddivisione di unità in un'organizzazione.<br/>                         |
| S<br/> ST<br/>        | \_nome della \_ \_ provincia o \_ dello stato OID XCN \_<br/>  | Contiene il nome completo di uno stato o di una provincia.<br/>                                          |
| STREET<br/>                 | XCN \_ OID \_ via \_<br/>            | Contiene l'indirizzo fisico.<br/>                                                          |
| SN<br/>                     | \_nome XCN OID \_ sur \_<br/>                  | Contiene il nome della famiglia di una persona.<br/>                                                   |
| T<br/> TITLE<br/>     | \_titolo OID \_ XCN<br/>                      | Contiene il titolo di una persona dell'organizzazione.<br/>                                     |



 

Quando si Inizializza un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , è possibile identificare il formato del nome distinto specificando un valore del tipo di enumerazione [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) . Si supponga, ad esempio, che il nome distinto del soggetto sia costituito dai seguenti RDNs:<dl> CN = amministratore  
CN = utenti  
DC = jdomcsc  
DC = nttest  
DC = Microsoft  
DC = com  
</dl>

Se si concatenano questi RDNs nella seguente stringa del nome distinto delimitato da virgole, è possibile specificare il valore del **\_ \_ \_ \_ \_ flag virgola Str del nome del certificato XCN** per l'inizializzazione di un oggetto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica di un nome soggetto](encoding-a-subject-name.md)
</dt> <dt>

[Nomi soggetto](subject-names.md)
</dt> </dl>

 

 




