---
title: Connessione ad Active Directory
description: Esistono diversi metodi usati per accedere ad Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Connessione ad Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6afd5aa0edd8a4c4a87bae7cde6a135fc3467771eed2dbc0cb7673984040832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692009"
---
# <a name="connecting-to-active-directory"></a>Connessione ad Active Directory

Esistono diversi metodi usati per accedere ad Active Directory. È consigliabile usare l'API ADSI per accedere ad Active Directory. ADSI implementa il protocollo LDAP per comunicare con Active Directory. Gli esempi di codice seguenti illustrano come accedere ad Active Directory.


```VB
Set ns = GetObject("LDAP:")
```



Verrà aperto il provider LDAP e preparato per recuperare i dati. Non viene stabilita alcuna connessione fino a quando non vengono richiesti dati. Quando vengono richiesti dati, ADSI, con l'aiuto del servizio localizzatore, tenta di trovare il controller di dominio migliore per la connessione e stabilirà una connessione al server. Questo processo è noto come associazione serverless.

ADSI consente anche di specificare il nome del server da utilizzare per la connessione.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



In un altro scenario è possibile conoscere solo il nome di dominio, ma non il nome del server specifico. Anche in questo caso, ADSI consente di specificare il nome di dominio. In Windows 2000 il nome di dominio è rappresentato come nome DNS. Ad esempio, se Joe Worden, l'amministratore di rete, sceglie di connettersi usando il nome di dominio, potrebbe usare l'esempio di codice seguente.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI si connetterà a uno dei controller di dominio nel fabrikam.com dominio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione a oggetti di Active Directory](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




