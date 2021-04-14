---
title: Mapping di interfacce ADSI alle funzioni di gestione della rete
description: Le interfacce ADSI (Active Directory Service Interfaces) sono un set di interfacce COM utilizzate per accedere alle funzionalità dei servizi directory da provider di rete diversi.
ms.assetid: dfa81c58-3ce4-40ee-8bfc-a19a13781992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ec1a1055d3d016bf8b7b1bd3f357810b7ddd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339206"
---
# <a name="mapping-adsi-interfaces-to-the-network-management-functions"></a>Mapping di interfacce ADSI alle funzioni di gestione della rete

Le interfacce ADSI (Active Directory Service Interfaces) sono un set di interfacce COM utilizzate per accedere alle funzionalità dei servizi directory da provider di rete diversi. ADSI presenta un unico set di interfacce del servizio directory per la gestione delle risorse di rete in un ambiente di elaborazione distribuito.

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di interfaccia ADSI per ottenere la stessa funzionalità che è possibile ottenere chiamando determinate funzioni di gestione della rete.

Nella tabella seguente sono elencate le funzioni di gestione della rete e i gruppi di funzioni e le interfacce ADSI a cui viene mappata la funzione.



| Funzioni                                                                  | Interfacce                                                                                             |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum), [ **NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations) |
| [NetGroup](group-functions.md)\*                                          | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetLocalGroup](local-group-functions.md)\*                               | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetServer](server-functions.md)\*                                        | [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                                                  |
| [NetSession](session-functions.md)\*                                      | [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)   |
| [NetShare](share-functions.md)\*                                          | [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)                                                                |
| [NetUser](user-functions.md)\*                                            | [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser), [ **IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                   |
| [NetUserModals](user-modal-functions.md)\*                                | [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)                                                                      |



 

Per ulteriori informazioni sui servizi directory e la programmazione con ADSI, vedere [Active Directory interfacce del servizio](/windows/desktop/ADSI/active-directory-service-interfaces-adsi). Per informazioni sulle proprietà personalizzate che il provider WinNT rende disponibile per la classe utente e sui metodi di proprietà dell'interfaccia [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) che il provider WinNT non supporta, vedere [provider ADSI WinNT](/windows/desktop/ADSI/adsi-winnt-provider).

 

 