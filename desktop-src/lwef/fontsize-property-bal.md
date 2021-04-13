---
title: Proprietà FontSize (oggetto Balloon)
description: Proprietà FontSize
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569c07e98fb8bf973a554e89655f71e816b4a51b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400156"
---
# <a name="fontsize-property-balloon-object"></a><span data-ttu-id="18193-103">Proprietà FontSize (oggetto Balloon)</span><span class="sxs-lookup"><span data-stu-id="18193-103">FontSize Property (Balloon Object)</span></span>

<span data-ttu-id="18193-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="18193-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="18193-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="18193-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="18193-106">Restituisce o imposta la dimensione del carattere supportata per la parola Balloon per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="18193-106">Returns or sets the font size supported for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="18193-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="18193-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="18193-108">*Agent. \* \* \* caratteri* \*  **("**_CharacterID_*_"). Punti di Balloon. FontSize_* \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="18193-108">*agent.\*\*\*Characters*\* **("**_CharacterID_*_").Balloon.FontSize_* \[ = *Points*\]</span></span>



| <span data-ttu-id="18193-109">Parte</span><span class="sxs-lookup"><span data-stu-id="18193-109">Part</span></span>     | <span data-ttu-id="18193-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18193-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="18193-111">*Punti*</span><span class="sxs-lookup"><span data-stu-id="18193-111">*Points*</span></span> | <span data-ttu-id="18193-112">Valore long integer che specifica la dimensione del carattere in punti.</span><span class="sxs-lookup"><span data-stu-id="18193-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18193-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="18193-113">Remarks</span></span>

<span data-ttu-id="18193-114">La proprietà [**FontSize**](fontsize-property.md) restituisce un valore long integer che specifica la dimensione corrente del carattere in punti.</span><span class="sxs-lookup"><span data-stu-id="18193-114">The [**FontSize**](fontsize-property.md) property returns a Long integer value specifying the current font size in points.</span></span> <span data-ttu-id="18193-115">Il valore massimo per **FontSize** è 2160 punti.</span><span class="sxs-lookup"><span data-stu-id="18193-115">The maximum value for **FontSize** is 2160 points.</span></span>

<span data-ttu-id="18193-116">Il valore predefinito per le impostazioni del tipo di carattere del fumetto di parole di un carattere viene impostato nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="18193-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="18193-117">Inoltre, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="18193-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

 

 




