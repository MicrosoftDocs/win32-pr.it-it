---
description: È possibile usare l'interfaccia IX500DistinguishedName per creare un nome soggetto da una stringa di nome distinto.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Creazione di un nome soggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00a7350268c4b7fe5f0d6bde0630bfa7556bc8dd6085e11261456299b725dd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670211"
---
# <a name="creating-a-subject-name"></a>Creazione di un nome soggetto

È possibile usare [**l'interfaccia IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) per creare un nome soggetto da una stringa di nome distinto. La stringa è costituita da nomi distinti relativi concatenati (RDN). Le chiavi RDN seguenti sono supportate dall'API di registrazione certificati.

| Chiave                               | OID                                             | Descrizione                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | XCN \_ OID \_ COUNTRY \_ NAME<br/>              | Contiene un codice paese o area geografica ISO 3166 di due lettere.<br/>                                  |
| CN<br/>                     | NOME COMUNE OID XCN \_ \_ \_<br/>               | Contiene un nome comune.<br/>                                                                 |
| E<br/> Posta elettronica<br/>     | XCN \_ OID \_ RSA \_ emailAddr<br/>             | Contiene un indirizzo di posta elettronica.<br/>                                                              |
| DC<br/>                     | COMPONENTE DOMINIO OID XCN \_ \_ \_<br/>          | Contiene una parte di un Domain Name System (DNS).<br/>                                   |
| G<br/> GivenName<br/> | NOME OID XCN \_ \_ \_ SPECIFICATO<br/>                | Contiene la parte del nome di una persona che non è un cognome.<br/>                             |
| I<br/>                      | INIZIALI \_ OID \_ XCN<br/>                   | Contiene le iniziali di una persona.<br/>                                                           |
| L<br/>                      | XCN \_ OID \_ LOCALITY \_ NAME<br/>             | Contiene il nome della località che identifica una città, un paese o un'altra area geografica.<br/> |
| O<br/>                      | NOME ORGANIZZAZIONE OID XCN \_ \_ \_<br/>         | Contiene il nome di un'organizzazione.<br/>                                                   |
| OU<br/>                     | XCN \_ OID \_ NOME UNITÀ \_ \_ ORGANIZZATIVA<br/> | Contiene il nome di una suddivisione di unità all'interno di un'organizzazione.<br/>                         |
| S<br/> ST<br/>        | XCN \_ OID \_ STATE \_ OR \_ PROVINCE \_ NAME<br/>  | Contiene il nome completo di uno stato o di una provincia.<br/>                                          |
| STREET<br/>                 | XCN \_ OID \_ STREET \_ ADDRESS<br/>            | Contiene l'indirizzo fisico.<br/>                                                          |
| SN<br/>                     | XCN \_ OID \_ SUR \_ NAME<br/>                  | Contiene il nome della famiglia di una persona.<br/>                                                   |
| T<br/> TITLE<br/>     | XCN \_ OID \_ TITLE<br/>                      | Contiene il titolo di una persona nell'organizzazione.<br/>                                     |



 

Quando si inizializza un oggetto [**IX500DistinguishedName,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) è possibile identificare il formato del nome distinto specificando un valore dal tipo di enumerazione [**X500NameFlags.**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) Si supponga, ad esempio, che il nome distinto del soggetto sia costituito dai nomi RDN seguenti:<dl> CN=Administrator  
CN=Users  
DC=jdomcsc  
DC=nttest  
DC=microsoft  
DC=com  
</dl>

Se si concatenano questi nomi RDN nella stringa del nome distinto delimitata da virgole seguente, è possibile specificare il valore **XCN \_ CERT \_ NAME \_ STR \_ COMMA \_ FLAG** durante l'inizializzazione di un oggetto [**IX500DistinguishedName.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica di un nome soggetto](encoding-a-subject-name.md)
</dt> <dt>

[Nomi soggetto](subject-names.md)
</dt> </dl>

 

 




