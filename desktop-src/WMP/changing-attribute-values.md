---
title: Modifica dei valori di attributo
description: Modifica dei valori di attributo
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
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
- attributi, modifica di valori
- modifica dei valori di attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044865"
---
# <a name="changing-attribute-values"></a>Modifica dei valori di attributo

È possibile modificare il valore di un attributo se la pagina Web o l'applicazione ha accesso in lettura/scrittura alla libreria e l'attributo può essere letto e scritto.

È possibile modificare un attributo dell'elemento multimediale corrente. Per modificare gli attributi di più elementi multimediali, è possibile assegnare ognuno di essi a turno al *lettore*. proprietà **currentMedia** .

In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Per modificare un attributo, chiamare il *lettore*. *currentMedia*. metodo **setItemInfo** come illustrato nell'esempio di C# seguente.


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



Si consiglia di chiamare il *supporto*. metodo **isReadOnlyItem** per determinare se è possibile modificare un attributo specifico.

> [!Note]  
> Se si incorpora il controllo nell'applicazione, gli attributi di file modificati non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player. Se si usa il controllo in un'applicazione remota scritta in C++, gli attributi di file che vengono modificati verranno scritti nel file multimediale digitale subito dopo aver apportato le modifiche. In entrambi i casi, le modifiche sono immediatamente disponibili tramite la libreria.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Accesso alla libreria**](library-access.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Lettura di valori di attributo**](reading-attribute-values.md)
</dt> </dl>

 

 




