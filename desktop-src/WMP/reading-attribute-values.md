---
title: Lettura dei valori degli attributi
description: Lettura dei valori degli attributi
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
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
- attributi,lettura di valori
- lettura dei valori degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8431405b68435f41cb357a810e30c37bb96c5971824b3878b1982986aa0d0833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002831"
---
# <a name="reading-attribute-values"></a>Lettura dei valori degli attributi

Gli attributi che è possibile trovare nella libreria e Windows file multimediali hanno nomi predefiniti. È possibile scrivere codice che recupera il valore di un attributo passando il nome di tale attributo a *Media*. **getItemInfo** o *Media*. **getItemInfoByType**. È anche possibile scrivere codice che recupera i valori di tutti gli attributi in un file o in un elemento.

L'esempio C# seguente recupera il valore **dell'attributo Title** e lo visualizza in una finestra di messaggio. In questo esempio **l'oggetto Player** è stato definito come axWMPLib.AxWindowsMediaPlayer Player.


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



Nella chiamata a **getItemInfoByType** il secondo parametro è una stringa che specifica la lingua. Se si passa una stringa vuota come illustrato in questo esempio, il metodo recupera il valore nella lingua predefinita. Per informazioni sul terzo parametro, vedere [Attributi con più valori](attributes-with-multiple-values.md).

Nell'esempio C# seguente vengono recuperati i valori per un determinato attributo nell'elemento multimediale corrente. Restituisce questi valori come stringa delimitata da punto e virgola. Si noti che per gli attributi rappresentati come oggetti, ad esempio **WM/Lyrics \_ Synchronised,** **WM/Picture** e **WM/UserWebURL,** la funzione restituisce una stringa vuota.


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



Il terzo argomento passato al **metodo getItemInfoByType** è l'indice di un attributo specifico in un set di attributi con lo stesso nome.

È possibile usare codice simile per recuperare attributi con nomi univoci. In questi casi, **getAttributeCountByType** restituisce 1. Nell'esempio illustrato in precedenza, la chiamata a **getItemInfoByType** verrebbe eseguita una sola volta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modifica dei valori degli attributi**](changing-attribute-values.md)
</dt> <dt>

[**Attributi dell'elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Lettura dei valori degli attributi da un CD o dvd**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




