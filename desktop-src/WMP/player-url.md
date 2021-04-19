---
title: Player. URL
description: La proprietà URL specifica o Recupera il nome dell'elemento multimediale da riprodurre.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player. URL Windows Media Player
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327061"
---
# <a name="playerurl"></a><span data-ttu-id="047d8-104">Player. URL</span><span class="sxs-lookup"><span data-stu-id="047d8-104">Player.URL</span></span>

<span data-ttu-id="047d8-105">La proprietà **URL** specifica o Recupera il nome dell'elemento multimediale da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="047d8-105">The **URL** property specifies or retrieves the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="047d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="047d8-106">Syntax</span></span>

<span data-ttu-id="047d8-107">*Player* . **URL** di</span><span class="sxs-lookup"><span data-stu-id="047d8-107">*player* .**URL**</span></span>

## <a name="possible-values"></a><span data-ttu-id="047d8-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="047d8-108">Possible Values</span></span>

<span data-ttu-id="047d8-109">Questa proprietà è una **stringa** di lettura/scrittura senza valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="047d8-109">This property is a read/write **String** with no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="047d8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="047d8-110">Remarks</span></span>

<span data-ttu-id="047d8-111">Questa proprietà può essere impostata solo su un URL in un'area di sicurezza uguale o meno restrittiva rispetto all'area di sicurezza del programma chiamante o della pagina Web.</span><span class="sxs-lookup"><span data-stu-id="047d8-111">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="047d8-112">Le applicazioni che aprono elementi multimediali da dietro un firewall avranno prestazioni migliori se l'indirizzo viene specificato usando il nome del Domain Name Server (DNS) invece dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="047d8-112">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="047d8-113">Non chiamare questo metodo dal codice del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="047d8-113">Do not call this method from event handler code.</span></span> <span data-ttu-id="047d8-114">Chiamata del *lettore*. L' **URL** di un gestore eventi può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="047d8-114">Calling *Player*.**URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="047d8-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="047d8-115">Examples</span></span>

<span data-ttu-id="047d8-116">Nell'esempio seguente vengono creati un elemento input di testo HTML e un elemento input BUTTON HTML.</span><span class="sxs-lookup"><span data-stu-id="047d8-116">The following example creates an HTML TEXT input element and an HTML BUTTON input element.</span></span> <span data-ttu-id="047d8-117">L'elemento di testo consente all'utente di digitare un percorso per specificare un file multimediale digitale da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="047d8-117">The TEXT element allows the user to type a path to specify a digital media file to play.</span></span> <span data-ttu-id="047d8-118">L'elemento BUTTON esegue JScript che apre il file e avvia Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="047d8-118">The BUTTON element executes JScript that opens the file and starts Windows Media Player.</span></span> <span data-ttu-id="047d8-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="047d8-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="047d8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="047d8-120">Requirements</span></span>



| <span data-ttu-id="047d8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="047d8-121">Requirement</span></span> | <span data-ttu-id="047d8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="047d8-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="047d8-123">Versione</span><span class="sxs-lookup"><span data-stu-id="047d8-123">Version</span></span><br/> | <span data-ttu-id="047d8-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="047d8-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="047d8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="047d8-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="047d8-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="047d8-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047d8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="047d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047d8-128">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="047d8-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





