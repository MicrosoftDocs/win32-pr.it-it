---
description: Voci del registro di sistema Decoder-Specific
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Voci del registro di sistema Decoder-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319116"
---
# <a name="decoder-specific-registry-entries"></a>Voci del registro di sistema Decoder-Specific


Oltre alle voci del registro di sistema necessarie per tutti i codificatori e i decodificatori, le voci del registro di sistema seguenti sono necessarie specificamente per i decodificatori.

Queste voci registrano il decodificatore sotto la categoria di decodificatori di Windows Imaging Component (WIC). Il primo GUID in queste voci è l'identificatore di categoria (CATId) per [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

Come indicato nella sezione [individuazione ed arbitraggio](-wic-howwicworks.md) del funzionamento del componente Imaging di Windows, il meccanismo che consente di individuare un decodificatore appropriato per un'immagine specifica in fase di esecuzione è basato sulla corrispondenza di uno schema di identificazione incorporato nel file di immagine con un modello specificato nella voce del registro di sistema del decodificatore. Per abilitare l'individuazione in fase di esecuzione dei decodificatori, è necessario registrare il modello di identificazione univoco per il formato di immagine come indicato di seguito. Tutte queste voci del registro di sistema sono necessarie, ad eccezione della voce **EndOfStream** , che è facoltativa, come descritto nella tabella seguente.

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| Valore       | Descrizione                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posizione    | Offset nel file in cui è possibile trovare il modello.                                                                                                                                                                                                                                                                        |
| Length      | Lunghezza del modello.                                                                                                                                                                                                                                                                                                      |
| Modello     | Bit effettivi che costituiscono il modello. Si tratta dei bit che corrispondono al modello di identificazione in un file di immagine durante l'individuazione.                                                                                                                                                                                |
| Mask        | Consente i valori jolly nei criteri. La maschera viene applicata eseguendo un'operazione AND logica sul modello e sulla maschera. Qualsiasi bit del modello che corrisponde a un bit nella maschera con un valore pari a 0 viene ignorato.                                                                                                       |
| EndOfStream | L'offset del pattern di identificazione deve essere calcolato dalla fine del flusso, anziché dall'inizio. Alcuni formati di immagine posizionano il modello di identificazione alla fine del file o in prossimità della fine del file. Poiché l'impostazione predefinita prevede la ricerca dall'inizio, a meno che il modello non sia vicino alla fine del file, è possibile omettere questa voce. |



 

Un codec può supportare più di un modello di identificazione. In tal caso, è necessario ripetere tutte le chiavi in **HKEY \_ classi \_ radice \\ CLSID \\ {decodificatore CLSID} \\ modelli** e usare la chiave numerica (0 nell'esempio) per distinguere tra i diversi modelli. È necessario includere ognuno dei quattro valori sotto la chiave per ogni modello.

## <a name="registering-a-container-format-with-metadata-readers"></a>Registrazione di un formato contenitore con i lettori di metadati

Se si crea un nuovo formato del contenitore per il codec, è necessario creare anche le voci del registro di sistema per supportare l'individuazione dei lettori di metadati per i blocchi di metadati nelle immagini, proprio come per i writer dei metadati. È necessario creare le voci seguenti nell'identificatore di classe (CLSID) del lettore di metadati per ogni formato di metadati supportato dal formato del contenitore. Si noti che, se il codec usa un contenitore Tagged Image File Format (TIFF), queste informazioni sono già presenti nel registro di sistema.

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

Poiché le voci per i lettori di metadati vengono usate anche per l'individuazione, sono molto simili alle voci per i decodificatori. Queste voci vengono usate dalla factory dei componenti per trovare i lettori di metadati supportati dal contenitore e per selezionare quello appropriato, quando l'implementazione di [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) richiede un lettore di metadati.



| Valore      | Descrizione                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posizione   | Offset nel contenitore del blocco di metadati in cui è possibile trovare l'intestazione dei metadati. Per i blocchi di metadati di primo livello, si tratta dell'offset nel flusso di file. Per i blocchi di metadati annidati in altri blocchi di metadati, si tratta dell'offset rispetto al blocco di metadati contenitore. |
| Modello    | Bit effettivi che costituiscono il modello. Si tratta dei bit che corrispondono al modello di identificazione in un file di immagine durante l'individuazione.                                                                                                                            |
| Mask       | L'intestazione dei metadati è generalmente definita dal gestore di metadati. È consigliabile usare l'intestazione di metadati standard per ogni lettore, a meno che, per qualche motivo, il modello deve avere un formato diverso nel contenitore.                                                          |
| DataOffset | Offset dall'inizio dell'intestazione dei metadati in corrispondenza della quale iniziano i dati effettivi. Nei casi in cui i metadati non si trovano in un offset specifico dall'intestazione, questa voce può essere omessa.                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Voci del registro di sistema specifiche del codificatore](-wic-encoderregentries.md)
</dt> <dt>

[Integrazione con raccolta foto di Windows e Esplora risorse](-wic-integrationregentries.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



