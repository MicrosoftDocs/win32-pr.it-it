---
title: BorderColor (proprietà)
description: BorderColor (proprietà)
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981d3ac280669f64219961b74d05c6ba73f1008
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471206"
---
# <a name="bordercolor-property"></a><span data-ttu-id="b405d-103">BorderColor (proprietà)</span><span class="sxs-lookup"><span data-stu-id="b405d-103">BorderColor Property</span></span>

<span data-ttu-id="b405d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b405d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b405d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b405d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b405d-106">Restituisce il colore del bordo attualmente visualizzato per la finestra del fumetto di Word per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="b405d-106">Returns the border color currently displayed for the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="b405d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="b405d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b405d-108">\* Agent ***. Caratteri ("*** CharacterID \***").** Balloon. BorderColor</span><span class="sxs-lookup"><span data-stu-id="b405d-108">*agent ***.Characters ("*** CharacterID\*\*\*").*\* Balloon.BorderColor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b405d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b405d-109">Remarks</span></span>

<span data-ttu-id="b405d-110">L'intervallo valido per un colore RGB normale è compreso tra 0 e 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="b405d-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="b405d-111">L'alto byte di un numero in questo intervallo è uguale a 0; i 3 byte inferiori, dal meno significativo al più significativo, determinano rispettivamente la quantità di rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="b405d-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="b405d-112">Ognuno dei componenti rosso, verde e blu è rappresentato da un numero compreso tra 0 e 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="b405d-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




