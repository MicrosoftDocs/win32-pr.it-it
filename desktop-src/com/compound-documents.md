---
title: Documenti composti
description: I documenti composti OLE consentono agli utenti di lavorare all'interno di una singola applicazione di modificare i dati scritti in vari formati e derivati da più origini.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118558"
---
# <a name="compound-documents"></a>Documenti composti

I documenti composti OLE consentono agli utenti di lavorare all'interno di una singola applicazione di modificare i dati scritti in vari formati e derivati da più origini. Ad esempio, un utente può inserire in un documento di elaborazione di Word un grafo creato in una seconda applicazione e un oggetto audio creato in una terza applicazione. Se si attiva il grafo, la seconda applicazione caricherà la propria interfaccia utente o almeno quella parte contenente gli strumenti necessari per modificare l'oggetto. L'attivazione dell'oggetto audio comporta la riproduzione della terza applicazione. In entrambi i casi, un utente è in grado di modificare i dati da origini esterne dall'interno del contesto di un singolo documento.

La tecnologia per documenti compositi OLE si basa su una base composta da COM, archiviazione strutturata e trasferimento dati uniforme. Come riepilogato di seguito, ognuna di queste tecnologie di base svolge un ruolo fondamentale nei documenti compositi OLE:

<dl> <dt>

<span id="COM"></span><span id="com"></span>COM
</dt> <dd>

Un oggetto documento composto è essenzialmente un oggetto COM che può essere incorporato o collegato a un documento esistente. Come oggetto COM, un oggetto documento composto espone l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , tramite la quale i client possono ottenere i puntatori alle altre interfacce, inclusi diversi, ad esempio [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)e [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), che forniscono funzionalità speciali univoche per gli oggetti documento composti.

</dd> <dt>

<span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Archiviazione strutturata
</dt> <dd>

Un oggetto documento composto deve implementare [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) o, facoltativamente, le interfacce [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) per gestire la propria archiviazione. Un contenitore utilizzato per creare documenti composti deve fornire l'interfaccia [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , tramite la quale gli oggetti archiviano e recuperano i dati. I contenitori forniscono quasi sempre istanze di **IStorage** ottenute dall'implementazione dei file composti di OLE. I contenitori devono usare anche le interfacce **IPersistStorage** e/o **IPersistStream** di un oggetto.

</dd> <dt>

<span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer
</dt> <dd>

Le applicazioni che supportano i documenti composti devono implementare [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) perché gli oggetti incorporati e gli oggetti collegati iniziano come dati trasferiti con formati degli Appunti OLE speciali, anziché con formati degli Appunti standard di Microsoft Windows. In altre parole, la formattazione dei dati come oggetto incorporato o collegato è semplicemente un'altra opzione fornita dal modello di trasferimento dei dati uniforme di OLE.

</dd> </dl>

La tecnologia dei documenti compositi di OLE offre agli sviluppatori e agli utenti del software lo stesso vantaggio. Anziché essere obbligati a stipare ogni funzionalità concepibile in un'unica applicazione, gli sviluppatori di software sono ora gratuiti, se desiderano, per sviluppare applicazioni più piccole e più mirate che si basano su altre applicazioni per fornire funzionalità aggiuntive. Nei casi in cui uno sviluppatore di software decide di fornire un'applicazione con funzionalità oltre alle funzionalità di base, lo sviluppatore può implementare questi servizi aggiuntivi come DLL separate, che vengono caricati in memoria solo quando sono necessari i relativi servizi. Gli utenti traggono vantaggio da software più piccolo, più veloce e più idoneo che possono combinare in base alle esigenze, manipolando tutti i componenti necessari da un singolo documento master.

Per altre informazioni, vedere i seguenti argomenti:

-   [Contenitori e server](containers-and-servers.md)
-   [Collegamento e incorporamento](linking-and-embedding.md)
-   [Gestori di oggetti](object-handlers.md)
-   [Server in-process](in-process-servers.md)
-   [Oggetti collegati e moniker](linked-objects-and-monikers.md)
-   [Notifications](notifications.md)
-   [Interfacce di documenti composti](compound-document-interfaces.md)
-   [Stati degli oggetti](object-states.md)
-   [Implementazione di In-Place attivazione](implementing-in-place-activation.md)
-   [Creazione di oggetti collegati e incorporati da dati esistenti](creating-linked-and-embedded-objects-from-existing-data.md)
-   [Visualizza Caching](view-caching.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dati](data-transfer.md)
</dt> <dt>

[Archiviazione strutturata](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 