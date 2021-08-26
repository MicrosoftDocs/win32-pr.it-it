---
description: L'API documento XPS implementa il modello a oggetti XPS e consente agli sviluppatori di creare un OM XPS, modificare il contenuto dei documenti XPS in programmi Windows nativi e salvare l'OM XPS in un file o flusso come documento \\ \\ XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Informazioni sull'API documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b2363bba55fed184b1cf80bfc81fac9474444f77c9b867b461940e6b72d8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950911"
---
# <a name="about-xps-document-api"></a>Informazioni sull'API documento XPS

L'API documento [XPS](documents-xps.md) implementa il modello a oggetti XPS e consente agli sviluppatori di creare un OM XPS, modificare il contenuto dei documenti XPS in programmi Windows nativi e salvare l'OM XPS in un file o flusso come documento \\ \\ XPS. Gli sviluppatori di moduli della pipeline di filtro XPSDrv possono anche usare l'API documento XPS per modificare il contenuto dei documenti XPS in un filtro del driver della stampante XPSDrv.

## <a name="xps-document-api-overview"></a>Panoramica dell'API documento XPS

Il modello a oggetti XPS è il modello di informazioni di un documento XPS. Il modello di informazioni del documento XPS è separato dal modello di markup utilizzato all'interno delle parti del documento. Il modello a oggetti XPS descrive l'organizzazione dei componenti interni che costituiscono un documento XPS e il modello di markup descrive il contenuto di tali componenti.

In un programma viene creata un'istanza del modello a oggetti XPS come OM XPS. XpS OM è essenzialmente una versione in memoria del contenuto di un documento XPS. Sebbene sia simile nell'organizzazione logica a un documento XPS, un OM XPS non viene considerato un documento XPS fino a quando non viene serializzato in un file o in un flusso.

La struttura esatta del markup non è disponibile per XPS OM quando un documento XPS viene deserializzato dal markup a un OM XPS. Ad esempio, se la proprietà è stata rappresentata come elemento o attributo nel markup, il valore della proprietà di un oggetto documento viene presentato dall'OM XPS esattamente nello stesso modo.

[L'API documento XPS](documents-xps.md) può essere suddivisa nelle categorie seguenti:

-   [Interfacce trunk XPS OM](xps-om-trunk-interfaces.md)

    Le interfacce trunk forniscono l'accesso ai componenti di primo livello della struttura del documento XPS. Queste interfacce forniscono anche i mezzi per serializzare un OM XPS e deserializzare un documento XPS.

-   [Interfacce di pagina OM XPS](xps-object-model-page-interfaces.md)

    Le interfacce di pagina consentono di accedere al contenuto di una pagina in un documento XPS. Le interfacce che descrivono il contenuto della pagina sono incluse anche nelle interfacce di pagina.

-   [Firme digitali XPS OM](using-the-xps-digital-signatures.md)

    XPS OM supporta le firme digitali. Tuttavia, è possibile accedere direttamente alle firme digitali in un documento XPS senza creare un OM XPS. Per altre informazioni su come accedere alle firme digitali XPS senza un OM XPS, vedere [XPS Digital Signature API](xps-digital-signatures.md).

-   [Interfacce print ticket XPS OM](xps-object-model-print-ticket-interfaces.md)

    I documenti XPS supportano print ticket a livello di pacchetto (processo), documento e pagina. I ticket di stampa contengono informazioni su come formattare il contenuto del documento per la stampa o la visualizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Argomenti della sezione**
</dt> <dt>

[Interfacce trunk XPS OM](xps-om-trunk-interfaces.md)
</dt> <dt>

[Interfacce di pagina OM XPS](xps-object-model-page-interfaces.md)
</dt> <dt>

[Firme digitali XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Interfacce print ticket XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

**Altri argomenti correlati**
</dt> <dt>

[Inizializzare un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Firme digitali XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



