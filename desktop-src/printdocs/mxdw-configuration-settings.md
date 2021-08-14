---
description: Il Microsoft XPS Document Writer (MXDW) consente agli utenti di creare file di documenti XPS stampando da qualsiasi Windows applicazione.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Configurazione di MXDW Impostazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75d45ea3ad9c8c74280d1e70e418ee0bf4823d1f0332e3d5c772d29976cf2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971190"
---
# <a name="mxdw-configuration-settings"></a>Configurazione di MXDW Impostazioni

Il Microsoft XPS Document Writer (MXDW) consente agli utenti di creare file di documenti XPS stampando da qualsiasi Windows applicazione. Gli sviluppatori di applicazioni possono controllare le impostazioni di output seguenti di MXDW usando le parti PrintTicket e PrintCapabilities dello [schema di stampa.](./printschema.md)

## <a name="jobinterleaving"></a>JobInterleaving

L'impostazione JobInterleaving controlla l'ordine di interfoliazione del contenuto per i documenti XPS. Per informazioni sull'interfoliazione dei processi, vedere [l'XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf). MXDW supporta le due opzioni seguenti per questa impostazione:

-   **Off:** questa opzione disabilita l'interfoliazione in modo che tutti i dati per ogni elemento di contenuto nel documento siano contigui, migliorando così l'efficienza dell'accesso casuale. Questa opzione è ideale per la visualizzazione di un documento XPS.
-   **Sì:** questa opzione abilita l'interfoliazione in modo che i dati per ogni elemento di contenuto vengono suddivisi e riordinati per un'elaborazione sequenziale più efficiente. Questa opzione è ideale per il download Web e la stampa.

L'esempio seguente è un esempio del file XML PrintCapabilities che include l'impostazione JobInterleaving.


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



Il codice XML PrintTicket è simile, ad eccezione del fatto che specifica un'opzione specifica. Per informazioni [dettagliate, vedere Schema](./printschema.md) di stampa.

Poiché JobInterleaving non è una delle parole chiave pubbliche dello [schema](./print-schema-public-keywords.md)di stampa , è necessario includere una dichiarazione dello spazio dei nomi (in questo caso "ns0000" nel tag **PrintCapabilities** (o **PrintTicket**) all'inizio del documento PrintCapabilities (o PrintTicket), come illustrato nell'esempio seguente:


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>JobImageType

JobImageType controlla il formato di output dei formati bitmap incorporati. MXDW supporta le quattro opzioni seguenti per questa impostazione:

-   **JPEGHigh:** questa opzione specifica l'immagine JPEG con un livello elevato di compressione. Questa opzione produce le dimensioni del file più piccole, ma la qualità dell'immagine più bassa.
-   **JPEGMed:** questa opzione specifica l'immagine JPEG con un livello medio di compressione. Questa opzione offre il miglior equilibrio tra dimensioni del file e qualità dell'immagine.
-   **JPEGLow:** questa opzione specifica l'immagine JPEG con un basso livello di compressione. Questa opzione produce la riduzione minima delle dimensioni del file e la qualità elevata dell'immagine.
-   **PNG:** questa opzione specifica il formato di immagine PNG con compressione senza perdita di dati. Questa opzione produce le dimensioni massime del file e la massima qualità dell'immagine.

Il file XML PrintCapabilities dell'impostazione JobImageType viene visualizzato di seguito:


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



Il codice XML PrintTicket è simile, ad eccezione del fatto che specifica un'opzione specifica. Per informazioni [dettagliate, vedere Schema](./printschema.md) di stampa.

Poiché JobImageType non è una delle parole chiave pubbliche dello [schema](./print-schema-public-keywords.md)di stampa , è necessario includere una dichiarazione dello spazio dei nomi (in questo caso "ns0000" nel tag **PrintCapabilities** (o **PrintTicket**) all'inizio del documento PrintCapabilities (o PrintTicket), come illustrato nell'esempio seguente:


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

[Schema di stampa](./printschema.md)
</dt> <dt>

[Specifiche XPS e download delle licenze](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
