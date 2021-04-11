---
description: Questo attributo aggiunge l'icona di elevazione (UAC) del controllo dell'account utente (icona scudo) al controllo pulsante.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Attributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131790"
---
# <a name="elevationshield-attribute"></a><span data-ttu-id="b15b8-103">Attributo ElevationShield</span><span class="sxs-lookup"><span data-stu-id="b15b8-103">ElevationShield Attribute</span></span>

<span data-ttu-id="b15b8-104">Questo attributo aggiunge l'icona di elevazione (UAC) del [*controllo dell'account utente*](u-gly.md) (icona scudo) al [controllo pulsante](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="b15b8-104">This attribute adds the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon) to the [PushButton control](pushbutton-control.md).</span></span>

<span data-ttu-id="b15b8-105">Se questo bit è impostato e l'installazione non è ancora in esecuzione con privilegi [*elevati*](e-gly.md) , il controllo pulsante viene creato usando l'icona di elevazione del [*controllo dell'account utente*](u-gly.md) (UAC).</span><span class="sxs-lookup"><span data-stu-id="b15b8-105">If this bit is set, and the installation is not yet running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon).</span></span>

<span data-ttu-id="b15b8-106">Se questo bit è impostato e l'installazione è già in esecuzione con privilegi [*elevati*](e-gly.md) , il controllo pulsante viene creato usando gli altri attributi dell'icona.</span><span class="sxs-lookup"><span data-stu-id="b15b8-106">If this bit is set, and the installation is already running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the other icon attributes.</span></span>

<span data-ttu-id="b15b8-107">Se questo bit non è impostato, il controllo pulsante viene creato usando gli altri attributi dell'icona.</span><span class="sxs-lookup"><span data-stu-id="b15b8-107">If this bit is not set, the pushbutton control is created using the other icon attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b15b8-108">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="b15b8-108">Valid Controls</span></span>

[<span data-ttu-id="b15b8-109">Pulsante</span><span class="sxs-lookup"><span data-stu-id="b15b8-109">PushButton</span></span>](pushbutton-control.md)

## <a name="value"></a><span data-ttu-id="b15b8-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b15b8-110">Value</span></span>



| <span data-ttu-id="b15b8-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="b15b8-111">Decimal</span></span> | <span data-ttu-id="b15b8-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b15b8-112">Hexadecimal</span></span> | <span data-ttu-id="b15b8-113">Costante</span><span class="sxs-lookup"><span data-stu-id="b15b8-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="b15b8-114">8388608</span><span class="sxs-lookup"><span data-stu-id="b15b8-114">8388608</span></span> | <span data-ttu-id="b15b8-115">0x00800000</span><span class="sxs-lookup"><span data-stu-id="b15b8-115">0x00800000</span></span>  | <span data-ttu-id="b15b8-116">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="b15b8-116">**msidbControlAttributesElevationShield**</span></span> |



 

 

 



