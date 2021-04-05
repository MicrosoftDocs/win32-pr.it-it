---
title: Modifica della configurazione della partizione di directory applicativa
description: Per modificare una partizione di directory applicativa, è possibile modificare determinati attributi dell'oggetto crossRef che rappresenta la partizione di directory applicativa.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Modifica della configurazione della partizione di directory applicativa AD
- Directory dell'applicazione partizioni di Active Directory, modifica della configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c976c297e8491dbb87a32cf2241446ca0403e7f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872294"
---
# <a name="modifying-application-directory-partition-configuration"></a>Modifica della configurazione della partizione di directory applicativa

Per modificare una partizione di directory applicativa, è possibile modificare determinati attributi dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta la partizione di directory applicativa. Per individuare l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta una determinata partizione di directory applicativa, cercare nel contenitore partizioni un oggetto **crossRef** con un valore di attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) uguale al nome distinto della partizione di directory applicativa. Il nome distinto dell'oggetto **crossRef** può quindi essere utilizzato per l'associazione all'oggetto **crossRef** .

Nella tabella seguente sono elencati gli attributi dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che è possibile modificare.

| Attributo                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Specifica il ritardo, in secondi, dopo la modifica di un oggetto di origine prima della notifica del primo partner di replica. Per altre informazioni, vedere [replica della partizione di directory applicativa](application-directory-partition-replication.md).                                                                                                   |
| [**msDS-Replication-Notify-successivo-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Specifica il ritardo, in secondi, tra le notifiche successive e la seconda, la terza e così via sui partner di replica. Per altre informazioni, vedere [replica della partizione di directory applicativa](application-directory-partition-replication.md).                                                                                                 |
| [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifica il dominio utilizzato dal sottosistema di sicurezza per interpretare i riferimenti di dominio locali negli attributi [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) degli oggetti nella partizione di directory applicativa. Per altre informazioni, vedere [sicurezza della partizione di directory applicativa](application-directory-partition-security.md). |
| [**msDS-NC-replica-posizioni**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Contiene il nome distinto dell'oggetto [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) per ogni controller di dominio che ospita una replica della partizione di directory applicativa. Per ulteriori informazioni, vedere [aggiunta o eliminazione di una replica della partizione di directory applicativa](adding-or-deleting-an-application-directory-partition-replica.md).            |



 

 

 