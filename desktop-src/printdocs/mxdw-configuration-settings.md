---
description: Microsoft XPS Document Writer (MXDW) consente agli utenti di creare file di documenti XPS stampando da qualsiasi applicazione Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Impostazioni di configurazione di MXDW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320965"
---
# <a name="mxdw-configuration-settings"></a>Impostazioni di configurazione di MXDW

Microsoft XPS Document Writer (MXDW) consente agli utenti di creare file di documenti XPS stampando da qualsiasi applicazione Windows. Gli sviluppatori di applicazioni possono controllare le seguenti impostazioni di output di MXDW utilizzando le parti PrintTicket e PrintCapabilities dello [schema di stampa](./printschema.md).

## <a name="jobinterleaving"></a>JobInterleaving

L'impostazione JobInterleaving controlla l'ordine di interfoliazione del contenuto per i documenti XPS. Per informazioni sull'interfoliazione dei processi, vedere la [specifica del documento XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf). MXDW supporta le due opzioni seguenti per questa impostazione:

-   **Off** : questa opzione Disabilita l'interfoliazione in modo che tutti i dati per ogni elemento contenuto nel documento siano contigui, migliorando così l'efficienza dell'accesso casuale. Questa opzione è consigliata per la visualizzazione di un documento XPS.
-   **On** : questa opzione consente l'interfoliazione in modo che i dati per ogni elemento di contenuto vengano suddivisi e riordinati per un'elaborazione sequenziale più efficiente. Questa opzione è consigliata per il download e la stampa Web.

Nell'esempio seguente viene riportato un esempio del codice XML PrintCapabilities che include l'impostazione JobInterleaving.


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



Il codice XML PrintTicket è simile, ad eccezione del fatto che specifica una particolare opzione. Per informazioni dettagliate, vedere lo [schema di stampa](./printschema.md) .

Poiché JobInterleaving non è una delle [parole chiave pubbliche dello schema di stampa](./print-schema-public-keywords.md), è necessario includere una dichiarazione dello spazio dei nomi (in questo caso "ns0000" nel tag **PrintCapabilities** (o **PrintTicket**) all'inizio del documento PrintCapabilities (o PrintTicket), come illustrato nell'esempio seguente:


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>JobImageType

JobImageType controlla il formato di output dei formati bitmap incorporati. MXDW supporta le quattro opzioni seguenti per questa impostazione:

-   **JPEGHigh** : questa opzione specifica l'immagine JPEG con un livello elevato di compressione. Questa opzione produce le dimensioni del file più piccole, ma la qualità dell'immagine più bassa.
-   **JPEGMed** : questa opzione specifica l'immagine JPEG con un livello di compressione medio. Questa opzione offre il migliore equilibrio tra dimensioni del file e qualità dell'immagine.
-   **JPEGLow** : questa opzione specifica l'immagine JPEG con un basso livello di compressione. Questa opzione produce una riduzione minima delle dimensioni dei file e della qualità dell'immagine elevata.
-   **Png** : questa opzione specifica il formato dell'immagine PNG con compressione senza perdita di perdite. Questa opzione produce le dimensioni massime del file e la qualità dell'immagine più elevata.

Di seguito è riportato il codice XML PrintCapabilities dell'impostazione JobImageType:


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



Il codice XML PrintTicket è simile, ad eccezione del fatto che specifica una particolare opzione. Per informazioni dettagliate, vedere lo [schema di stampa](./printschema.md) .

Poiché JobImageType non è una delle [parole chiave pubbliche dello schema di stampa](./print-schema-public-keywords.md), è necessario includere una dichiarazione dello spazio dei nomi (in questo caso "ns0000" nel tag **PrintCapabilities** (o **PrintTicket**) all'inizio del documento PrintCapabilities (o PrintTicket), come illustrato nell'esempio seguente:


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Stampa schema](./printschema.md)
</dt> <dt>

[Specifiche XPS e download delle licenze](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
