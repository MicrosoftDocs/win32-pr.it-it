---
title: Esempio di documento ServiceInfo per un negozio online di tipo 2
description: Esempio di documento ServiceInfo per un negozio online di tipo 2
ms.assetid: d9bbce89-15b4-495f-8995-24dda99a4f40
keywords:
- Windows Media Player negozi online, esempio di documento ServiceInfo
- negozi online, documento ServiceInfo di esempio
- Tipo 2 di negozi online, esempio di documento ServiceInfo
- Windows Media Player negozi online, documento ServiceInfo
- negozi online, documento ServiceInfo
- Tipo 2 negozi online, documento ServiceInfo
- Windows Media Player negozi online, esempio di codice
- negozi online, esempio di codice
- Tipo 2 di negozi online, esempio di codice
- Esempio di documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7962f7548f8c880e60320d3a7fb071e2a076ffafdac9a56b4cf6d8aa41b5d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650121"
---
# <a name="example-serviceinfo-document-for-a-type-2-online-store"></a>Esempio di documento ServiceInfo per un negozio online di tipo 2

L'esempio di codice seguente illustra un documento ServiceInfo.xml completo. È possibile usare questo codice XML come punto di partenza per il documento ServiceInfo.


```C++
<?xml version="1.0" encoding="utf-8" ?>
<ServiceInfo Version="1.00" Key="Proseware">
    <FriendlyName>Proseware Service</FriendlyName>
    <Image 
        MenuURL = "https://www.proseware.com/service/images/menuicon.jpg"
        ServiceLargeURL = "https://www.proseware.com/service/images/30x30.jpg" />
    <Color
        MediaPlayer = "#FF8040"
        MediaPlayerText = "#FFFFFF"/>
    <ServiceTask1
        URL = "https://www.proseware.com/service/html/Music.asp">
        <ButtonText>Proseware\nMusic</ButtonText>
        <ButtonTip>Proseware Music Store</ButtonTip>
    </ServiceTask1>
    <ServiceTask2
        URL = "https://www.proseware.com/service/html/Video.asp">
        <ButtonText>Proseware\nVideo</ButtonText>
        <ButtonTip>Proseware Video</ButtonTip>
    </ServiceTask2>
    <ServiceTask3
        URL = "https://www.proseware.com/service/html/Radio.asp">
        <ButtonText>Proseware\nRadio</ButtonText>
        <ButtonTip>Proseware Radio</ButtonTip>
    </ServiceTask3>
    <Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
    </Navigate>
    <InfoCenter
        URL = "https://www.proseware.com/service/html/InfoCenter.asp"/>
    <AlbumInfo
        URL = "https://www.proseware.com/service/html/AlbumInfo.asp"/>
    <BuyCD
        MediaPlayerURL = "https://www.proseware.com/service/html/BuyCDMediaPlayer.asp"
        MediaCenterURL = "https://www.proseware.com/service/html/BuyCDMediaCenter.asp"
        BrowserURL = "https://www.proseware.com/service/html/BuyCDBrowser.asp"/>
    <DownloadStatus
        URL = "https://www.proseware.com/service/html/Music_Download.htm"/>
    <HTMLView
        BaseURL = "https://www.proseware.com/"/>
</ServiceInfo>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi online di tipo 2**](programming-guide-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo per un Negozio online di tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




