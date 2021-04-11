---
title: Motivi di non raggiungibilità
description: Nella tabella seguente sono elencati i valori costanti che indicano il motivo per cui un'interfaccia non è raggiungibile.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047094"
---
# <a name="unreachability-reasons"></a>Motivi di non raggiungibilità

Nella tabella seguente sono elencati i valori costanti che indicano il motivo per cui un'interfaccia non è raggiungibile.



| Valore                                       | Significato                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| \_amministratore interfaccia \_ MPR \_ disabilitato             | L'amministratore ha disabilitato l'interfaccia.                                                  |
| \_errore di \_ connessione dell'interfaccia MPR \_         | Il tentativo di connessione precedente non è riuscito. Esaminare il membro **dwLastError** per il codice di errore. |
| \_ \_ restrizione delle ore di connessione dell'interfaccia MPR \_ \_ | La connessione remota non è consentita all'ora corrente.                                                   |
| \_interfaccia MPR \_ \_ di \_ risorse insufficienti          | Non sono disponibili porte o dispositivi da usare.                                                     |
| \_servizio di interfaccia MPR \_ \_ sospeso             | Il servizio è in pausa.                                                                         |
| \_interfaccia MPR \_ senza \_ media \_ Sense            | Il cavo di rete è disconnesso dalla scheda di rete.                                       |
| \_interfaccia MPR \_ senza \_ dispositivo                  | La scheda di rete è stata rimossa dal computer.                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_Interfaccia MPR \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**\_Interfaccia MPR \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**\_IFROW MIB**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**\_IFSTATUS MIB**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 