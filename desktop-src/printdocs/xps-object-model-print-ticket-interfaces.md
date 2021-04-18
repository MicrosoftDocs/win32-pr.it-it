---
description: Questa interfaccia IXpsOMPrintTicketResource dell'API documento XPS consente di accedere a un ticket di stampa esistente e di creare un Print Ticket in un OM XPS.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: Interfacce del ticket di stampa XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646089455e7106b1be3716c0ccf0774be361f130
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321059"
---
# <a name="xps-om-print-ticket-interfaces"></a>Interfacce del ticket di stampa XPS OM

Questa interfaccia [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) dell'API documento XPS consente di accedere a un ticket di stampa esistente e di creare un Print Ticket in un OM XPS.

## <a name="print-ticket-resources"></a>Risorse di Print Ticket

L'interfaccia [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) consente a un programma di leggere il contenuto di un ticket di stampa esistente chiamando il metodo **GetPrintTicketResource** di un'interfaccia che supporta un ticket di stampa. È possibile aggiungere nuove risorse di Print Ticket a una parte del documento chiamando **SetPrintTicketResource**.

Sono disponibili tre livelli di ticket di stampa, che specificano l'ambito del ticket di stampa. I livelli del ticket di stampa sono: il livello del processo (o del pacchetto), il livello del documento e il livello di pagina. Nella tabella seguente viene illustrata la relazione tra il livello del ticket di stampa, l'interfaccia OM XPS corrispondente e i metodi utilizzati per accedere alla risorsa Print Ticket.

| Livello ticket di stampa | Interfaccia                                                | Metodo Get                                                                      | Metodo Set                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Processo                | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Documento           | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| Pagina               | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Stampa il contenuto del ticket

È possibile accedere al contenuto di una risorsa del ticket di stampa esistente leggendo dal flusso associato alla risorsa. Il metodo [**GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) dell'interfaccia [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) restituisce il puntatore a un flusso di sola lettura che contiene il contenuto in formato XML del ticket di stampa. Il formato del contenuto del ticket di stampa è descritto nella [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

È possibile creare una nuova risorsa del ticket di stampa creando una nuova interfaccia [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) . Un ticket di stampa valido in formato XML viene scritto in un flusso e viene creato un URI di parte per identificare la parte di Print Ticket. Per ulteriori informazioni sul contenuto di un Print Ticket valido, fare riferimento alla [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Il flusso e l'URI della parte vengono passati come parametri della chiamata di [**contenuto**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) per impostare la nuova risorsa del ticket di stampa e la risorsa del ticket di stampa viene aggiunta alla parte del documento corrispondente chiamando il metodo **SetPrintTicketResource** illustrato nella tabella precedente.

## <a name="print-ticket-inheritance"></a>Ereditarietà del ticket di stampa

I ticket di stampa ereditano le proprietà dei ticket di stampa con ambito maggiore. Ad esempio, un ticket di stampa a livello di documento eredita le proprietà del ticket di stampa a livello di processo associato alla sequenza del documento del documento. Analogamente, un ticket di stampa a livello di pagina eredita le proprietà del ticket di stampa a livello di documento associato al documento della pagina. In questo processo di ereditarietà, le proprietà specificate nel ticket di stampa di livello inferiore eseguono l'override delle proprietà corrispondenti che verrebbero altrimenti ereditate dal ticket di stampa di livello superiore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



