---
description: Le funzioni seguenti vengono implementate da una DLL del provider di rete per comunicare con il router a più provider.
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Funzioni implementate dai provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892bcb5c19f54e5de667eb72119f6b9e5fc9b183b8d5038ce37b7e556ae5d3a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016321"
---
# <a name="functions-implemented-by-network-providers"></a>Funzioni implementate dai provider di rete

Le funzioni seguenti vengono implementate da una DLL del provider di rete per comunicare con [*il router a più provider.*](/windows/desktop/SecGloss/m-gly) Si noti che solo le [funzioni di funzionalità](capabilities-functions.md) devono essere implementate da un provider di rete. L'implementazione degli altri tipi di funzioni è facoltativa e dipende dai requisiti del provider di rete.



| Set di funzioni                                                                                    | Descrizione                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funzioni di funzionalità](capabilities-functions.md)<br/>                                 | Consente al chiamante di determinare le funzionalità del provider di rete.<br/>                                                                |
| [Funzioni del nome utente](user-name-functions.md)<br/>                                       | Richiede al provider di rete il nome utente associato a una connessione.<br/>                                                            |
| [Funzioni di reindirizzamento dei dispositivi](device-redirecting-functions.md)<br/>                     | Consente a un provider di rete di reindirizzare i dispositivi, le lettere di unità e le porte LPT standard nel sistema operativo Microsoft MS-DOS.<br/> |
| [Funzioni della finestra di dialogo specifiche del provider](provider-specific-dialog-box-functions.md)<br/> | Consente a un provider di rete di visualizzare o agire su informazioni specifiche della rete.<br/>                                                            |
| [Funzioni amministrative](administrative-functions.md)<br/>                             | Consente a un provider di rete di visualizzare o agire su directory di rete speciali.<br/>                                                             |
| [Funzioni di enumerazione](enumeration-functions.md)<br/>                                   | Consente all'utente di esplorare le risorse di rete.<br/>                                                                                            |



 

Per altre informazioni su come creare e registrare un provider di rete, vedere [Implementazione](implementing-a-network-provider.md) di un provider di rete e Registrazione di provider di [rete e gestori credenziali](registering-network-providers-and-credential-managers.md).

 

