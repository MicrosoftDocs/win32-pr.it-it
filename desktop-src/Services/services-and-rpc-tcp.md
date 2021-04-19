---
description: A partire da Windows Vista, gestione controllo servizi (SCM) supporta le chiamate di procedure remote su entrambe le Transmission Control Protocol (RPC/TCP) e le named pipe (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Servizi e RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fdb2ef3b21f280ba4e5078d302813de41a5a43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317672"
---
# <a name="services-and-rpctcp"></a>Servizi e RPC/TCP

A partire da Windows Vista, gestione controllo servizi (SCM) supporta le chiamate di procedure remote su entrambe le Transmission Control Protocol (RPC/TCP) e le named pipe (RPC/NP). Per impostazione predefinita, le funzioni SCM sul lato client utilizzano RPC/TCP.

RPC/TCP è adatto per la maggior parte delle applicazioni che utilizzano le funzioni SCM in modalità remota, ad esempio strumenti di amministrazione remota o di monitoraggio. Tuttavia, per compatibilità e prestazioni, è possibile che alcune applicazioni debbano disabilitare RPC/TCP impostando i valori del registro di sistema descritti in questo argomento.

Quando un servizio chiama una funzione SCM remota, il controllo SCM sul lato client tenta prima di tutto di usare RPC/TCP per comunicare con SCM sul lato server. Se nel server è in esecuzione una versione di Windows che supporta RPC/TCP e consente il traffico RPC/TCP, la connessione RPC/TCPP avrà esito positivo. Se nel server è in esecuzione una versione di Windows che non supporta RPC/TCP oppure supporta RPC/TCP ma opera dietro un firewall che consente solo il traffico di named pipe, la connessione RPC/TCP scade e il controllo SCM ritenta la connessione con RPC/NP. Questa operazione avrà esito positivo, ma potrebbe richiedere del tempo (in genere più di 20 secondi), causando la visualizzazione del blocco della funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) .

Il protocollo TCP non porta le credenziali utente specificate con un comando **net use** . Di conseguenza, se RPC/TCP è abilitato e **sc.exe** viene usato per tentare di accedere al servizio specificato, il comando potrebbe non riuscire con accesso negato. La disabilitazione di RPC/TCP sul lato client fa in modo che il **sc.exe** comando usi una named pipe che contenga le credenziali utente, quindi il comando avrà esito positivo. Per informazioni su sc.exe, vedere [controllo di un servizio con SC](controlling-a-service-using-sc.md).

> [!Note]  
> Un servizio non deve fornire credenziali esplicite a un comando **net use** , perché tali credenziali potrebbero essere condivise inavvertitamente all'esterno dei limiti del servizio. Il servizio deve invece usare la [rappresentazione client](/windows/desktop/SecAuthZ/client-impersonation) per rappresentare l'utente.

 

### <a name="rpctcp-registry-values"></a>Valori del registro di sistema RPC/TCP

RPC/TCP è controllato dai valori del registro di sistema **SCMApiConnectionParam**, **DisableRPCOverTCP** e **DisableRemoteScmEndpoints** , che si trovano tutti sotto la chiave di controllo CurrentControlSet **\_ locale del \_ computer HKEY** \\  \\  \\  . Tutti questi valori hanno un tipo di \_ dati reg DWORD. Nelle procedure riportate di seguito viene illustrato come utilizzare questi valori del registro di sistema per controllare RPC/TCP.

Nella procedura riportata di seguito viene descritto come disabilitare RPC/TCP sul lato client.

**Per disabilitare RPC/TCP sul lato client**

1.  Combinare il valore del registro di sistema **SCMApiConnectionParam** con il valore mask 0x80000000.
2.  Riavviare l'applicazione che chiama la funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) .

Nella procedura riportata di seguito viene descritto come disabilitare TCP sul lato server.

**Per disabilitare TCP sul lato server**

1.  Impostare il valore del registro di sistema **DisableRPCOverTCP** su 1.
2.  Riavviare il server.

Nella procedura riportata di seguito viene descritto come disabilitare RPC/TCP e RPC/NP sul server, ad esempio per ridurre la superficie di attacco.

**Per disabilitare RPC/TCP e RPC/NP sul server**

1.  Impostare il valore del registro di sistema **DisableRemoteScmEndpoints** su 1.
2.  Riavviare il server.

Il valore del registro di sistema **SCMApiConnectionParam** può essere utilizzato anche per specificare l'intervallo di timeout RPC/TCP, in millisecondi. Ad esempio, un valore di 30.000 specifica un intervallo di timeout di 30 secondi. Il valore predefinito è 21.000 (21 secondi).

 

 
