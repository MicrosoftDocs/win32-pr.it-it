---
title: Individuazione di un server host della partizione di directory applicativa
description: In questo argomento viene descritto come individuare un server host della partizione di directory applicativa.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Individuazione di un server host della partizione di directory applicativa AD
- Partizioni di directory applicative AD, individuazione di un server host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3cef9442d694b80893f67d5530b83aa188df4d172028271117492ed221bd239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186792"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Individuazione di un server host della partizione di directory applicativa

Il servizio NetLogon registra l'elenco seguente di record SRV per una partizione di directory applicativa:

-   \_ldap. \_ Tcp.<partition name>
-   \_ldap. \_ tcp. <site name> . \_ Siti.<partition name>

Per individuare un controller di dominio che ospita una replica di una partizione di directory applicativa specificata, chiamare la funzione [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) con il parametro *DomainName* impostato sul nome DNS della partizione di directory applicativa e il flag **\_ DS ONLY \_ LDAP \_ NEEDED** impostato nel parametro *Flags.* Per altre informazioni e un esempio di codice che illustra, usando la funzione **DsGetDcName,** come individuare un controller di dominio che ospita una replica di una partizione di directory applicativa, vedere Codice di esempio per l'individuazione di un server host della partizione di [directory applicativa](example-code-for-locating-an-application-directory-partition-host-server.md).

 

 




