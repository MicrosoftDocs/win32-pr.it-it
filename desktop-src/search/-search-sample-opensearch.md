---
description: Nell'esempio di codice OpenSearch viene illustrato come creare un servizio di ricerca federato utilizzando il protocollo OpenSearch e un file descrittore OpenSearch (con estensione osdx) (un connettore di ricerca).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401628"
---
# <a name="opensearch"></a>OpenSearch

Nell'esempio di codice OpenSearch viene illustrato come creare un servizio di ricerca federato utilizzando il protocollo [OpenSearch](https://github.com/dewitt/opensearch) e un file descrittore OpenSearch (con estensione osdx) (un connettore di ricerca).

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
| GitHub  | [Esempio OpenSearch](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.

 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **AdventureSearch** . 
2.  Immettere `msbuild AdventureSearch.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **AdventureSearch** .
2.  Fare doppio clic sull'icona per il file AdventureSearch. sln per aprire il progetto in Visual Studio.
    > [!Note]  
    > L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite. In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo, "Microsoft Visual Studio soluzione".

     

3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando la finestra del prompt dei comandi o Esplora risorse.
2.  Al prompt dei comandi, immettere `AdventureSearch.exe` o da Esplora risorse, fare doppio clic sull'icona per AdventureSearch.exe.
3.  Al prompt dei comandi, immettere `GetOSDX.exe` o da Esplora risorse, fare doppio clic sull'icona per GetOSDX.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Panoramica dello schema di descrizione del connettore di ricerca](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Esempi di codice di ricerca](-search-samples-ovw.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Schema Descrizione libreria](../shell/library-schema-entry.md)
</dt> </dl>

 

 
