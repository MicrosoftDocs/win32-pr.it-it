---
description: A partire da Windows Vista, Gestione controllo servizi (SCM) supporta le chiamate di procedura remota su Transmission Control Protocol (RPC/TCP) e named pipe (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Servizi e RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d4ddfe95e114a972c600c9bef44864aa99fbe4ec412312d03e08fa7d7fe15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888558"
---
# <a name="services-and-rpctcp"></a>Servizi e RPC/TCP

A partire da Windows Vista, Gestione controllo servizi (SCM) supporta le chiamate di procedura remota su Transmission Control Protocol (RPC/TCP) e named pipe (RPC/NP). Le funzioni SCM sul lato client usano RPC/TCP per impostazione predefinita.

RPC/TCP è appropriato per la maggior parte delle applicazioni che usano funzioni SCM in modalità remota, ad esempio strumenti di amministrazione remota o di monitoraggio. Tuttavia, per motivi di compatibilità e prestazioni, alcune applicazioni potrebbero dover disabilitare RPC/TCP impostando i valori del Registro di sistema descritti in questo argomento.

Quando un servizio chiama una funzione SCM remota, SCM sul lato client tenta prima di tutto di usare RPC/TCP per comunicare con SCM sul lato server. Se il server esegue una versione di Windows che supporta RPC/TCP e consente il traffico RPC/TCP, la connessione RPC/TCPP avrà esito positivo. Se il server esegue una versione di Windows che non supporta RPC/TCP o supporta RPC/TCP, ma funziona dietro un firewall che consente solo il traffico named pipe, si verifica il timeout della connessione RPC/TCP e gestione controllo servizi ritenta la connessione con RPC/NP. Questa operazione avrà esito positivo alla fine, ma può richiedere del tempo (in genere più di 20 secondi), causando il blocco della funzione [**OpenSCManager.**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)

TCP non contiene le credenziali utente specificate con un **comando net use.** Pertanto, se RPC/TCP è abilitato **esc.exe** viene usato per tentare di accedere al servizio specificato, il comando potrebbe non riuscire con accesso negato. Se si disabilita RPC/TCP sul lato client, il comando **sc.exe** usa un named pipe che contiene credenziali utente, quindi il comando avrà esito positivo. Per informazioni sulle sc.exe, vedere [Controllo di un servizio tramite SC.](controlling-a-service-using-sc.md)

> [!Note]  
> Un servizio non deve fornire credenziali esplicite a un comando **net use,** perché tali credenziali potrebbero essere inavvertitamente condivise all'esterno dei limiti del servizio. Il servizio deve invece usare la [rappresentazione client](/windows/desktop/SecAuthZ/client-impersonation) per rappresentare l'utente.

 

### <a name="rpctcp-registry-values"></a>Valori del Registro di sistema RPC/TCP

RPC/TCP è controllato dai valori del Registro di sistema **SCMApiConnectionParam,** **DisableRPCOverTCP** e **DisableRemoteScmEndpoints,** tutti nella **chiave HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control.** Tutti questi valori hanno un tipo di \_ dati REG DWORD. Le procedure seguenti illustrano come usare questi valori del Registro di sistema per controllare RPC/TCP.

La procedura seguente descrive come disabilitare RPC/TCP sul lato client.

**Per disabilitare RPC/TCP sul lato client**

1.  Combinare il **valore del Registro di sistema SCMApiConnectionParam** con il valore mask 0x80000000.
2.  Riavviare l'applicazione che chiama la [**funzione OpenSCManager.**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)

La procedura seguente descrive come disabilitare TCP sul lato server.

**Per disabilitare TCP sul lato server**

1.  Impostare il **valore del Registro di sistema DisableRPCOverTCP** su 1.
2.  Riavviare il server.

La procedura seguente descrive come disabilitare RPC/TCP e RPC/NP nel server , ad esempio per ridurre la superficie di attacco.

**Per disabilitare RPC/TCP e RPC/NP nel server**

1.  Impostare il valore del Registro di sistema **DisableRemoteScmEndpoints** su 1.
2.  Riavviare il server.

Il valore del Registro di sistema **SCMApiConnectionParam** può essere usato anche per specificare l'intervallo di timeout RPC/TCP, espresso in millisecondi. Ad esempio, il valore 30.000 specifica un intervallo di timeout di 30 secondi. Il valore predefinito è 21.000 (21 secondi).

 

 
