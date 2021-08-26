---
title: Configurazione dei computer per RPC su HTTP
description: Per utilizzare HTTP come protocollo di trasporto per RPC, il proxy RPC in esecuzione in Internet Information Server (IIS) deve essere configurato nella rete del programma server.
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4628339afe09e2b6e9a6f216504f411550d37b7a285614e507c89a4a8052c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022471"
---
# <a name="configuring-computers-for-rpc-over-http"></a>Configurazione dei computer per RPC su HTTP

Per utilizzare HTTP come protocollo di trasporto per RPC, il proxy RPC in esecuzione in Internet Information Server (IIS) deve essere configurato nella rete del programma server. In questa sezione vengono descritte le opzioni di configurazione. Per consigli sulle procedure consigliate per la programmazione e la configurazione quando si usa RPC su HTTP, vedere [Rpc over HTTP Deployment Consigli](rpc-over-http-deployment-recommendations.md). L'attività principale è la configurazione del proxy RPC per accettare e inoltrare RPC su connessioni HTTP a un programma server RPC su HTTP.

IIS deve prima essere installato nel computer che esegue il proxy RPC. Dopo l'installazione di IIS, viene installato il proxy RPC. Sia IIS che il proxy RPC possono essere installati contemporaneamente da **Aggiungi/Rimuovi** componenti Windows nel Pannello di controllo. Il proxy RPC viene installato **da Servizi di** rete e viene chiamato proxy RPC su **HTTP** Windows configurazione. Se IIS e il proxy RPC sono installati contemporaneamente, Windows verifica che siano installati nell'ordine corretto.

> [!Note]  
> Al termine dell'installazione, è necessario riavviare IIS se era in esecuzione durante il processo di installazione.

 

Dopo l'installazione del proxy RPC, è necessario eseguire alcune attività di configurazione aggiuntive:

1.  Aprire lo snap-in MMC IIS e configurare la directory virtuale proxy RPC per richiedere la sicurezza, come illustrato in [Rpc over HTTP Security](rpc-over-http-security.md). Questo passaggio è obbligatorio solo se si prevede di usare RPC su HTTP v2.
2.  Se IIS non dispone di un certificato installato, è necessario ottenere e installare un certificato valido per tale computer per utilizzare SSL durante la comunicazione con il proxy RPC. Questo passaggio è rilevante solo per RPC su HTTP v2. Poiché RPC su HTTP v1 non supporta SSL, questo passaggio può essere omesso per RPC su HTTP v1.
3.  Impostare la **chiave ValidPorts** come descritto in Rpc over HTTP Security ( [Sicurezza RPC su HTTP).](rpc-over-http-security.md)

Al termine di queste attività di configurazione, il proxy RPC su HTTP è pronto per inoltrare le richieste dal client RPC su HTTP al server RPC su HTTP.

## <a name="rpc-over-http-registry-keys"></a>Chiavi del Registro di sistema RPC su HTTP

In questa sezione vengono illustrate le chiavi del Registro di sistema aggiuntive usate per configurare il client, il server o il proxy RPC in una connessione RPC su HTTP. Queste chiavi in genere non sono necessarie. vengono forniti qui per completezza.

**HKLM \\ Software \\ Microsoft \\ Rpc \\ DefaultChannelLifetime**

DWORD. Esegue l'override della durata del canale predefinita. Utilizzato nel client e nel proxy RPC. La durata del canale è espressa in byte. Se non specificato, viene usato 1 GB. Usato solo in RPC su HTTP v2. Quando viene modificato nel proxy RPC, è necessario riavviare IIS per l'applicazione della modifica.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ ClientReceiveWindow**

DWORD. Se presente, specifica la finestra di ricezione utilizzata dal client per i dati ricevuti dal proxy RPC. Il valore minimo valido è 8K. Il valore massimo è 1 GB. Se il valore non è presente, viene usato 64K. Usato solo in RPC su HTTP v2.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ InProxyReceiveWindow**

DWORD. Se presente, specifica la finestra di ricezione utilizzata dal proxy RPC per i dati ricevuti dal client. Il valore minimo valido è 8K. Il valore massimo è 1 GB. Se il valore non è presente, viene usato 64K. Usato solo in RPC su HTTP v2. Quando vengono apportate modifiche a questo valore, è necessario riavviare IIS per avere effetto.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ OutProxyReceiveWindow**

DWORD. Se presente, specifica la finestra di ricezione utilizzata dal proxy RPC per i dati ricevuti dal server. Il valore minimo valido è 8K. Il valore massimo è 1 GB. Se il valore non è presente, viene usato 64K. Usato solo in RPC su HTTP v2. Quando vengono apportate modifiche a questo valore, è necessario riavviare IIS per avere effetto.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ ServerReceiveWindow**

DWORD. Se presente, specifica la finestra di ricezione utilizzata dal server per i dati ricevuti dal proxy RPC. Il valore minimo valido è 8K. Il valore massimo è 1 GB. Se il valore non è presente, viene usato 64K. Usato solo in RPC su HTTP v2. Quando vengono apportate modifiche a questo valore, è necessario riavviare IIS per avere effetto.

\-

**Criteri software HKLM \\ \\ Microsoft Windows NT Rpc \\ \\ \\ \\ MinimumConnectionTimeout**

DWORD. Se presente, specifica il timeout di connessione minimo utilizzato dal client e dal proxy RPC, in secondi. Il timeout effettivo usato è il valore inferiore di questo valore e il timeout della connessione inattiva di IIS. Se zero o la chiave non è presente, viene utilizzato il timeout di connessione inattiva di IIS. Usato solo in RPC su HTTP v2. Quando vengono apportate modifiche a questo valore nel proxy RPC, è necessario riavviare IIS per l'applicazione della modifica.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ UseProxyForIPAddrIfRDNSFails**

Se presente e impostato su un valore diverso da zero e viene fornito un indirizzo IP numerico come indirizzo proxy RPC, un client RPC su HTTP tenterà la risoluzione dei nomi inversa e, in caso di errore, tenterà la connessione al proxy RPC tramite un proxy HTTP. Può essere usato per emulare Windows NT comportamento nelle installazioni che richiedono tale comportamento. Ignorato per RPC su HTTP v2. Utilizzato solo quando si usa RPC su HTTP v1. Supportato solo in Windows 2000 con Service Pack 3 (SP3) e versioni successive.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RpcProxy \\ AllowAnonymous**

DWORD. Se non è presente o è impostato su zero, il proxy RPC controlla se la connessione è autenticata e se è protetta (viene usato SSL o un'altra forma di crittografia). Se uno dei due è false, la connessione viene rifiutata. Se questo valore contiene un valore diverso da zero, sono consentite connessioni anonime e non crittografate. Questa impostazione è un'aggiunta alle impostazioni della directory virtuale. Ad esempio, se l'accesso anonimo è disabilitato a livello di directory virtuale, ma **AllowAnonymous** è diverso da zero, l'accesso anonimo verrà comunque bloccato a livello di IIS. Usato nel proxy RPC solo in RPC su HTTP v2. Quando vengono apportate modifiche a questo valore nel proxy RPC, è necessario riavviare IIS per l'applicazione della modifica.

> [!WARNING]
> Microsoft sconsiglia vivamente di impostare il **valore AllowAnonymous** nei sistemi di produzione per considerazioni sulla sicurezza. L'unico motivo per cui questa chiave deve essere impostata è per il test su reti chiuse senza accesso esterno. Qualsiasi sistema connesso a Internet e che esegue il proxy RPC con la chiave **AllowAnonymous** impostata su un valore diverso da zero può essere vulnerabile agli attacchi.

 

 

 




