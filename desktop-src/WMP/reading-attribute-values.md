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
# <a name="reading-attribute-values"></a><span data-ttu-id="8c043-114">Lettura di valori di attributo</span><span class="sxs-lookup"><span data-stu-id="8c043-114">Reading Attribute Values</span></span>

<span data-ttu-id="8c043-115">Gli attributi che è possibile trovare nella libreria e nei file di Windows Media hanno nomi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="8c043-115">The attributes you can find in the library and in Windows Media files have predefined names.</span></span> <span data-ttu-id="8c043-116">È possibile scrivere codice che recupera il valore di un attributo passando il nome di tale attributo ai *supporti*. **GetItemInfo** o *supporti*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="8c043-116">You can write code that retrieves the value of one attribute by passing the name of that attribute to *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="8c043-117">È anche possibile scrivere codice per recuperare i valori di tutti gli attributi in un file o in un elemento.</span><span class="sxs-lookup"><span data-stu-id="8c043-117">You can also write code that retrieves the values of all of the attributes in a file or item.</span></span>

<span data-ttu-id="8c043-118">Nell'esempio C# seguente il valore dell'attributo **title** viene recuperato e visualizzato in una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="8c043-118">The following C# example retrieves the value of the **Title** attribute and displays it in a message box.</span></span> <span data-ttu-id="8c043-119">In questo esempio, l'oggetto **Player** è stato definito come AxWMPLib. AxWindowsMediaPlayer Player.</span><span class="sxs-lookup"><span data-stu-id="8c043-119">In this example, the **Player** object was defined as axWMPLib.AxWindowsMediaPlayer Player.</span></span>


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



<span data-ttu-id="8c043-120">Nella chiamata a **getItemInfoByType** il secondo parametro è una stringa che specifica la lingua.</span><span class="sxs-lookup"><span data-stu-id="8c043-120">In the call to **getItemInfoByType**, the second parameter is a string that specifies the language.</span></span> <span data-ttu-id="8c043-121">Se si passa una stringa vuota come illustrato in questo esempio, il metodo recupera il valore nella lingua predefinita.</span><span class="sxs-lookup"><span data-stu-id="8c043-121">If you pass an empty string as shown in this example, the method retrieves the value in the default language.</span></span> <span data-ttu-id="8c043-122">Per informazioni sul terzo parametro, vedere [attributi con più valori](attributes-with-multiple-values.md).</span><span class="sxs-lookup"><span data-stu-id="8c043-122">For information about the third parameter, see [Attributes with Multiple Values](attributes-with-multiple-values.md).</span></span>

<span data-ttu-id="8c043-123">Nell'esempio C# seguente vengono recuperati i valori per un determinato attributo nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="8c043-123">The following C# example retrieves the values for a given attribute in the current media item.</span></span> <span data-ttu-id="8c043-124">Restituisce questi valori come stringa delimitata da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="8c043-124">It returns these values as a semicolon-delimited string.</span></span> <span data-ttu-id="8c043-125">Si noti che per gli attributi rappresentati come oggetti, ad esempio **WM/lyrics \_ sincronizzati**, **WM/Picture** e **WM/UserWebURL**, la funzione restituisce una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="8c043-125">Note that for attributes represented as objects, such as **WM/Lyrics\_Synchronised**, **WM/Picture**, and **WM/UserWebURL**, the function returns an empty string.</span></span>


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



<span data-ttu-id="8c043-126">Il terzo argomento passato al metodo **getItemInfoByType** è l'indice di un attributo specifico in un set di attributi con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="8c043-126">The third argument passed to the **getItemInfoByType** method is the index of a particular attribute in a set of attributes with the same name.</span></span>

<span data-ttu-id="8c043-127">È possibile usare codice simile per recuperare gli attributi con nomi univoci.</span><span class="sxs-lookup"><span data-stu-id="8c043-127">You can use similar code to retrieve attributes that have unique names.</span></span> <span data-ttu-id="8c043-128">In questi casi, **getAttributeCountByType** restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="8c043-128">In those cases, **getAttributeCountByType** returns 1.</span></span> <span data-ttu-id="8c043-129">Nell'esempio illustrato in precedenza, la chiamata a **getItemInfoByType** verrebbe eseguita una sola volta.</span><span class="sxs-lookup"><span data-stu-id="8c043-129">In the example shown earlier, the call to **getItemInfoByType** would execute only once.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c043-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c043-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c043-131">**Modifica dei valori di attributo**</span><span class="sxs-lookup"><span data-stu-id="8c043-131">**Changing Attribute Values**</span></span>](changing-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="8c043-132">**Attributi elemento multimediale**</span><span class="sxs-lookup"><span data-stu-id="8c043-132">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c043-133">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="8c043-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="8c043-134">**Lettura di valori di attributo da un CD o DVD**</span><span class="sxs-lookup"><span data-stu-id="8c043-134">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




