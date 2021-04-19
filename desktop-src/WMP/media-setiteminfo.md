---
title: Media. setItemInfo, metodo
description: Il metodo setItemInfo imposta il valore dell'attributo specificato per l'elemento multimediale corrente.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player, classe media
- Media class Media Player Windows, metodo setItemInfo
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330362"
---
# <a name="mediasetiteminfo-method"></a><span data-ttu-id="12256-106">Media. setItemInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="12256-106">Media.setItemInfo method</span></span>

<span data-ttu-id="12256-107">Il metodo **setItemInfo** imposta il valore dell'attributo specificato per l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="12256-107">The **setItemInfo** method sets the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="12256-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12256-108">Syntax</span></span>


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="12256-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="12256-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12256-110">*attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12256-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12256-111">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="12256-111">**String** containing the attribute name.</span></span> <span data-ttu-id="12256-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="12256-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="12256-113">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="12256-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12256-114">**Stringa** che contiene il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="12256-114">**String** containing the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12256-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12256-115">Return value</span></span>

<span data-ttu-id="12256-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="12256-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12256-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="12256-117">Remarks</span></span>

<span data-ttu-id="12256-118">La proprietà **attributeCount** contiene il numero di attributi disponibili per un determinato oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="12256-118">The **attributeCount** property contains the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="12256-119">I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare i nomi degli attributi predefiniti che possono essere usati con questo metodo.</span><span class="sxs-lookup"><span data-stu-id="12256-119">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="12256-120">Prima di usare questo metodo, usare il metodo **isReadOnlyItem** per determinare se è possibile impostare un particolare attributo.</span><span class="sxs-lookup"><span data-stu-id="12256-120">Before using this method, use the **isReadOnlyItem** method to determine whether a particular attribute can be set.</span></span>

<span data-ttu-id="12256-121">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="12256-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="12256-122">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="12256-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="12256-123">**Nota**</span><span class="sxs-lookup"><span data-stu-id="12256-123">**Note**</span></span>

<span data-ttu-id="12256-124">Se si incorpora il controllo Windows Media Player nell'applicazione, gli attributi di file modificati non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="12256-124">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="12256-125">Se si usa il controllo in un'applicazione remota scritta in C++, gli attributi di file che vengono modificati verranno scritti nel file multimediale digitale subito dopo aver apportato le modifiche.</span><span class="sxs-lookup"><span data-stu-id="12256-125">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="12256-126">In entrambi i casi, le modifiche sono immediatamente disponibili per il codice tramite la libreria.</span><span class="sxs-lookup"><span data-stu-id="12256-126">In either case, the changes are immediately available to your code through the library.</span></span>

<span data-ttu-id="12256-127">**Windows Media Player 10 Mobile:** Questo metodo non è implementato.</span><span class="sxs-lookup"><span data-stu-id="12256-127">**Windows Media Player 10 Mobile:** This method is not implemented.</span></span>

## <a name="examples"></a><span data-ttu-id="12256-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="12256-128">Examples</span></span>

<span data-ttu-id="12256-129">Nell'esempio JScript seguente viene usato il *supporto*. **setItemInfo** per modificare il valore dell'attributo genre per l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="12256-129">The following JScript example uses *Media*.**setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="12256-130">Un elemento input di testo HTML denominato genText consente all'utente di immettere una stringa di testo, che viene quindi usata per modificare le informazioni sugli attributi.</span><span class="sxs-lookup"><span data-stu-id="12256-130">An HTML TEXT input element named genText allows the user to enter a text string, which is then used to change the attribute information.</span></span> <span data-ttu-id="12256-131">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="12256-131">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a><span data-ttu-id="12256-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12256-132">Requirements</span></span>



| <span data-ttu-id="12256-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="12256-133">Requirement</span></span> | <span data-ttu-id="12256-134">Valore</span><span class="sxs-lookup"><span data-stu-id="12256-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12256-135">Versione</span><span class="sxs-lookup"><span data-stu-id="12256-135">Version</span></span><br/> | <span data-ttu-id="12256-136">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="12256-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="12256-137">DLL</span><span class="sxs-lookup"><span data-stu-id="12256-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="12256-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12256-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12256-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12256-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12256-140">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="12256-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="12256-141">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="12256-141">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="12256-142">**Media. isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="12256-142">**Media.isReadOnlyItem**</span></span>](media-isreadonlyitem.md)
</dt> <dt>

[<span data-ttu-id="12256-143">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="12256-143">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="12256-144">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="12256-144">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





