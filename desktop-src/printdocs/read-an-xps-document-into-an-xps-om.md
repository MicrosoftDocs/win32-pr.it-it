---
description: Viene descritto come leggere un documento XPS esistente da un file in un OM XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Leggere un documento XPS in un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348221"
---
# <a name="read-an-xps-document-into-an-xps-om"></a>Leggere un documento XPS in un OM XPS

Viene descritto come leggere un documento XPS esistente da un file in un OM XPS.

Per creare un oggetto XPS OM da un documento XPS, chiamare il metodo [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .

Prima di usare questi esempi di codice nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Esempio di codice

Nell'esempio di codice seguente si presuppone che l'inizializzazione descritta in [Initialize a XPS om](xps-object-model-initialization.md) abbia avuto esito positivo.


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



Per creare un oggetto XPS OM da un documento XPS archiviato come flusso, chiamare [**IXpsOMObjectFactory:: CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).

## <a name="remarks"></a>Commenti

Se si scrive un OM XPS immediatamente dopo aver letto un pacchetto XPS, è possibile che alcuni contenuti originali vengano persi o modificati.

Alcune delle modifiche che possono verificarsi in questo caso sono elencate nella tabella seguente:

| Funzionalità del documento                      | Azione                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| Firme digitali<br/>         | Rimosso dal documento<br/>                               |
| Parte DiscardControl<br/>        | Rimosso dal documento<br/>                               |
| Parti del documento esterno<br/>     | Rimosso dal documento<br/>                               |
| Markup FixedPage<br/>           | Modificato dall'originale<br/>                              |
| Markup del dizionario risorse<br/> | Modificato dall'originale, se è impostato il flag di ottimizzazione<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Esplorare XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[Scrivere testo in un OM XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Creare grafica in un OM XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Inserire immagini in un OM XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Usato in questa sezione**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

**Per ulteriori informazioni**
</dt> <dt>

[Inizializzare un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[API per la creazione di pacchetti](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

