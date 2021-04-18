---
description: L'API del documento XPS implementa il modello a oggetti XPS e consente agli sviluppatori di creare un modello a oggetti XPS, modificare il contenuto del documento XPS nei programmi Windows nativi \\ \\ e salvare i dati XPS om in un file o in un flusso come documento XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Informazioni sull'API documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316428"
---
# <a name="about-xps-document-api"></a>Informazioni sull'API documento XPS

L' [API del documento XPS](documents-xps.md) implementa il modello a oggetti XPS e consente agli sviluppatori di creare un modello a oggetti XPS, modificare il contenuto del documento XPS nei programmi Windows nativi \\ \\ e salvare i dati XPS om in un file o in un flusso come documento XPS. Gli sviluppatori dei moduli della pipeline filtro XPSDrv possono inoltre utilizzare l'API documento XPS per modificare il contenuto del documento XPS in un filtro di driver della stampante XPSDrv.

## <a name="xps-document-api-overview"></a>Panoramica dell'API documento XPS

Il modello a oggetti XPS è il modello informativo di un documento XPS. Il modello informativo del documento XPS è separato dal modello di markup utilizzato nelle parti del documento. Nel modello a oggetti XPS viene descritta l'organizzazione dei componenti interni che costituiscono un documento XPS e nel modello di markup viene descritto il contenuto di tali componenti.

In un programma, viene creata un'istanza del modello a oggetti XPS come OM XPS. XPS OM è essenzialmente una versione in memoria del contenuto di un documento XPS. Analogamente, in un'organizzazione logica a un documento XPS, un OM XPS non viene considerato un documento XPS fino a quando non viene serializzato in un file o in un flusso.

La struttura esatta del markup non è disponibile per XPS OM quando un documento XPS viene deserializzato dal markup a un OM XPS. Ad esempio, se la proprietà è stata rappresentata come elemento o attributo nel markup, il valore della proprietà di un oggetto documento viene presentato da XPS OM esattamente allo stesso modo.

L' [API documento XPS](documents-xps.md) può essere divisa nelle categorie seguenti:

-   [Interfacce trunk XPS OM](xps-om-trunk-interfaces.md)

    Le interfacce trunk consentono di accedere ai componenti di primo livello della struttura del documento XPS. Queste interfacce forniscono inoltre i mezzi per serializzare un oggetto XPS OM e deserializzare un documento XPS.

-   [Interfacce di pagine XPS OM](xps-object-model-page-interfaces.md)

    Le interfacce di pagina consentono di accedere al contenuto di una pagina in un documento XPS. Le interfacce che descrivono il contenuto della pagina sono incluse anche con le interfacce di pagina.

-   [Firme digitali XPS OM](using-the-xps-digital-signatures.md)

    XPS OM supporta le firme digitali. Tuttavia, è possibile accedere direttamente alle firme digitali in un documento XPS senza creare un OM XPS. Per ulteriori informazioni su come accedere alle firme digitali XPS senza XPS OM, vedere [XPS Digital Signature API](xps-digital-signatures.md).

-   [Interfacce del ticket di stampa XPS OM](xps-object-model-print-ticket-interfaces.md)

    I documenti XPS supportano i ticket di stampa a livello di pacchetto (processo), documento e pagina. I ticket di stampa contengono informazioni su come formattare il contenuto del documento per la stampa o la visualizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Argomenti della sezione**
</dt> <dt>

[Interfacce trunk XPS OM](xps-om-trunk-interfaces.md)
</dt> <dt>

[Interfacce di pagine XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[Firme digitali XPS OM](using-the-xps-digital-signatures.md)
</dt> <dt>

[Interfacce del ticket di stampa XPS OM](xps-object-model-print-ticket-interfaces.md)
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

 

 



