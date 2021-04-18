---
title: Problemi di binding per ambienti misti
description: Problemi di binding per ambienti misti
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilizzo, associazione di problemi per ambienti misti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300420"
---
# <a name="binding-issues-for-mixed-environments"></a>Problemi di binding per ambienti misti

Per gli ambienti in cui il dominio che contiene Active Directory dispone di una relazione di trust con un dominio di Windows NT 4,0, potrebbe essersi verificato un problema nell'utilizzo del binding senza server per l'associazione agli oggetti Active Directory.

In alcuni ambienti di rete sono state configurate relazioni di trust tra controller di dominio contenenti Active Directory e server Windows NT 4,0 allo scopo di consentire l'autenticazione tra domini. In questi ambienti misti, se un utente che è membro di Windows NT 4,0, il dominio tenta di usare un'associazione senza server per eseguire l'associazione a un oggetto Active Directory in un dominio trusted, l'associazione non riuscirà e verrà restituito un errore. Ciò è dovuto al fatto che un'associazione senza server utilizza la funzione [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) per eseguire l'associazione all'oggetto in Active Directory, che dipende dal DNS appropriato.

In questo scenario, è necessario che l'utente di Windows NT fornisca il nome di un dominio specifico a cui eseguire l'associazione. Di seguito è riportato un esempio.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 