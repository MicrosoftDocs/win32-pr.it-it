---
title: Media.name
description: La proprietà Name specifica o Recupera il nome dell'elemento multimediale.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media Player Windows Media.name
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329306"
---
# <a name="medianame"></a><span data-ttu-id="7f4f4-104">Media.name</span><span class="sxs-lookup"><span data-stu-id="7f4f4-104">Media.name</span></span>

<span data-ttu-id="7f4f4-105">La proprietà **Name** specifica o Recupera il nome dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-105">The **name** property specifies or retrieves the name of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f4f4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f4f4-106">Syntax</span></span>

<span data-ttu-id="7f4f4-107">*Player*. *currentMedia*. **nome**</span><span class="sxs-lookup"><span data-stu-id="7f4f4-107">*player*.*currentMedia*.**name**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7f4f4-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="7f4f4-108">Possible Values</span></span>

<span data-ttu-id="7f4f4-109">Questa proprietà è una **stringa** di lettura/scrittura contenente il nome dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-109">This property is a read/write **String** containing the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f4f4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f4f4-110">Remarks</span></span>

<span data-ttu-id="7f4f4-111">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="7f4f4-112">Per specificare il valore di questa proprietà, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-112">To specify the value of this property, full access to the library is required.</span></span> <span data-ttu-id="7f4f4-113">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7f4f4-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7f4f4-114">Prima di utilizzare questo metodo per specificare il nome di un elemento multimediale, utilizzare **isReadOnlyItem** per determinare se è possibile impostare il nome.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-114">Before using this method to specify the name of a media item, use **isReadOnlyItem** to determine whether the name can be set.</span></span>

<span data-ttu-id="7f4f4-115">**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-115">**Windows Media Player 10 Mobile:** This property is read-only.</span></span>

## <a name="examples"></a><span data-ttu-id="7f4f4-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="7f4f4-116">Examples</span></span>

<span data-ttu-id="7f4f4-117">Nell'esempio JScript seguente viene usato il *supporto*. **nome** per modificare il nome dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-117">The following JScript example uses *Media*.**name** to change the name of the current media item.</span></span> <span data-ttu-id="7f4f4-118">Un elemento input di testo HTML denominato NameText consente all'utente di immettere una stringa di testo per il nuovo nome.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-118">An HTML TEXT input element named NameText allows the user to enter a text string for the new name.</span></span> <span data-ttu-id="7f4f4-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7f4f4-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a><span data-ttu-id="7f4f4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f4f4-120">Requirements</span></span>



| <span data-ttu-id="7f4f4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f4f4-121">Requirement</span></span> | <span data-ttu-id="7f4f4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7f4f4-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4f4-123">Versione</span><span class="sxs-lookup"><span data-stu-id="7f4f4-123">Version</span></span><br/> | <span data-ttu-id="7f4f4-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="7f4f4-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7f4f4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7f4f4-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7f4f4-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f4f4-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f4f4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f4f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4f4-128">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="7f4f4-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7f4f4-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7f4f4-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7f4f4-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7f4f4-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





