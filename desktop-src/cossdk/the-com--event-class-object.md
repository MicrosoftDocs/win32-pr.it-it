---
description: Il servizio Eventi COM+ usa un oggetto classe di evento per gestire la connessione tra il server di pubblicazione e il sottoscrittore.
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: Oggetto della classe di evento COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5650969895cdfa63f07e6ba77e617a962335101d4f56aeb21a5b439b27daaf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546153"
---
# <a name="the-com-event-class-object"></a>Oggetto della classe di evento COM+

Il servizio Eventi COM+ usa un oggetto *classe di evento per* gestire la connessione tra il server di pubblicazione e il sottoscrittore. L'oggetto classe di evento è un componente COM+ che viene gestito e archiviato dal sistema di eventi COM+ e contiene le interfacce e i metodi usati da un editore per la generazione di eventi. Si tratta di un oggetto persistente che indica gli eventi che possono verificarsi e, facoltativamente, identifica il server di pubblicazione. È possibile specificare le interfacce e i metodi che devono essere contenuti in una classe di evento fornendo una libreria dei tipi.

Per la generazione di un evento, l'editore crea un'istanza dell'oggetto classe di evento chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o il metodo **CreateObject** di Microsoft Visual Basic e richiedendo che l'interfaccia dell'evento sia restituita. L'oggetto classe di evento di cui è stata creata un'istanza contiene l'implementazione del sistema di eventi dell'interfaccia richiesta. Un sottoscrittore interessato deve inoltre implementare l'interfaccia della classe di evento per ricevere eventi da un determinato server di pubblicazione. Quando viene creata un'istanza dell'oggetto della classe di evento, il sistema di eventi lo associa ai sottoscrittori appropriati. L'elenco dei sottoscrittori viene mantenuto per la durata dell'oggetto della classe di evento. Un evento può essere recapitato a più sottoscrittori in serie o in parallelo.

Quando si implementa un oggetto classe di evento, è necessario fornire una DLL autoregistrazione che esporta le funzioni [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer.**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) La **funzione DllRegisterServer** registra una classe COM e la **funzione DllUnregisterServer** annulla la registrazione del componente. Gli oggetti classe di evento vengono archiviati nel catalogo COM+, usando lo strumento di amministrazione Servizi componenti o a livello di codice usando i metodi delle interfacce [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) o [**ICOMAdminCatalog::InstallMultipleEventClasses.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) Per informazioni dettagliate sulla registrazione di oggetti classe di evento, vedere [Registrazione di una classe di evento.](registering-an-event-class.md)

Poiché gli oggetti classe di evento sono componenti configurati, è possibile configurare altri attributi, ad esempio accodamento, transazioni, sicurezza e così via, usando lo strumento di amministrazione Servizi componenti o le funzioni dell'SDK amministrativo COM+.

> [!Note]  
> Il servizio Eventi COM+ usa il marshalling della libreria dei tipi. In questo modo vengono applicate alcune restrizioni alle interfacce delle classi di evento. Ad esempio, il gestore di marshalling della libreria dei tipi non supporta la dimensione degli attributi MIDL [**\_ è**](/windows/desktop/Midl/size-is) e [**la lunghezza \_ è**](/windows/desktop/Midl/length-is).

 

Un oggetto classe di evento dispone di attributi di pubblicazione che determinano la modalità di pubblicazione degli eventi, nonché delle proprietà seguenti:

-   **EventCLSID**. Identificatore univoco che specifica il CLSID del componente.
-   **EventClassName**. Identificatore univoco che specifica il PROGID del componente.
-   **TypeLibrary**. Fornisce un elenco di interfacce offerte dall'oggetto della classe di evento. Non è necessario implementare le interfacce di attivazione specificate nella libreria dei tipi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni sulla sicurezza degli eventi COM+](com--events-security-considerations.md)
</dt> <dt>

[Filtro di eventi in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Pubblicazione e recapito di eventi in COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Sottoscrizioni](subscriptions.md)
</dt> <dt>

[Uso di eventi COM+ con componenti in coda COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
