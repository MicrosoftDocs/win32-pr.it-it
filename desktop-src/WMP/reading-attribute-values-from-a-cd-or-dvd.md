---
title: Lettura dei valori degli attributi da un CD o DVD
description: Lettura dei valori degli attributi da un CD o DVD
ms.assetid: 441916fb-f66d-4a12-a95c-b47561c93e64
keywords:
- Windows Media Player,attributi per elementi multimediali
- Windows Media Player a oggetti, attributi per elementi multimediali
- modello a oggetti,attributi per elementi multimediali
- Windows Media Player Dispositivi mobili, attributi per elementi multimediali
- Windows Media Player ActiveX controllo, attributi per elementi multimediali
- Windows Media Player Controllo mobile ActiveX,attributi per elementi multimediali
- ActiveX, attributi per elementi multimediali
- Windows Media Player, attributi per elementi multimediali
- libreria, attributi per elementi multimediali
- attributi, lettura di valori
- lettura di valori di attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fda1bf3002f015873b69e29503ecba637a978bac1b167724c04f5f15228b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861771"
---
# <a name="reading-attribute-values-from-a-cd-or-dvd"></a>Lettura dei valori degli attributi da un CD o DVD

In questo argomento **l'oggetto Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Il codice di esempio C# seguente recupera i valori di tutti gli attributi nel disco corrente che si trova nell'unità e li scrive in un file.


```C++
private void logDiscAttributes()
{
    int iCDCount = 0; // Count of CD and DVD drives
    int iAttrCount = 0; // Attribute count.
    int iPLCount = 0; // Playlist item count.

    IWMPCdromCollection cdCollection;
    IWMPPlaylist playlist;
    IWMPMedia media;
    string strAttribName = "";
    string strAttribValue = "";
    string strText = "";

    // Create a StreamWriter object to write
    // the output to a file.
    StreamWriter sw = new StreamWriter(strOutFile, true);

    cdCollection = Player.cdromCollection;
    iCDCount = cdCollection.count;

    // Loop through the CD and DVD drives.
    for (int i = 0; i < iCDCount; i++)
    {
        playlist = cdCollection.Item(i).Playlist;

        // Loop through the playlist attributes.
        iAttrCount = playlist.attributeCount;
        for (int j = 0; j < iAttrCount; j++)
        {
            strText += "Playlist Attribute: \t";
            strAttribName = playlist.get_attributeName(j);
            strText += "\t" + strAttribName + "\t";
            strAttribValue = playlist.getItemInfo(strAttribName);
            strText += strAttribValue + "\n";
        }

        // Loop through the playlist.
        iPLCount = playlist.count;
        for (int k = 0; k < iPLCount; k++)
        {
            media = playlist.get_Item(k);

            // Loop through the media attributes.
            iAttrCount = media.attributeCount;
            for (int m = 0; m < iAttrCount; m++)
            {
                strText += "Track or Chapter [" + m.ToString() + "]";
                strAttribName = media.getAttributeName(m);
                strText += "\t" + strAttribName + "\t";
                strText += "Read Only: " + media.isReadOnlyItem(strAttribName) + "\t";
                strAttribValue = media.getItemInfo(strAttribName);
                strText += strAttribValue + "\n";
            }
        }
    }

    sw.Write(strText);
    sw.Close();

    MessageBox.Show(strOutFile + " created");
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi degli elementi multimediali**](media-item-attributes.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> </dl>

 

 




