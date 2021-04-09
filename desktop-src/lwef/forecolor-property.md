---
title: ForeColor (proprietà)
description: ForeColor (proprietà)
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855633"
---
# <a name="forecolor-property"></a><span data-ttu-id="185a2-103">ForeColor (proprietà)</span><span class="sxs-lookup"><span data-stu-id="185a2-103">ForeColor Property</span></span>

<span data-ttu-id="185a2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="185a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="185a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="185a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="185a2-106">Restituisce il colore di primo piano attualmente visualizzato nella finestra del fumetto di Word per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="185a2-106">Returns the foreground color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="185a2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="185a2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="185a2-108">*agente ***. Caratteri ("*** CharacterID \* \* *"). Balloon. ForeColor**</span><span class="sxs-lookup"><span data-stu-id="185a2-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.ForeColor*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="185a2-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="185a2-109">Remarks</span></span>

<span data-ttu-id="185a2-110">La proprietà **ForeColor** restituisce un valore che specifica il colore del testo nel fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="185a2-110">The **ForeColor** property returns a value that specifies the color of text in the word balloon.</span></span> <span data-ttu-id="185a2-111">L'intervallo valido per un colore RGB normale è compreso tra 0 e 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="185a2-111">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="185a2-112">L'alto byte di un numero in questo intervallo è uguale a 0; i 3 byte inferiori, dal meno significativo al più significativo, determinano rispettivamente la quantità di rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="185a2-112">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="185a2-113">Ognuno dei componenti rosso, verde e blu è rappresentato da un numero compreso tra 0 e 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="185a2-113">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




