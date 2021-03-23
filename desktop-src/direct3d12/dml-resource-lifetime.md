---
title: Durata e sincronizzazione delle risorse
description: Per evitare un comportamento non definito, l'applicazione DirectML deve gestire correttamente le durate degli oggetti e la sincronizzazione tra la CPU e la GPU.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 6e8ab30c5c87c135ef3bdac0c1bc2a3d64040787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103990"
---
# <a name="resource-lifetime-and-synchronization"></a>Durata e sincronizzazione delle risorse

Analogamente a Direct3D 12, l'applicazione DirectML deve (per evitare un comportamento non definito) gestire correttamente le durate degli oggetti e la sincronizzazione tra la CPU e la GPU. DirectML segue un modello di durata delle risorse identico a quello di Direct3D 12.

- Le dipendenze di durata tra due oggetti CPU sono gestite da DirectML usando conteggi dei riferimenti sicuri. L'applicazione non deve gestire manualmente le dipendenze della durata della CPU. Ogni dispositivo figlio, ad esempio, include un riferimento sicuro al dispositivo padre.
- Le dipendenze di durata tra oggetti GPU &mdash; o dipendenze che si estendono su CPU e GPU &mdash; non vengono gestite automaticamente. È responsabilità dell'applicazione assicurarsi che le risorse GPU siano attive almeno finché tutto il lavoro che usa tale risorsa non ha completato l'esecuzione sulla GPU.

## <a name="directml-devices"></a>Dispositivi DirectML

Il dispositivo DirectML è un oggetto factory senza stato thread-safe. Ogni dispositivo figlio (vedere [**IDMLDeviceChild**](/windows/desktop/api/directml/nn-directml-idmldevicechild)) include un riferimento sicuro al dispositivo DirectML padre (vedere [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice)). Ciò significa che è sempre possibile recuperare l'interfaccia del dispositivo padre da qualsiasi interfaccia figlio del dispositivo.

Un dispositivo DirectML a sua volta include un riferimento sicuro al dispositivo Direct3D 12 usato per crearlo (vedere [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)e interfacce derivate).

Poiché il dispositivo DirectML è senza stato, è implicitamente thread-safe. È possibile chiamare i metodi sul dispositivo DirectML da più thread contemporaneamente senza la necessità di sincronizzazione esterna.

Tuttavia, a differenza del dispositivo Direct3D 12, il dispositivo DirectML non è un oggetto singleton. Si è liberi di creare tutti i dispositivi DirectML desiderati. Tuttavia, non è possibile combinare e associare gli elementi figlio del dispositivo che appartengono a dispositivi diversi. Ad esempio, [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) e [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) sono due tipi di elementi figlio (entrambe le interfacce derivano direttamente o indirettamente da **IDMLDeviceChild**). E non è possibile usare una tabella di binding (**IDMLBindingTable**) per eseguire il binding per un operatore (**IDMLCompiledOperator**) se l'operatore e la tabella di associazione appartengono a diverse istanze di dispositivo DirectML.

Poiché il dispositivo DirectML non è un singleton, la rimozione dei dispositivi viene eseguita in base ai singoli dispositivi, anziché essere un evento a livello di processo così come per un dispositivo Direct3D 12. Per altre informazioni, vedere [gestione degli errori e rimozione dei dispositivi in DirectML](dml-errors.md).

## <a name="lifetime-requirements-of-gpu-resources"></a>Requisiti di durata delle risorse GPU

Analogamente a Direct3D 12, DirectML non viene sincronizzato automaticamente tra la CPU e la GPU; né mantiene automaticamente le risorse attive mentre sono utilizzate dalla GPU. Al contrario, si tratta di responsabilità dell'applicazione.

Quando si esegue un elenco di comandi che contiene DirectML, l'applicazione deve garantire che le risorse GPU rimangano attive fino a quando tutto il lavoro che usa tali risorse non ha completato l'esecuzione sulla GPU.

Nel caso di [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) per un operatore DirectML, che include gli oggetti seguenti.

- [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) in esecuzione (o [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) , se si esegue l'inizializzazione dell'operatore).
- **IDMLCompiledOperator** che esegue il backup della tabella di associazione utilizzata per associare l'operatore.
- Gli oggetti [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) associati come input/output dell'operatore.
- Gli oggetti **ID3D12Resource** associati come risorse permanenti e temporanee, se applicabile.
- [**ID3D12CommandAllocator**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator) che esegue il backup dell'elenco dei comandi.

Non tutte le interfacce DirectML rappresentano risorse GPU. Una tabella di binding, ad esempio, *non* deve essere mantenuta attiva fino a quando tutti gli invii che lo usano non hanno completato l'esecuzione sulla GPU. Questo perché la tabella di associazione non possiede risorse GPU. Piuttosto, l'heap del descrittore. Pertanto, l' *heap del descrittore* sottostante è l'oggetto che deve essere mantenuto attivo fino al completamento dell'esecuzione e non alla tabella di associazione.

In Direct3D 12 esiste un concetto simile. Un *allocatore* di comandi deve rimanere attivo fino a quando tutte le esecuzioni che lo usano non sono state completate sulla GPU; poiché possiede la memoria GPU. Tuttavia, un *elenco* di comandi non è proprietario della memoria GPU, pertanto può essere reimpostato o rilasciato non appena è stato inviato per l'esecuzione.

In DirectML, gli operatori compilati ([**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator)) e gli inizializzatori di operatore ([**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer)) possiedono direttamente risorse GPU, pertanto devono essere mantenuti attivi fino a quando tutti gli invii che li usano non hanno completato l'esecuzione sulla GPU. Inoltre, le risorse Direct3D 12 utilizzate (allocatori di comandi, heap di descrittori, buffer come esempi) devono essere mantenute attive dall'applicazione.

Se si rilascia un oggetto in modo prematuro mentre è ancora in uso dalla GPU, il risultato è un comportamento non definito, che può causare la rimozione del dispositivo o altri errori.

## <a name="cpu-and-gpu-synchronization"></a>Sincronizzazione CPU e GPU

DirectML non invia alcun lavoro per l'esecuzione nella GPU. Al contrario, il [metodo **IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) *registra* l'invio di tale lavoro in un elenco di comandi per l'esecuzione successiva. L'applicazione deve quindi chiudere e inviare il proprio elenco di comandi per l'esecuzione chiamando [**ID3D12CommandQueue:: oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists), come con qualsiasi elenco di comandi Direct3D 12.

Poiché DirectML non invia alcun lavoro per l'esecuzione sulla GPU, non crea alcun limite, né esegue alcuna forma di sincronizzazione CPU/GPU per conto dell'utente. È responsabilità dell'applicazione usare le primitive Direct3D 12 appropriate per attendere il completamento dell'esecuzione del lavoro inviato sulla GPU, se necessario. Per altre informazioni, vedere [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) e [**ID3D12CommandQueue:: Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal).

## <a name="see-also"></a>Vedi anche

* [Esecuzione e sincronizzazione degli elenchi di comandi](/windows/desktop/direct3d12/executing-and-synchronizing-command-lists)
* [Gestione degli errori e della rimozione dei dispositivi in DirectML](dml-errors.md)