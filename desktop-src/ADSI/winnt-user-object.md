---
title: Oggetto utente WinNT
description: L'oggetto utente WinNT rappresenta un account utente in un dominio Windows NT 4,0.
ms.assetid: c57016e2-538b-4f37-a1bb-699fcf3c080d
ms.tgt_platform: multiple
keywords:
- Oggetto utente WinNT ADSI
- ADSI del provider WinNT, oggetto utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2448fbc7cd77be9c76290777b16e23b2f7e97e61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955070"
---
# <a name="winnt-user-object"></a>Oggetto utente WinNT

L'oggetto utente WinNT rappresenta un account utente in un dominio Windows NT 4,0. L'oggetto presenta funzionalità speciali. In un'istanza di non sono supportati tutti i metodi di proprietà dell'interfaccia [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) . In una seconda istanza, supporta alcune proprietà personalizzate a cui è possibile accedere solo con il metodo [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) .

Per ulteriori informazioni sugli oggetti utente WinNT, vedere:

-   [Proprietà IADsUser non supportate](unsupported-iadsuser-properties.md)
-   [Proprietà utente personalizzate WinNT](winnt-custom-user-properties.md)
-   [Esempi di gestione degli account utente WinNT](winnt-user-account-management-examples.md)

 

 




