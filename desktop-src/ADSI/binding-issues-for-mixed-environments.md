---
title: Problemi di associazione per ambienti misti
description: Problemi di associazione per ambienti misti
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , uso, problemi di associazione per ambienti misti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822795e050d2b69a3f7b60aac6847a150760f35cc62806c36f14d4d6c4694a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017995"
---
# <a name="binding-issues-for-mixed-environments"></a>Problemi di associazione per ambienti misti

Per gli ambienti in cui il dominio che contiene Active Directory ha una relazione di trust con un dominio di Windows NT 4.0, potrebbe verificarsi un problema con l'uso dell'associazione serverless per l'associazione a oggetti di Active Directory.

In alcuni ambienti di rete sono state impostate relazioni di trust tra controller di dominio che contengono Active Directory e server Windows NT 4.0 allo scopo di consentire l'autenticazione tra domini. In questi ambienti misti, se un utente membro di Windows NT 4.0 tenta di usare l'associazione serverless per l'associazione a un oggetto Active Directory in un dominio trusted, l'associazione avrà esito negativo e verrà restituito un errore. Ciò è dovuto al fatto che un'associazione serverless usa la funzione [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) per eseguire l'associazione all'oggetto in Active Directory, che dipende dal DNS appropriato.

In questo scenario l'Windows NT utente deve specificare il nome di un dominio specifico a cui eseguire l'associazione. Di seguito è riportato un esempio.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 