---
description: Cloaking è un'estensione alla rappresentazione che consente un controllo migliore sul modo in cui COM rappresenta un client su un proxy. Come molte forme di sicurezza WMI, si imposta il cloaking tramite le interfacce CoSetProxyBlanket e CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementazione del cloaking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d32333250bc37d8ccbfdb17421fed635f0da77e6394229220b2b36a1ce57f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318896"
---
# <a name="implementing-cloaking"></a>Implementazione del cloaking

Cloaking è un'estensione alla rappresentazione che consente un controllo migliore sul modo in cui COM rappresenta un client su un proxy. Come molte forme di sicurezza WMI, si imposta il cloaking tramite [**le interfacce CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) e [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

COM offre le seguenti forme di cloaking:

-   Statica

    COM stabilisce l'identità del token dal token del thread o del processo alla prima chiamata al proxy. Se si usa il cloaking statico [**con CoSetProxyBlanket,**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)si imposta l'identità del proxy per la durata del proxy.

-   Dynamic

    COM ristabilirà l'identità del token dal token del thread o del processo in ogni chiamata al proxy. Poiché COM controlla l'identità in ogni chiamata, il cloaking dinamico consente un controllo più fine sull'identità del client. Tuttavia, il cloaking dinamico è meno efficiente del cloaking statico.

Quando si imposta il cloaking in combinazione con il livello di delega di rappresentazione, un server può propagare l'identità di un client tra server, anche se i server sono remoti. Se non si abilita il cloaking, COM effettua qualsiasi chiamata da un server locale a un server remoto nel contesto del processo server effettivo.

Cloaking consente a WMI di rappresentare un client per accedere alle risorse di rete locali e remote attraverso più limiti di computer. WMI può passare l'identità del client a server locali e remoti, ad esempio altre istanze remote di WMI. Tali server remoti possono quindi eseguire operazioni nel contesto client iniziale.

La procedura seguente descrive come usare il cloaking e la delega insieme.

**Per usare cloaking e delega insieme**

1.  Impostare il servizio di autenticazione su Kerberos.

    Kerberos è l'unico servizio di autenticazione che supporta la delega e il cloaking remoto. Ciò significa che il cloaking e la delega possono essere usati solo nei server remoti.

2.  Contrassegnare l'account di accesso del server come "Trusted for Delegation" nei servizi di Active Directory.
3.  Contrassegnare l'account di accesso client come "L'account è sensibile e non può essere delegato" nei servizi Active Directory.

Ad esempio, una chiamata al provider di visualizzazione, che può restituire oggetti da più istanze di WMI in più computer, può trarre vantaggio dalla delega e dal cloaking.

 

 
