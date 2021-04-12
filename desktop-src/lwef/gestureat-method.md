---
title: Metodo GestureAt
description: Metodo GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472803"
---
# <a name="gestureat-method"></a><span data-ttu-id="c43b2-103">Metodo GestureAt</span><span class="sxs-lookup"><span data-stu-id="c43b2-103">GestureAt Method</span></span>

<span data-ttu-id="c43b2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c43b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c43b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c43b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c43b2-106">Riproduce l'animazione gestuale per il carattere specificato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c43b2-106">Plays the gesturing animation for the specified character at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="c43b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="c43b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c43b2-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). GestureAt* \*  *x, y*</span><span class="sxs-lookup"><span data-stu-id="c43b2-108">*agent ***.Characters ("*** CharacterID\*\*\*").GestureAt*\* *x,y*</span></span>



| <span data-ttu-id="c43b2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c43b2-109">Part</span></span>  | <span data-ttu-id="c43b2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c43b2-110">Description</span></span>                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c43b2-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="c43b2-111">*x,y*</span></span> | <span data-ttu-id="c43b2-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c43b2-112">Required.</span></span> <span data-ttu-id="c43b2-113">Valore intero che indica la coordinata orizzontale (*x*) dello schermo e la coordinata verticale (*y*) dello schermo a cui il carattere gestirà.</span><span class="sxs-lookup"><span data-stu-id="c43b2-113">An integer value that indicates the horizontal (*x*) screen coordinate and vertical (*y*) screen coordinate to which the character will gesture.</span></span> <span data-ttu-id="c43b2-114">È necessario specificare queste coordinate in pixel.</span><span class="sxs-lookup"><span data-stu-id="c43b2-114">These coordinates must be specified in pixels.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c43b2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c43b2-115">Remarks</span></span>

<span data-ttu-id="c43b2-116">Il server esegue automaticamente l'animazione appropriata per eseguire un movimento verso la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c43b2-116">The server automatically plays the appropriate animation to gesture toward the specified location.</span></span> <span data-ttu-id="c43b2-117">Le coordinate sono sempre relative all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="c43b2-117">The coordinates are always relative to the screen origin (upper left).</span></span>

<span data-ttu-id="c43b2-118">Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="c43b2-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="c43b2-119">Inoltre, se l'animazione associata non è stata caricata nel computer locale, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **richiesta** su "failed" con un numero di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="c43b2-119">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="c43b2-120">Se pertanto si utilizza il protocollo HTTP per accedere ai dati di animazione di tipo carattere, utilizzare il metodo [**Get**](get-method.md) per caricare le animazioni dello stato **gestuale** prima di chiamare il metodo **GestureAt** .</span><span class="sxs-lookup"><span data-stu-id="c43b2-120">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Gesturing** state animations before calling the **GestureAt** method.</span></span>

 

 