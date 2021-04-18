---
title: Player. versionInfo
description: La proprietà versionInfo recupera un valore stringa che specifica la versione di Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player. versionInfo Windows Media Player
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327056"
---
# <a name="playerversioninfo"></a><span data-ttu-id="6eceb-104">Player. versionInfo</span><span class="sxs-lookup"><span data-stu-id="6eceb-104">Player.versionInfo</span></span>

<span data-ttu-id="6eceb-105">La proprietà **VERSIONINFO** recupera un valore stringa che specifica la versione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6eceb-105">The **versionInfo** property retrieves a String value specifying the version of the Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eceb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6eceb-106">Syntax</span></span>

<span data-ttu-id="6eceb-107">*Player* . **VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="6eceb-107">*player* .**versionInfo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="6eceb-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="6eceb-108">Possible Values</span></span>

<span data-ttu-id="6eceb-109">Questa proprietà è una **stringa** di sola lettura nel formato seguente: "*X*. 0,0. *Aaaa*"dove *X* rappresenta il numero di versione principale e *aaaa* rappresenta il numero di Build.</span><span class="sxs-lookup"><span data-stu-id="6eceb-109">This property is a read-only **String** in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="6eceb-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="6eceb-110">Examples</span></span>

<span data-ttu-id="6eceb-111">Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando selezionato, Visualizza una finestra di messaggio contenente le informazioni sulla versione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6eceb-111">The following example creates an HTML BUTTON element that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="6eceb-112">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6eceb-112">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a><span data-ttu-id="6eceb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6eceb-113">Requirements</span></span>



| <span data-ttu-id="6eceb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eceb-114">Requirement</span></span> | <span data-ttu-id="6eceb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6eceb-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6eceb-116">Versione</span><span class="sxs-lookup"><span data-stu-id="6eceb-116">Version</span></span><br/> | <span data-ttu-id="6eceb-117">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="6eceb-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6eceb-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6eceb-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="6eceb-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6eceb-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eceb-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6eceb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eceb-121">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="6eceb-121">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





