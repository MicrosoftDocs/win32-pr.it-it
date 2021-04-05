---
title: Connessione a Active Directory
description: Sono disponibili diversi metodi per accedere Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Connessione a Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955107"
---
# <a name="connecting-to-active-directory"></a>Connessione a Active Directory

Sono disponibili diversi metodi per accedere Active Directory. Si consiglia di usare l'API ADSI per accedere Active Directory. ADSI implementa il protocollo LDAP per comunicare con Active Directory. Negli esempi di codice seguenti viene illustrato come accedere a Active Directory.


```VB
Set ns = GetObject("LDAP:")
```



Il provider LDAP verrà aperto e preparato per il recupero dei dati. Non viene stabilita alcuna connessione fino a quando non vengono richiesti i dati. Quando vengono richiesti dati, ADSI, con l'aiuto del servizio Locator, tenta di trovare il controller di dominio migliore per la connessione e stabilisce una connessione al server. Questo processo è noto come binding senza server.

ADSI consente inoltre di specificare il nome del server da utilizzare per la connessione.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



In un altro scenario, è possibile che si conosca solo il nome di dominio, ma non il nome del server specifico. Anche in questo caso, ADSI consente di specificare il nome di dominio. In Windows 2000, il nome di dominio è rappresentato come nome DNS. Ad esempio, se Joe worden, l'amministratore di rete sceglie di connettersi usando il nome di dominio, può usare l'esempio di codice seguente.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI si connetterà a uno dei controller di dominio nel dominio fabrikam.com.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione a oggetti Active Directory](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




