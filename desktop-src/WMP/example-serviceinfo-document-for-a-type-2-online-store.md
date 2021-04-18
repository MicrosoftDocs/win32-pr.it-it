---
title: Documento ServiceInfo di esempio per un negozio online di tipo 2
description: Documento ServiceInfo di esempio per un negozio online di tipo 2
ms.assetid: d9bbce89-15b4-495f-8995-24dda99a4f40
keywords:
- Windows Media Player Online Stores, esempio di documento ServiceInfo
- archivi online, documento ServiceInfo di esempio
- digitare 2 negozi online, esempio di documento ServiceInfo
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- Windows Media Player Online Stores, esempio di codice
- negozi online, esempio di codice
- digitare 2 negozi online, esempio di codice
- documento ServiceInfo di esempio
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02214b9d7180296fa11bb877f978c6bde85f3a4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298531"
---
# <a name="example-serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="fa9e2-114">Documento ServiceInfo di esempio per un negozio online di tipo 2</span><span class="sxs-lookup"><span data-stu-id="fa9e2-114">Example ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="fa9e2-115">Nell'esempio di codice seguente viene illustrato un documento di ServiceInfo.xml completo.</span><span class="sxs-lookup"><span data-stu-id="fa9e2-115">The following code example shows a complete ServiceInfo.xml document.</span></span> <span data-ttu-id="fa9e2-116">È possibile usare questo codice XML come punto di partenza per il proprio documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="fa9e2-116">You can use this XML as a starting point for your own ServiceInfo document.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fa9e2-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa9e2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa9e2-118">**Guida per programmatori per i negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="fa9e2-118">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fa9e2-119">**Documento ServiceInfo per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="fa9e2-119">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="fa9e2-120">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="fa9e2-120">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




