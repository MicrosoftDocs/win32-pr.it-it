---
title: MoveTo (metodo)
description: MoveTo (metodo)
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046745"
---
# <a name="moveto-method"></a><span data-ttu-id="f16e2-103">MoveTo (metodo)</span><span class="sxs-lookup"><span data-stu-id="f16e2-103">MoveTo Method</span></span>

<span data-ttu-id="f16e2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f16e2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f16e2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f16e2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f16e2-106">Sposta il carattere specificato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="f16e2-106">Moves the specified character to the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="f16e2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="f16e2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f16e2-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). MoveTo* \*  *x, y* \[ *velocità*\]</span><span class="sxs-lookup"><span data-stu-id="f16e2-108">*agent ***.Characters ("*** CharacterID\*\*\*").MoveTo*\* *x,y*\[*Speed*\]</span></span>



| <span data-ttu-id="f16e2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f16e2-109">Part</span></span>    | <span data-ttu-id="f16e2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f16e2-110">Description</span></span>                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16e2-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="f16e2-111">*x,y*</span></span>   | <span data-ttu-id="f16e2-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f16e2-112">Required.</span></span> <span data-ttu-id="f16e2-113">Valore intero che indica il bordo sinistro (*x*) e il bordo superiore (*y*) del frame di animazione.</span><span class="sxs-lookup"><span data-stu-id="f16e2-113">An integer value that indicates the left edge (*x*) and top edge (*y*) of the animation frame.</span></span> <span data-ttu-id="f16e2-114">Esprimere queste coordinate in pixel.</span><span class="sxs-lookup"><span data-stu-id="f16e2-114">Express these coordinates in pixels.</span></span>                                                   |
| <span data-ttu-id="f16e2-115">*Velocità*</span><span class="sxs-lookup"><span data-stu-id="f16e2-115">*Speed*</span></span> | <span data-ttu-id="f16e2-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f16e2-116">Optional.</span></span> <span data-ttu-id="f16e2-117">Valore long integer che specifica in millisecondi la velocità con cui il frame del carattere viene spostato.</span><span class="sxs-lookup"><span data-stu-id="f16e2-117">A Long integer value specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="f16e2-118">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="f16e2-118">The default value is 1000.</span></span> <span data-ttu-id="f16e2-119">Se si specifica zero (0), il frame viene spostato senza riprodurre un'animazione.</span><span class="sxs-lookup"><span data-stu-id="f16e2-119">Specifying zero (0) moves the frame without playing an animation.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f16e2-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f16e2-120">Remarks</span></span>

<span data-ttu-id="f16e2-121">Il server esegue automaticamente l'animazione appropriata assegnata agli Stati di **trasferimento** .</span><span class="sxs-lookup"><span data-stu-id="f16e2-121">The server automatically plays the appropriate animation assigned to the **Moving** states.</span></span> <span data-ttu-id="f16e2-122">La posizione di un carattere è basata sull'angolo superiore sinistro del frame.</span><span class="sxs-lookup"><span data-stu-id="f16e2-122">The location of a character is based on the upper left corner of its frame.</span></span>

<span data-ttu-id="f16e2-123">Se si dichiara una variabile oggetto e la si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="f16e2-123">If you declare an object variable and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="f16e2-124">Inoltre, se l'animazione associata non è stata caricata nel computer locale, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **richiesta** su "failed" con un numero di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="f16e2-124">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="f16e2-125">Se pertanto si utilizza il protocollo HTTP per accedere ai dati di tipo carattere o di animazione, utilizzare il metodo [**Get**](get-method.md) per caricare le animazioni dello stato di **trasferimento** prima di chiamare il metodo **MoveTo** .</span><span class="sxs-lookup"><span data-stu-id="f16e2-125">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method to load the **Moving** state animations before calling the **MoveTo** method.</span></span>

<span data-ttu-id="f16e2-126">Anche se l'animazione non è caricata, il server sposta ancora il frame.</span><span class="sxs-lookup"><span data-stu-id="f16e2-126">Even if the animation is not loaded, the server still moves the frame.</span></span>

> [!Note]  
> <span data-ttu-id="f16e2-127">Se si chiama **MoveTo** con un valore diverso da zero prima che il carattere venga visualizzato, viene restituito uno stato di errore se è stato assegnato un oggetto [**Request**](/windows/desktop/lwef/the-request-object) , perché il valore diverso da zero indica che si sta provando a riprodurre un'animazione quando il carattere non è visibile.</span><span class="sxs-lookup"><span data-stu-id="f16e2-127">If you call **MoveTo** with a nonzero value before the character is shown, it will return a failure status if you assigned it a [**Request**](/windows/desktop/lwef/the-request-object) object, because the nonzero value indicates that you are attempting to play an animation when the character is not visible.</span></span>

 

> [!Note]  
> <span data-ttu-id="f16e2-128">L'effetto effettivo del parametro *Speed* può variare in base alla velocità del processore del computer e alla priorità di altre attività in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="f16e2-128">The *Speed* parameter's actual effect may vary based on the speed of the processor of the computer and the priority of other tasks running on the system.</span></span>

 

 

 