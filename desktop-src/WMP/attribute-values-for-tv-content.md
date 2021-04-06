---
title: Valori di attributo per il contenuto TV
description: Valori di attributo per il contenuto TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Media Player di Windows, attributi per elementi multimediali
- Modello a oggetti di Windows Media Player, attributi per elementi multimediali
- modello a oggetti, attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX di Windows Media Player, attributi per elementi multimediali
- Controllo ActiveX Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX, attributi per elementi multimediali
- Windows Media Player Library, attributi per elementi multimediali
- libreria, attributi per elementi multimediali
- attributi, contenuto TV
- Valori degli attributi di contenuto TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045351"
---
# <a name="attribute-values-for-tv-content"></a>Valori di attributo per il contenuto TV

In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Windows Media Player 10 o versione successiva può organizzare il contenuto della TV nella libreria. Windows Media Player considera il contenuto TV come una sottocategoria di contenuto video. Per visualizzare il contenuto video nei nodi TV della libreria, impostare gli attributi **WM/MediaClassPrimaryID** e **WM/MediaClassSecondaryID** sui valori nella tabella seguente utilizzando il *supporto*. metodo **setItemInfo** :



| Attributo                    | Valore                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

È anche possibile usare questi valori per determinare se un particolare elemento multimediale digitale contiene contenuto TV usando il *supporto*. **GetItemInfo** o *supporti*. metodi **getItemInfoByType** .

Ricordarsi di usare i valori **GUID** come valori **stringa** quando si specificano o si recuperano questi valori.

Il codice di esempio C# seguente imposta gli attributi della classe multimediale in modo che un elemento multimediale venga identificato come contenuto TV.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Per ulteriori informazioni sui possibili valori per gli attributi delle classi multimediali, vedere le [linee guida sull'utilizzo dei metadati di Windows Media](/previous-versions/ms867702(v=msdn.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Accesso alla libreria**](library-access.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> </dl>

 

 




