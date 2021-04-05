---
title: Proprietà Height (oggetto characters)
description: Height (proprietà)
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739322"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="ef7e0-103">Proprietà Height (oggetto characters)</span><span class="sxs-lookup"><span data-stu-id="ef7e0-103">Height Property (Characters Object)</span></span>

<span data-ttu-id="ef7e0-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef7e0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ef7e0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ef7e0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ef7e0-106">Restituisce o imposta l'altezza del frame del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="ef7e0-106">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="ef7e0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="ef7e0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ef7e0-108">\*agente \***. Caratteri ("**_CharacterID_\*_")._ \*  \[ =  *Valore* altezza\]</span><span class="sxs-lookup"><span data-stu-id="ef7e0-108">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="ef7e0-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ef7e0-109">Part</span></span>    | <span data-ttu-id="ef7e0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef7e0-110">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="ef7e0-111">*value*</span><span class="sxs-lookup"><span data-stu-id="ef7e0-111">*value*</span></span> | <span data-ttu-id="ef7e0-112">Valore long integer che specifica l'altezza del frame del carattere.</span><span class="sxs-lookup"><span data-stu-id="ef7e0-112">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef7e0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef7e0-113">Remarks</span></span>

<span data-ttu-id="ef7e0-114">La proprietà **Height** è sempre espressa in pixel, rispetto alle coordinate dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="ef7e0-114">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="ef7e0-115">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="ef7e0-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="ef7e0-116">Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, l'altezza del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ef7e0-116">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




