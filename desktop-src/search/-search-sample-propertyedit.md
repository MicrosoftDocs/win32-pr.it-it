---
description: L'esempio di codice PropertyEdit illustra come convertire il nome canonico della proprietà in PROPERTYKEY, impostare il valore dell'archivio proprietà su quello dell'elemento e scrivere nuovamente i dati nel flusso di file.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944419f990c8f1f8b52706dbab0b08102829e77a5bfa8a91c72a5bc16eddfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944670"
---
# <a name="propertyedit"></a>PropertyEdit

L'esempio di codice PropertyEdit illustra come convertire il nome canonico della proprietà in PROPERTYKEY, impostare il valore dell'archivio proprietà su quello dell'elemento e scrivere nuovamente i dati nel flusso di file.

In questo argomento sono contenute le sezioni seguenti.

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="requirements"></a>Requisiti



| Prodotto     | Versione minima del prodotto |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località      | URL percorso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Esempio di PropertyEdit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> Per tutte le versioni di Windows, Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory **del progetto PropertyEdit.** 
2.  Immettere `msbuild PropertyEdit.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto PropertyEdit.**
2.  Fare doppio clic sull'icona per il file PropertyEdit.sln per aprire il progetto in Visual Studio.
    > [!Note]  
    > L'estensione di file sln non viene visualizzata nelle impostazioni predefinite della cartella. In questo caso, può essere identificato dalla relativa icona univoca o dalla relativa descrizione del tipo, "Microsoft Visual Studio Soluzione".

     

3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile usando la finestra del prompt dei comandi o Windows Explorer.
2.  Al prompt dei comandi immettere o in Esplora Windows fare doppio clic `PropertyEdit.exe` sull'icona per PropertyEdit.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Esempi di codice di ricerca](-search-samples-ovw.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[Informazioni su proprietà e gestori di proprietà](../properties/building-property-handlers-properties.md)
</dt> <dt>

[Schema di descrizione della proprietà](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
