---
title: Proprietà BackColor (funzionalità dell'ambiente Windows legacy)
description: BackColor (proprietà)
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739655"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a><span data-ttu-id="38cb6-103">Proprietà BackColor (funzionalità dell'ambiente Windows legacy)</span><span class="sxs-lookup"><span data-stu-id="38cb6-103">BackColor Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="38cb6-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38cb6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="38cb6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="38cb6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="38cb6-106">Restituisce il colore di sfondo attualmente visualizzato nella finestra del fumetto di Word per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="38cb6-106">Returns the background color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="38cb6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="38cb6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="38cb6-108">\*agente \***. Caratteri ("**_CharacterID_*_"). Balloon. BackColor_*</span><span class="sxs-lookup"><span data-stu-id="38cb6-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.BackColor_\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38cb6-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="38cb6-109">Remarks</span></span>

<span data-ttu-id="38cb6-110">L'intervallo valido per un colore RGB normale è compreso tra 0 e 16.777.215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="38cb6-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="38cb6-111">L'alto byte di un numero in questo intervallo è uguale a 0; i 3 byte inferiori, dal meno significativo al più significativo, determinano rispettivamente la quantità di rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="38cb6-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="38cb6-112">Ognuno dei componenti rosso, verde e blu è rappresentato da un numero compreso tra 0 e 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="38cb6-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 




