---
title: Proprietà FontSize (oggetto Balloon)
description: Informazioni sulla proprietà dell'oggetto FontSize Balloon. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068218"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="ca0de-104">Proprietà FontSize (oggetto Balloon)</span><span class="sxs-lookup"><span data-stu-id="ca0de-104">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="ca0de-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ca0de-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ca0de-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ca0de-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ca0de-107">Restituisce o imposta la dimensione del carattere supportata per il fumetto per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="ca0de-107">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="ca0de-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="ca0de-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ca0de-109">*agent.\*\*\*Caratteri* \*  **("**_CharacterID_*_"). Balloon.FontSize_* \[  =  *Points*\]</span><span class="sxs-lookup"><span data-stu-id="ca0de-109">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="ca0de-110">Parte</span><span class="sxs-lookup"><span data-stu-id="ca0de-110">Part</span></span>     | <span data-ttu-id="ca0de-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca0de-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="ca0de-112">*Punti*</span><span class="sxs-lookup"><span data-stu-id="ca0de-112">*Points*</span></span> | <span data-ttu-id="ca0de-113">Valore Long Integer che specifica la dimensione del carattere in punti.</span><span class="sxs-lookup"><span data-stu-id="ca0de-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca0de-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca0de-114">Remarks</span></span>

<span data-ttu-id="ca0de-115">La [**proprietà FontSize**](fontsize-property.md) restituisce un valore Long Integer che specifica le dimensioni correnti del carattere in punti.</span><span class="sxs-lookup"><span data-stu-id="ca0de-115">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="ca0de-116">Il valore massimo per **FontSize** è 2160 punti.</span><span class="sxs-lookup"><span data-stu-id="ca0de-116">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="ca0de-117">Il valore predefinito per le impostazioni del carattere del fumetto di un carattere viene impostato nell'Editor caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ca0de-117">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="ca0de-118">Inoltre, l'utente può eseguire l'override delle impostazioni dei caratteri per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ca0de-118">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




