---
description: Il cloaking è un'estensione della rappresentazione che consente di controllare meglio il modo in cui COM rappresenta un client su un proxy. Analogamente a molte forme di sicurezza WMI, è possibile impostare il cloaking tramite le interfacce CoSetProxyBlanket e CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementazione del mascheramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232629"
---
# <a name="implementing-cloaking"></a>Implementazione del mascheramento

Il cloaking è un'estensione della rappresentazione che consente di controllare meglio il modo in cui COM rappresenta un client su un proxy. Analogamente a molte forme di sicurezza WMI, è possibile impostare il cloaking tramite le interfacce [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

COM offre le seguenti forme di mascheramento:

-   Static

    COM stabilisce l'identità del token dal thread o dal token del processo nella prima chiamata al proxy. Se si usa il cloaking statico con [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), si imposta l'identità del proxy per il ciclo di vita del proxy.

-   Dynamic

    COM ristabilisce l'identità del token dal thread o dal token del processo a ogni chiamata al proxy. Poiché COM controlla l'identità a ogni chiamata, il cloaking dinamico consente un controllo più preciso sull'identità del client. Tuttavia, il mascheramento dinamico è meno efficiente del mascheramento statico.

Quando si imposta il cloaking insieme al livello di delega della rappresentazione, un server può propagare l'identità di un client tra i server, anche se i server sono remoti. Se non si Abilita il mascheramento, COM effettua qualsiasi chiamata da un server locale a un server remoto nel contesto del processo server effettivo.

Il mascheramento consente a WMI di rappresentare un client per accedere alle risorse di rete locali e remote tra più limiti del computer. WMI può passare l'identità del client ai server locali e remoti, ad esempio altre istanze remote di WMI. Tali server remoti possono quindi eseguire operazioni nel contesto client iniziale.

Nella procedura seguente viene descritto come utilizzare il mascheramento e la delega insieme.

**Per utilizzare il mascheramento e la delega insieme**

1.  Impostare il servizio di autenticazione su Kerberos.

    Kerberos è l'unico servizio di autenticazione che supporta il mascheramento e la delega remote. Ciò significa che il mascheramento e la delega possono essere utilizzati solo su server remoti.

2.  Contrassegnare l'account di accesso del server come "trusted per la delega" nei servizi Active Directory.
3.  Contrassegnare l'account di accesso client come "l'account è sensibile e non può essere delegato" nei servizi Active Directory.

Ad esempio, una chiamata al provider di visualizzazione, che può restituire oggetti da più istanze di WMI su più computer, può trarre vantaggio dalla delega e dal mascheramento.

 

 
