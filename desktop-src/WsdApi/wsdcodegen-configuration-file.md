---
description: Descrive il file di configurazione WsdCodeGen.
ms.assetid: 6dc340db-221e-4389-ba76-9f189f91866b
title: File di configurazione WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8c252c5361fda411e2b7eca4f906ba92085a552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130951"
---
# <a name="wsdcodegen-configuration-file"></a>File di configurazione WsdCodeGen

Un file di configurazione WsdCodeGen viene in genere generato dallo strumento WsdCodeGen. È possibile creare manualmente i file di configurazione, ma la complessità e la lunghezza del file in genere impediscono la codifica manuale. Per generare il file è consigliabile usare WsdCodeGen. Per ulteriori informazioni sulla generazione dei file di configurazione, vedere Utilizzo della [sintassi della riga di comando](wsdcodegen-command-line-syntax.md) [WsdCodeGen](using-wsdcodegen.md) e WsdCodeGen.

Esaminare il file di configurazione generato e, se necessario, modificarlo prima di utilizzarlo per creare codice sorgente. Il file di configurazione generato da WsdCodeGen è in genere sufficiente per la maggior parte dello sviluppo client.

Per usare il file di configurazione per lo sviluppo del server, sono necessarie alcune modifiche. Se l'hosting è abilitato, ovvero se è selezionata la modalità "tutti" o "host", modificare il contenuto dell'elemento [**ThisModelMetadata**](thismodelmetadata.md) e i relativi elementi figlio in base alle esigenze. Inoltre, modificare o rimuovere gli elementi [**PnPXDeviceCategory**](/windows/desktop/WsdApi/pnpxdevicecategory), [**PnPXHardwareId**](pnpxhardwareid.md)e [**PnPXCompatibleId**](/windows/desktop/WsdApi/pnpxcompatibleid) all'interno dell'elemento **ThisModelMetadata** o degli elementi [**ospitati**](hosted.md) , se necessario.

Un file di configurazione è costituito da una sequenza di elementi che forniscono i dati di input per la generazione di codice seguita da un numero qualsiasi di elementi [**file**](file.md) che descrivono i file da generare. I dati di input includono alcune proprietà globali e riferimenti ai tipi espressi in WSDL, XSD e assembly gestiti. Gli elementi text e CDATA negli elementi **file** vengono scritti nei file generati senza alcuna modifica. Gli altri elementi negli elementi **file** vengono sostituiti nei file generati con il codice generato.

È necessario che i file di configurazione XML seguano alcune regole generali per essere formattati correttamente per l'uso con l'utilità Generatore di codice. Si tratta di:

-   L'elemento radice di un file di configurazione è [**wsdCodeGen**](wsdcodegen.md).

-   Gli elementi che contengono tipi di dati semplici sono intercambiabili con gli attributi. Ad esempio:

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    Equivale a:

    ``` syntax
    <wsdCodeGen layerNumber="1"/>
    ```

-   In generale, non esiste alcun vincolo sull'ordinamento degli elementi. Ad esempio:

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
        <layerPrefix>MEDIA_</layerPrefix>
    </wsdCodeGen>
    ```

    Equivale a:

    ``` syntax
    <wsdCodeGen>
        <layerPrefix>MEDIA_</layerPrefix>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    Tuttavia, il generatore di codice elabora il file di configurazione in un unico passaggio e l'ordinamento ha una certa rilevanza. Ad esempio, gli elementi di [**file**](file.md) che generano codice relativo a un particolare tipo di porta devono essere eseguiti dopo l'elemento che indica al generatore di codice di leggere il contratto del tipo di porta.

Per un elenco completo degli elementi usati nei file di configurazione WsdCodeGen, vedere [riferimento XML del file di configurazione WsdCodeGen](wsdcodegen-configuration-file-xml-reference.md).

I file di configurazione di esempio sono inclusi nel Windows SDK. Per ulteriori informazioni, vedere [WSDAPI Samples](wsdapi-samples.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su WsdCodeGen](about-wsdcodegen.md)
</dt> <dt>

[Esempi di WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 
