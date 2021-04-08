---
description: Le funzioni seguenti sono implementate da una DLL del provider di rete per comunicare con il router multi-provider (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Funzioni implementate dai provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968300"
---
# <a name="functions-implemented-by-network-providers"></a>Funzioni implementate dai provider di rete

Le funzioni seguenti sono implementate da una DLL del provider di rete per comunicare con il [*router multi-provider*](/windows/desktop/SecGloss/m-gly) (MPR). Si noti che solo le [funzioni delle funzionalità](capabilities-functions.md) devono essere implementate da un provider di rete. L'implementazione degli altri tipi di funzioni è facoltativa e dipende dai requisiti del provider di rete.



| Set di funzioni                                                                                    | Descrizione                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funzioni funzionalità](capabilities-functions.md)<br/>                                 | Consente al chiamante di determinare le funzionalità del provider di rete.<br/>                                                                |
| [Funzioni nome utente](user-name-functions.md)<br/>                                       | Richiede al provider di rete il nome utente associato a una connessione.<br/>                                                            |
| [Funzioni di reindirizzamento del dispositivo](device-redirecting-functions.md)<br/>                     | Consente a un provider di rete di reindirizzare i dispositivi, le lettere di unità e le porte LPT standard nel sistema operativo Microsoft MS-DOS.<br/> |
| [Funzioni della finestra di dialogo specifiche del provider](provider-specific-dialog-box-functions.md)<br/> | Consente a un provider di rete di visualizzare o agire su informazioni specifiche della rete.<br/>                                                            |
| [Funzioni amministrative](administrative-functions.md)<br/>                             | Consente a un provider di rete di visualizzare o agire su directory di rete speciali.<br/>                                                             |
| [Funzioni di enumerazione](enumeration-functions.md)<br/>                                   | Consente all'utente di accedere alle risorse di rete.<br/>                                                                                            |



 

Per ulteriori informazioni su come creare e registrare un provider di rete, vedere [implementazione di un provider di rete](implementing-a-network-provider.md) e [registrazione di provider di rete e gestione credenziali](registering-network-providers-and-credential-managers.md).

 

