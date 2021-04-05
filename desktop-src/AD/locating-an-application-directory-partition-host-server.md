---
title: Individuazione di un server host partizione di directory applicativa
description: In questo argomento viene descritto come individuare un server host della partizione di directory applicativa.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Individuazione di un'istanza di Active Directory Partition server host
- Directory dell'applicazione partizioni di Active Directory, individuazione di un server host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707606"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Individuazione di un server host partizione di directory applicativa

Il servizio NetLogon registra l'elenco seguente di record SRV per una partizione di directory applicativa:

-   \_LDAP. \_ TCP.<partition name>
-   \_LDAP. \_ TCP. <site name> . \_ siti.<partition name>

Per individuare un controller di dominio che ospita una replica di una partizione di directory applicativa specificata, chiamare la funzione [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) con il parametro *DomainName* impostato sul nome DNS della partizione di directory applicativa e il flag **\_ solo DS \_ \_ necessario** impostato nel parametro *Flags* . Per ulteriori informazioni e un esempio di codice in cui viene illustrato, utilizzando la funzione **DsGetDcName** , come individuare un controller di dominio che ospita una replica di una partizione di directory applicativa, vedere il [codice di esempio per l'individuazione di un server host della partizione di directory applicativa](example-code-for-locating-an-application-directory-partition-host-server.md).

 

 




