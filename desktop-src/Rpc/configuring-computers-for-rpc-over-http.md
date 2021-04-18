---
title: Configurazione dei computer per RPC su HTTP
description: Per utilizzare HTTP come protocollo di trasporto per RPC, il proxy RPC in esecuzione in Internet Information Server (IIS) deve essere configurato nella rete del programma server.
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d1b39276633f3b827f778deef77edd5630c599
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298435"
---
# <a name="configuring-computers-for-rpc-over-http"></a>Configurazione dei computer per RPC su HTTP

Per utilizzare HTTP come protocollo di trasporto per RPC, il proxy RPC in esecuzione in Internet Information Server (IIS) deve essere configurato nella rete del programma server. In questa sezione vengono descritte le opzioni di configurazione. Per consigli sulla programmazione e sulle procedure di configurazione migliori quando si utilizza RPC su HTTP, vedere [indicazioni sulla distribuzione di RPC su http](rpc-over-http-deployment-recommendations.md). L'attività principale consiste nel configurare il proxy RPC per l'accettazione e l'inoltro delle connessioni RPC su HTTP a un programma server RPC su HTTP.

IIS deve prima essere installato nel computer in cui è in esecuzione il proxy RPC. Una volta installato IIS, viene installato il proxy RPC. Sia IIS che il proxy RPC possono essere installati contemporaneamente da **Installazione componenti di Windows** nel pannello di controllo. Il proxy RPC viene installato da **servizi di rete** ed è chiamato **RPC su proxy http** nell'installazione di Windows. Se sia IIS che proxy RPC vengono installati contemporaneamente, Windows garantisce che siano installati nell'ordine corretto.

> [!Note]  
> Al termine dell'installazione, è necessario riavviare IIS se era in esecuzione durante il processo di installazione.

 

Dopo l'installazione del proxy RPC, è necessario eseguire alcune attività di configurazione aggiuntive:

1.  Aprire lo snap-in MMC IIS e configurare la directory virtuale del proxy RPC in modo da richiedere la sicurezza, come descritto in [RPC su http Security](rpc-over-http-security.md). Questo passaggio è necessario solo se si prevede di usare RPC su HTTP V2.
2.  Se in IIS non è installato un certificato, è necessario ottenere e installare un certificato valido per tale computer per utilizzare SSL durante la comunicazione con il proxy RPC. Questo passaggio è pertinente solo per RPC su HTTP V2. Poiché RPC su HTTP V1 non supporta SSL, questo passaggio può essere omesso per RPC su HTTP V1.
3.  Impostare la chiave **ValidPorts** come descritto in [RPC su http Security](rpc-over-http-security.md).

Al termine di queste attività di configurazione, il proxy RPC su HTTP è pronto per l'inoltro delle richieste dal client RPC su http al server RPC su HTTP.

## <a name="rpc-over-http-registry-keys"></a>Chiavi del registro di sistema RPC su HTTP

In questa sezione vengono illustrate le chiavi aggiuntive del registro di sistema utilizzate per configurare il client, il server o il proxy RPC in una connessione RPC su HTTP. Queste chiavi non sono in genere necessarie; sono disponibili qui per completezza.

**HKLM \\ software \\ Microsoft \\ RPC \\ DefaultChannelLifetime**

DWORD. Esegue l'override della durata predefinita del canale. Utilizzato nel client e nel proxy RPC. La durata del canale è espressa in byte. Se non è specificato, viene usato 1 GB. Utilizzato solo in RPC su HTTP V2. Se il proxy RPC è stato modificato, è necessario riavviare IIS per rendere effettive le modifiche.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ ClientReceiveWindow**

DWORD. Quando è presente, specifica la finestra di ricezione utilizzata dal client per i dati ricevuti dal proxy RPC. Il valore minimo valido è 8 KB. Il valore massimo è 1 GB. Se il valore non è presente, viene usato 64K. Utilizzato solo in RPC su HTTP V2.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ InProxyReceiveWindow**

