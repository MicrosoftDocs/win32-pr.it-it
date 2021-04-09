---
description: Il servizio eventi COM+ utilizza un oggetto classe di evento per gestire la connessione tra server di pubblicazione e Sottoscrittore.
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: Oggetto della classe di evento COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae397f647354ac24395fa073365160829a687a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966104"
---
# <a name="the-com-event-class-object"></a>Oggetto della classe di evento COM+

Il servizio eventi COM+ utilizza un *oggetto classe di evento* per gestire la connessione tra server di pubblicazione e Sottoscrittore. L'oggetto della classe di evento è un componente COM+ gestito e archiviato dal sistema di eventi COM+ e contiene le interfacce e i metodi utilizzati da un server di pubblicazione per generare eventi. Si tratta di un oggetto persistente che indica gli eventi che possono verificarsi e, facoltativamente, identifica il server di pubblicazione. È possibile specificare le interfacce e i metodi che devono essere contenuti in una classe di evento fornendo una libreria dei tipi.

Per generare un evento, il server di pubblicazione crea un'istanza dell'oggetto della classe di evento chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o il metodo **CreateObject** Microsoft Visual Basic e richiedendo che venga restituita l'interfaccia evento. L'oggetto della classe di evento di cui è stata creata un'istanza contiene l'implementazione del sistema di eventi dell'interfaccia richiesta. Un Sottoscrittore interessato deve implementare anche l'interfaccia della classe di evento per ricevere eventi da un server di pubblicazione specificato. Quando viene creata un'istanza dell'oggetto della classe di evento, il sistema di eventi lo associa ai sottoscrittori appropriati. L'elenco di sottoscrittori viene mantenuto per la durata dell'oggetto classe di evento. Un evento può essere recapitato a più Sottoscrittori in serie o in parallelo.

Quando si implementa un oggetto della classe di evento, è necessario fornire una DLL con registrazione automatica che esporti le funzioni [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) . La funzione **DllRegisterServer** registra una classe com e la funzione **DllUnregisterServer** Annulla la registrazione del componente. Gli oggetti della classe di evento vengono archiviati nel catalogo COM+ utilizzando lo strumento di amministrazione Servizi componenti o a livello di codice utilizzando i metodi delle interfacce [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) o [**ICOMAdminCatalog:: InstallMultipleEventClasses**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) . Per informazioni dettagliate sulla registrazione di oggetti della classe di evento, vedere [registrazione di una classe di evento](registering-an-event-class.md).

Poiché gli oggetti della classe di evento sono componenti configurati, è possibile configurare altri attributi, ad esempio l'accodamento, le transazioni, la sicurezza e così via, usando lo strumento di amministrazione Servizi componenti o le funzioni SDK di amministrazione COM+.

> [!Note]  
> Il servizio eventi COM+ utilizza il marshalling della libreria dei tipi. Questa operazione impone alcune restrizioni sulle interfacce della classe di evento. Ad esempio, il gestore di marshalling della libreria dei tipi non supporta [**le \_ dimensioni**](/windows/desktop/Midl/size-is) degli attributi MIDL e la [**lunghezza \_ è**](/windows/desktop/Midl/length-is).

 

Un oggetto della classe di evento dispone degli attributi di pubblicazione che determinano la modalità di pubblicazione degli eventi, nonché le proprietà seguenti:

-   **EventCLSID**. Identificatore univoco che specifica il CLSID del componente.
-   **EventClassName**. Identificatore univoco che specifica il PROGID del componente.
-   **Libreria dei tipi**. Fornisce un elenco di interfacce offerte dall'oggetto della classe di evento. Non è necessario implementare le interfacce di attivazione specificate nella libreria dei tipi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni sulla sicurezza degli eventi COM+](com--events-security-considerations.md)
</dt> <dt>

[Filtro di eventi in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Pubblicazione e distribuzione di eventi in COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Sottoscrizioni](subscriptions.md)
</dt> <dt>

[Uso di eventi COM+ con componenti in coda COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
