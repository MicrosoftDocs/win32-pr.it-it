---
title: Rete. bufferingTime
description: La proprietà bufferingTime specifica o recupera la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima che inizi la riproduzione.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Media Player di Windows Network. bufferingTime
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326111"
---
# <a name="networkbufferingtime"></a><span data-ttu-id="e0558-104">Rete. bufferingTime</span><span class="sxs-lookup"><span data-stu-id="e0558-104">Network.bufferingTime</span></span>

<span data-ttu-id="e0558-105">La proprietà **bufferingTime** specifica o recupera la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima che inizi la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e0558-105">The **bufferingTime** property specifies or retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0558-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0558-106">Syntax</span></span>

<span data-ttu-id="e0558-107">*Player*. *rete*. **bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="e0558-107">*player*.*network*.**bufferingTime**</span></span>

## <a name="possible-values"></a><span data-ttu-id="e0558-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e0558-108">Possible Values</span></span>

<span data-ttu-id="e0558-109">Questa proprietà è un **numero** di lettura/scrittura (**Long**) compreso tra 0 e 60.000 e il valore predefinito è 5.000.</span><span class="sxs-lookup"><span data-stu-id="e0558-109">This property is a read/write **Number** (**long**) ranging from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="e0558-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="e0558-110">Examples</span></span>

<span data-ttu-id="e0558-111">Nell'esempio JScript seguente viene utilizzata la *rete*. **bufferingTime** per specificare il numero di secondi allocati per il buffering dei dati in ingresso.</span><span class="sxs-lookup"><span data-stu-id="e0558-111">The following JScript example uses *Network*.**bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="e0558-112">Le informazioni vengono recuperate da un elemento INPUT di testo HTML creato con ID = "bufText".</span><span class="sxs-lookup"><span data-stu-id="e0558-112">The information is retrieved from an HTML TEXT INPUT element created with ID = "bufText".</span></span> <span data-ttu-id="e0558-113">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e0558-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a><span data-ttu-id="e0558-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0558-114">Requirements</span></span>



| <span data-ttu-id="e0558-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0558-115">Requirement</span></span> | <span data-ttu-id="e0558-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e0558-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0558-117">Versione</span><span class="sxs-lookup"><span data-stu-id="e0558-117">Version</span></span><br/> | <span data-ttu-id="e0558-118">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="e0558-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e0558-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e0558-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="e0558-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0558-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0558-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0558-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0558-122">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="e0558-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





