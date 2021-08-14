---
title: Modifica della configurazione della partizione di directory applicativa
description: Una partizione di directory applicativa può essere modificata modificando determinati attributi dell'oggetto crossRef che rappresenta la partizione di directory applicativa.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Modifica della configurazione della partizione di directory applicativa AD
- Partizioni di directory applicative AD , modifica della configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc378536a552bb7612877fc09913fdbad9daf507adbb34b5f53f8946c946e8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186316"
---
# <a name="modifying-application-directory-partition-configuration"></a>Modifica della configurazione della partizione di directory applicativa

Una partizione di directory applicativa può essere modificata modificando determinati attributi dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta la partizione di directory applicativa. Per individuare l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta una partizione di directory applicativa specifica, cercare nel contenitore Partizioni un oggetto **crossRef** con un valore di attributo [**nCName**](/windows/desktop/ADSchema/a-ncname) uguale al nome distinto della partizione di directory applicativa. Il nome distinto **dell'oggetto crossRef** può quindi essere usato per l'associazione all'oggetto **crossRef.**

Nella tabella seguente sono elencati gli attributi [**dell'oggetto crossRef**](/windows/desktop/ADSchema/c-crossref) che possono essere modificati.

| Attributo                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Specifica il ritardo, in secondi, dopo la modifica di un oggetto di origine prima della notifica del primo partner di replica. Per altre informazioni, vedere [Replica della partizione di directory applicativa](application-directory-partition-replication.md).                                                                                                   |
| [**msDS-Replication-Notify-Subsequent-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Specifica il ritardo, in secondi, tra le notifiche successive ai partner di replica secondo, terzo e così via. Per altre informazioni, vedere [Replica della partizione di directory applicativa](application-directory-partition-replication.md).                                                                                                 |
| [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifica il dominio utilizzato dal sottosistema di sicurezza per interpretare i riferimenti al dominio locale negli [**attributi nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) degli oggetti nella partizione di directory applicativa. Per altre informazioni, vedere [Application Directory Partition Security](application-directory-partition-security.md). |
| [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Contiene il nome distinto dell'oggetto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) per ogni controller di dominio che ospita una replica della partizione di directory applicativa. Per altre informazioni, vedere [Aggiunta o eliminazione di una replica di partizione di directory applicativa](adding-or-deleting-an-application-directory-partition-replica.md).            |



 

 

 