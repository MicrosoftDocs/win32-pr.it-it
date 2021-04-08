---
title: Gestore di Client-Side Lightweight
description: I gestori lato client leggeri consentono di creare gestori lato client generali di qualsiasi dimensione, per facilitare l'esecuzione di qualsiasi tipo di attività standard.
ms.assetid: b712237c-55d7-4f52-9cf6-19c6e5fb3182
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e8df5be24e8773a660a4d0208b27a2f585e32
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730538"
---
# <a name="the-lightweight-client-side-handler"></a>Gestore di Client-Side Lightweight

I gestori lato client leggeri consentono di creare gestori lato client generali di qualsiasi dimensione, per facilitare l'esecuzione di qualsiasi tipo di attività standard. Poiché i gestori sono utilizzabili da più di un client. Si differenziano dai gestori OLE in quanto non possono essere creati prima che il server venga avviato e la loro durata è legata a quella di gestione proxy, impedendo un possibile race condition in cui il gestore potrebbe altrimenti essere rilasciato prematuramente.

Gestione proxy è l'oggetto creato dal sistema che implementa l'interfaccia [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) . Se si usa il marshalling standard, il sistema lo crea automaticamente quando si chiama [**CoGetStandardMarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (o [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)per la creazione di un gestore di marshalling aggregato per i gestori Lightweight) e implementa anche le interfacce [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) sull'oggetto. Sul lato server è presente un oggetto di sistema corrispondente che implementa anche **IMarshal**. Questi oggetti gestiscono il marshalling per l'utente in modo trasparente.

Esistono due tipi generali di questi gestori che è possibile implementare:

-   Gestore che esegue un servizio che non richiede dati aggiuntivi dal server
-   Gestore che utilizza dati aggiuntivi dal server

Di seguito sono riportati alcuni potenziali usi dei dati aggiuntivi nel flusso fornito dal server:

-   Dati statici dal server. Indipendentemente dall'interfaccia particolare sottoposta a marshalling, il server scrive gli stessi dati nel flusso.
-   Dati per interfaccia dal server. A seconda di quale interfaccia particolare viene sottoposta a marshalling, il server può scrivere dati diversi nel flusso.
-   Helper per interfaccia. Componenti COM per interfaccia aggregati nel gestore client e delega al proxy standard. Per migliorare le prestazioni di rete, ad esempio, un componente COM per [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) può eseguire la memorizzazione nella cache lato client dei dati, il read-ahead, il write-behind, il blocco di operazioni e così via.
-   Versione di rete di un'interfaccia. La versione di rete dell'interfaccia è diversa dall'interfaccia esposta dal codice dell'applicazione client e server. È possibile, ad esempio, che le interfacce esposte dal multiplex IA e IB si trovino sulla stessa interfaccia di rete INetAB, il modo in cui il gestore del server di incorporamento. Ad esempio, è possibile convertire un'interfaccia di trasferimento dati in un'interfaccia di rete che utilizza pipe per un efficace trasferimento dei dati.

I client legacy potrebbero non essere in grado di eseguire l'unmarshalling di interfacce con gestori personalizzati, per due motivi: prima potrebbero non comprendere il CLSID utilizzato nel pacchetto con marshalling personalizzato quando il gestore del server viene aggregato e l'oggetto richiede un gestore. In secondo luogo, il codice del gestore potrebbe non essere eseguito anche sul lato client se è necessaria una nuova funzionalità di COM per creare il gestore di marshalling standard aggregato ed eseguire chiamate [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) remote.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestore OLE](the-ole-handler.md)
</dt> </dl>

 

 