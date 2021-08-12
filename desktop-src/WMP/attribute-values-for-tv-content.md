---
title: Valori degli attributi per il contenuto TV
description: Valori degli attributi per il contenuto TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Windows Media Player,attributi per elementi multimediali
- Windows Media Player a oggetti, attributi per elementi multimediali
- modello a oggetti,attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Windows Media Player ActiveX, attributi per elementi multimediali
- Windows Media Player Controllo ActiveX per dispositivi mobili, attributi per elementi multimediali
- ActiveX, attributi per elementi multimediali
- Windows Media Player,attributi per elementi multimediali
- libreria,attributi per elementi multimediali
- attributi, contenuto TV
- Valori degli attributi del contenuto TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96f855d90fe0b65c4e9483dcb2ba4ae3ff7be049f1346f1038097789b2126c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583032"
---
# <a name="attribute-values-for-tv-content"></a>Valori degli attributi per il contenuto TV

In questo argomento **l'oggetto Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Windows Media Player 10 o versioni successive può organizzare il contenuto TV nella libreria. Windows Media Player tratta il contenuto TV come una sottocategoria di contenuto video. Per visualizzare il contenuto video nei nodi TV della libreria, impostare gli attributi **WM/MediaClassPrimaryID** e **WM/MediaClassSecondaryID** sui valori nella tabella seguente usando il supporto *.* **Metodo setItemInfo:**



| Attributo                    | Valore                                |
|------------------------------|--------------------------------------|
| **WM/MediaClassPrimaryID**   | DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B |
| **WM/MediaClassSecondaryID** | BA7F258A-62F7-47A9-B21F-4651C42A000E |



 

È anche possibile usare questi valori per determinare se un particolare elemento multimediale digitale contiene contenuto TV usando il *supporto*. **getItemInfo o** *supporti*. **Metodi getItemInfoByType.**

Ricordarsi di usare **i valori GUID** come **valori** stringa quando si specificano o si recuperano questi valori.

Il codice di esempio C# seguente imposta gli attributi della classe media in modo che un elemento multimediale sia identificato come contenuto TV.


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



Per altre informazioni sui valori possibili per gli attributi della classe media, vedere le linee guida per [l'Windows di](/previous-versions/ms867702(v=msdn.10))utilizzo dei metadati multimediali .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi dell'elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Accesso alla libreria**](library-access.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> </dl>

 

 




