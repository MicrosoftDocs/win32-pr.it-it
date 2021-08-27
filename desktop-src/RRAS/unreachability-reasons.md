---
title: Motivi di non raggiungibilità
description: Nella tabella seguente sono elencati i valori costanti che indicano il motivo per cui un'interfaccia non è raggiungibile.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb833409d9d2ba31adedbc2942d39399c0a5763ad4d65dc7cdcaf234f97efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025411"
---
# <a name="unreachability-reasons"></a>Motivi di non raggiungibilità

Nella tabella seguente sono elencati i valori costanti che indicano il motivo per cui un'interfaccia non è raggiungibile.



| Valore                                       | Significato                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| AMMINISTRATORE \_ DELL'INTERFACCIA \_ MPR \_ DISABILITATO             | L'amministratore ha disabilitato l'interfaccia.                                                  |
| ERRORE DI \_ CONNESSIONE \_ DELL'INTERFACCIA \_ MPR         | Il tentativo di connessione precedente non è riuscito. Esaminare il membro **dwLastError** per il codice di errore. |
| RESTRIZIONE DELLE \_ ORE \_ DI DIALOUT \_ DELL'INTERFACCIA \_ MPR | La connessione remota non è consentita al momento.                                                   |
| INTERFACCIA MPR \_ \_ FUORI \_ RISORSE \_          | Non sono disponibili porte o dispositivi per l'uso.                                                     |
| SERVIZIO DI \_ INTERFACCIA MPR \_ \_ SOSPESO             | Il servizio è in pausa.                                                                         |
| INTERFACCIA MPR \_ \_ NO MEDIA \_ \_ SENSE            | Il cavo di rete è disconnesso dalla scheda di rete.                                       |
| INTERFACCIA MPR \_ \_ NESSUN \_ DISPOSITIVO                  | La scheda di rete è stata rimossa dal computer.                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**INTERFACCIA MPR \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**INTERFACCIA MPR \_ \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**MIB \_ IFROW**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**MIB \_ IFSTATUS**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 