DWORD. Quando è presente, specifica la finestra di ricezione utilizzata dal proxy RPC per i dati ricevuti dal client. Il valore minimo valido è 8 KB. Il valore massimo è 1 GB. Se il valore non è presente, viene usato 64K. Utilizzato solo in RPC su HTTP V2. Quando vengono apportate modifiche a questo valore, è necessario riavviare IIS per rendere effettive le modifiche.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ OutProxyReceiveWindow**

DWORD. Quando è presente, specifica la finestra di ricezione utilizzata dal proxy RPC per i dati ricevuti dal server. Il valore minimo valido è 8 KB. Il valore massimo è 1 GB. Se il valore non è presente, viene usato 64K. Utilizzato solo in RPC su HTTP V2. Quando vengono apportate modifiche a questo valore, è necessario riavviare IIS per rendere effettive le modifiche.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ ServerReceiveWindow**

DWORD. Quando è presente, specifica la finestra di ricezione utilizzata dal server per i dati ricevuti dal proxy RPC. Il valore minimo valido è 8 KB. Il valore massimo è 1 GB. Se il valore non è presente, viene usato 64K. Utilizzato solo in RPC su HTTP V2. Quando vengono apportate modifiche a questo valore, è necessario riavviare IIS per rendere effettive le modifiche.

\-

**\\Criteri software \\ HKLM \\ Microsoft \\ Windows NT \\ RPC \\ MinimumConnectionTimeout**

DWORD. Quando è presente, specifica il timeout di connessione minimo utilizzato dal client e dal proxy RPC, in secondi. Il timeout effettivo utilizzato è minore di questo valore e il timeout della connessione inattiva di IIS. Se il valore è zero o la chiave non è presente, viene utilizzato il timeout della connessione inattiva IIS. Utilizzato solo in RPC su HTTP V2. Quando vengono apportate modifiche a questo valore sul proxy RPC, è necessario riavviare IIS per rendere effettive le modifiche.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ UseProxyForIPAddrIfRDNSFails**

Quando è presente e impostato su un valore diverso da zero e viene fornito un indirizzo IP numerico come indirizzo proxy RPC, un client RPC su HTTP tenterà la risoluzione dei nomi inverso e, in caso di errore, tenterà di connettersi al proxy RPC tramite un proxy HTTP. Può essere usato per emulare il comportamento di Windows NT nelle installazioni che richiedono un comportamento di questo tipo. Ignorato per RPC su HTTP V2. Usato solo quando viene usato RPC su HTTP V1. Supportato solo in Windows 2000 con Service Pack 3 (SP3) e versioni successive.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ Rpcproxy \\ AllowAnonymous**

DWORD. Se non è presente o è impostato su zero, il proxy RPC controlla se la connessione viene autenticata e se è protetta (SSL o un'altra forma di crittografia utilizzata). Se uno dei due è false, la connessione viene rifiutata. Se questo valore contiene un valore diverso da zero, sono consentite connessioni anonime e non crittografate. Questa impostazione è un'aggiunta alle impostazioni della directory virtuale. Ad esempio, se l'accesso anonimo è disabilitato a livello di directory virtuale, ma **AllowAnonymous** è diverso da zero, l'accesso anonimo verrà comunque bloccato a livello di IIS. Utilizzato sul proxy RPC solo in RPC su HTTP V2. Quando vengono apportate modifiche a questo valore sul proxy RPC, è necessario riavviare IIS per rendere effettive le modifiche.

> [!WARNING]
> Microsoft consiglia vivamente di non impostare il valore **AllowAnonymous** nei sistemi di produzione per considerazioni sulla sicurezza. L'unico motivo per cui questa chiave deve essere impostata è per il test su reti chiuse senza accesso esterno. Qualsiasi sistema connesso a Internet e che esegue il proxy RPC con la chiave **AllowAnonymous** impostata su un valore diverso da zero può essere vulnerabile agli attacchi.

 

 

 




