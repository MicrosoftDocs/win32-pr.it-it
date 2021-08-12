---
title: Modifica dei valori degli attributi
description: Modifica dei valori degli attributi
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
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
- attributi,modifica dei valori
- modifica dei valori degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870d8bfa13012bd79fdd672f1543db4a484ca5d9674ef1a9e48e832119ea1b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581117"
---
# <a name="changing-attribute-values"></a>Modifica dei valori degli attributi

È possibile modificare il valore di un attributo se la pagina Web o l'applicazione ha accesso in lettura/scrittura alla libreria e l'attributo può essere letto e scritto.

È possibile modificare un attributo dell'elemento multimediale corrente. Per modificare gli attributi di più elementi multimediali, è possibile assegnare ognuno a turno al *lettore*. **proprietà currentMedia.**

In questo argomento **l'oggetto Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Per modificare un attributo, chiamare *player*. *currentMedia*. **Metodo setItemInfo** come illustrato nell'esempio C# seguente.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



È consigliabile chiamare media *.* **Metodo isReadOnlyItem** per determinare se è possibile modificare un attributo specifico.

> [!Note]  
> Se si incorpora il controllo nell'applicazione, gli attributi di file che si modificano non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player. Se si usa il controllo in un'applicazione remota scritta in C++, gli attributi di file che si modificano verranno scritti nel file multimediale digitale poco dopo aver apportato le modifiche. In entrambi i casi, le modifiche sono immediatamente disponibili tramite la libreria.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi dell'elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Accesso alla libreria**](library-access.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Lettura dei valori degli attributi**](reading-attribute-values.md)
</dt> </dl>

 

 




