---
title: Proprietà Left (oggetto Characters)
description: Informazioni sulla proprietà dell'oggetto Left Characters. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988937"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="0a531-104">Proprietà Left (oggetto Characters)</span><span class="sxs-lookup"><span data-stu-id="0a531-104">Left Property (Characters Object)</span></span>

<span data-ttu-id="0a531-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a531-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0a531-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0a531-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0a531-107">Restituisce o imposta il bordo sinistro della cornice del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="0a531-107">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="0a531-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="0a531-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0a531-109">*agent\***. Caratteri ("**_CharacterID_*_"). Valore_ \*  \[  =  *a sinistra*\]</span><span class="sxs-lookup"><span data-stu-id="0a531-109">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="0a531-110">Parte</span><span class="sxs-lookup"><span data-stu-id="0a531-110">Part</span></span>    | <span data-ttu-id="0a531-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a531-111">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="0a531-112">*value*</span><span class="sxs-lookup"><span data-stu-id="0a531-112">*value*</span></span> | <span data-ttu-id="0a531-113">Valore Long integer che specifica il bordo sinistro della cornice del carattere.</span><span class="sxs-lookup"><span data-stu-id="0a531-113">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a531-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a531-114">Remarks</span></span>

<span data-ttu-id="0a531-115">La **proprietà Left** è sempre espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="0a531-115">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="0a531-116">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="0a531-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="0a531-117">Anche se il carattere viene visualizzato in una finestra di area irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con Microsoft Agent Character Editor.</span><span class="sxs-lookup"><span data-stu-id="0a531-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




