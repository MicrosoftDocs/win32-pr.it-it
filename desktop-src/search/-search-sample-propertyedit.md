---
description: Nell'esempio di codice PropertyEdit viene illustrato come convertire il nome di proprietà canonico in un PROPERTYKEY, impostare il valore dell'archivio delle proprietà su quello dell'elemento e riscrivere i dati nel flusso di file.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878810"
---
# <a name="propertyedit"></a>PropertyEdit

Nell'esempio di codice PropertyEdit viene illustrato come convertire il nome di proprietà canonico in un PROPERTYKEY, impostare il valore dell'archivio delle proprietà su quello dell'elemento e riscrivere i dati nel flusso di file.

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



| Location      | URL percorso                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Esempio PropertyEdit](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **PropertyEdit** . 
2.  Immettere `msbuild PropertyEdit.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **PropertyEdit** .
2.  Fare doppio clic sull'icona per il file PropertyEdit. sln per aprire il progetto in Visual Studio.
    > [!Note]  
    > L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite. In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.
2.  Al prompt dei comandi, immettere `PropertyEdit.exe` o da Esplora risorse, fare doppio clic sull'icona per PropertyEdit.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Esempi di codice di ricerca](-search-samples-ovw.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[Informazioni sulle proprietà e sui gestori di proprietà](../properties/building-property-handlers-properties.md)
</dt> <dt>

[Schema Descrizione proprietà](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
