---
title: Lettura di valori di attributo
description: Lettura di valori di attributo
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
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
- attributi, lettura di valori
- lettura di valori di attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298697"
---
# <a name="reading-attribute-values"></a>Lettura di valori di attributo

Gli attributi che è possibile trovare nella libreria e nei file di Windows Media hanno nomi predefiniti. È possibile scrivere codice che recupera il valore di un attributo passando il nome di tale attributo ai *supporti*. **GetItemInfo** o *supporti*. **getItemInfoByType**. È anche possibile scrivere codice per recuperare i valori di tutti gli attributi in un file o in un elemento.

Nell'esempio C# seguente il valore dell'attributo **title** viene recuperato e visualizzato in una finestra di messaggio. In questo esempio, l'oggetto **Player** è stato definito come AxWMPLib. AxWindowsMediaPlayer Player.


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



Nella chiamata a **getItemInfoByType** il secondo parametro è una stringa che specifica la lingua. Se si passa una stringa vuota come illustrato in questo esempio, il metodo recupera il valore nella lingua predefinita. Per informazioni sul terzo parametro, vedere [attributi con più valori](attributes-with-multiple-values.md).

Nell'esempio C# seguente vengono recuperati i valori per un determinato attributo nell'elemento multimediale corrente. Restituisce questi valori come stringa delimitata da punti e virgola. Si noti che per gli attributi rappresentati come oggetti, ad esempio **WM/lyrics \_ sincronizzati**, **WM/Picture** e **WM/UserWebURL**, la funzione restituisce una stringa vuota.


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



Il terzo argomento passato al metodo **getItemInfoByType** è l'indice di un attributo specifico in un set di attributi con lo stesso nome.

È possibile usare codice simile per recuperare gli attributi con nomi univoci. In questi casi, **getAttributeCountByType** restituisce 1. Nell'esempio illustrato in precedenza, la chiamata a **getItemInfoByType** verrebbe eseguita una sola volta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica dei valori di attributo**](changing-attribute-values.md)
</dt> <dt>

[**Attributi elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Lettura di valori di attributo da un CD o DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




