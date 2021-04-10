---
description: Linee guida di base per la progettazione di applicazioni COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Linee guida di base per la progettazione di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127162"
---
# <a name="basic-guidelines-for-designing-com-applications"></a>Linee guida di base per la progettazione di applicazioni COM+

Per sfruttare tutti i vantaggi di COM+, è possibile utilizzare alcune linee guida di base per la creazione di un'applicazione:

-   **Modellare lo stato durevole come schema di database, utilizzando lo strumento di database preferito.** Quasi tutte le applicazioni devono mantenere lo stato durevole. I database forniscono i servizi necessari per creare un archivio durevole e scalabile dello stato. Pertanto, il primo passaggio nella creazione di un'applicazione COM+ consiste nel modellare lo stato durevole dell'applicazione come una sorta di schema di database. Il database utilizzato non è rilevante. la maggior parte dei database commerciali è compatibile con COM+. Microsoft SQL Server è un valido esempio di una soluzione che è possibile usare.

-   **Modellare la logica dell'applicazione COM+ come un set di interfacce COM.** Quando si dispone di uno schema che rappresenta le informazioni sullo stato dell'applicazione, modellare gli interscambi che si verificano nell'applicazione come interfacce COM. Queste interfacce modellano il comportamento dell'applicazione. Si tratta anche della fase di sviluppo in cui è necessario determinare quali servizi COM+ funzionano meglio per l'applicazione.

-   **Compilare DLL del componente contenenti componenti che utilizzano lo schema di dati fisico ed esporre una visualizzazione logica dei dati ad altri componenti (il primo elemento dell'elenco), nonché i componenti implementati in termini di modello di dati logico (il secondo elemento in questo elenco).** Una volta che si dispone della struttura della logica e delle informazioni sullo stato, è possibile iniziare a scrivere il codice ed è ora possibile scrivere componenti COM basati su DLL che implementano le interfacce in termini di schema definito. I componenti fungono semplicemente da manipolatori per lavorare con le informazioni del database e le DLL dei componenti consentono di compilare un'applicazione COM+ che funziona e che viene ridimensionata correttamente.

-   **Distribuire i componenti nell'ambiente COM+ utilizzando i servizi COM+ selezionati.** Dopo aver compilato l'applicazione, è possibile distribuire l'applicazione in un cluster di rete o di server. È ora possibile prendere decisioni in base alle risorse disponibili ed è possibile personalizzare ogni componente per ottenere le prestazioni massime.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presupposti e principi di progettazione COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Progettazione dell'applicazione COM+ tramite UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Suggerimenti di progettazione generali per l'utilizzo di COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Ottimizzazione delle interazioni con il livello di logica di business COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Altri strumenti Microsoft per la creazione di applicazioni distribuite](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



