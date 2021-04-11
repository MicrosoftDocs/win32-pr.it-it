---
description: Viene descritto come scrivere il contenuto di un oggetto XPS OM in un programma in un file di documento XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Scrivere un OM XPS in un documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232372"
---
# <a name="write-an-xps-om-to-an-xps-document"></a>Scrivere un OM XPS in un documento XPS

Viene descritto come scrivere il contenuto di un oggetto XPS OM in un programma in un file di documento XPS.

Se un programma dispone di un OM XPS che contiene un documento completo, il programma può scrivere XPS OM in un file come documento XPS, chiamando il metodo [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) dell'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .

Prima di usare questi esempi di codice in un programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a>Scrittura di un OM XPS completo in un documento XPS

Dopo aver impostato il contenuto di un OM XPS, è possibile salvare XPS OM in un file come documento XPS, chiamando il metodo [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) dell'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> La scrittura di un modello OM XPS in un file o in un flusso non crea automaticamente un'anteprima per il documento XPS. Per creare un'anteprima del documento XPS, utilizzare l'interfaccia [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .

 

## <a name="incrementally-writing-an-xps-document"></a>Scrittura incrementale di un documento XPS

L'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) può essere utilizzata per scrivere in modo incrementale le parti di un documento XPS. ad esempio, quando le parti del documento vengono create o elaborate in sequenza.

> [!Note]  
> La scrittura di un modello OM XPS in un file o in un flusso non crea automaticamente un'anteprima per il documento XPS. Per creare un'anteprima del documento XPS, utilizzare l'interfaccia [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Stampare un OM XPS](print-an-xps-om.md)
</dt> <dt>

**Usato in questa sezione**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

**Per ulteriori informazioni**
</dt> <dt>

[Inizializzare un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
