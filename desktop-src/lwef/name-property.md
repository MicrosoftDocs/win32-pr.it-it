---
title: Proprietà Name (oggetto Characters)
description: Informazioni sulla proprietà Name dell'oggetto Characters. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989326"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="a87ff-104">Proprietà Name (oggetto Characters)</span><span class="sxs-lookup"><span data-stu-id="a87ff-104">Name Property (Characters Object)</span></span>

<span data-ttu-id="a87ff-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a87ff-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a87ff-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a87ff-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a87ff-107">Restituisce o imposta una stringa che specifica il nome predefinito del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="a87ff-107">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a87ff-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a87ff-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a87ff-109">*agent\***. Caratteri ("**_CharacterID_*_"). Stringa del_ \*  \[  =  *nome*\]</span><span class="sxs-lookup"><span data-stu-id="a87ff-109">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="a87ff-110">Parte</span><span class="sxs-lookup"><span data-stu-id="a87ff-110">Part</span></span>     | <span data-ttu-id="a87ff-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a87ff-111">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a87ff-112">*string*</span><span class="sxs-lookup"><span data-stu-id="a87ff-112">*string*</span></span> | <span data-ttu-id="a87ff-113">Valore stringa corrispondente al nome del carattere (nell'impostazione della lingua corrente).</span><span class="sxs-lookup"><span data-stu-id="a87ff-113">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a87ff-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a87ff-114">Remarks</span></span>

<span data-ttu-id="a87ff-115">Il nome di un **carattere** può dipendere dall'impostazione [**LanguageID del**](languageid-property.md) carattere.</span><span class="sxs-lookup"><span data-stu-id="a87ff-115">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="a87ff-116">Il nome di un carattere in una lingua può essere diverso o usare caratteri diversi rispetto a in un'altra.</span><span class="sxs-lookup"><span data-stu-id="a87ff-116">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="a87ff-117">Il nome predefinito **del** carattere per una lingua specifica viene definito quando il carattere viene compilato con Microsoft Agent Character Editor.</span><span class="sxs-lookup"><span data-stu-id="a87ff-117">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="a87ff-118">Evitare di rinominare un carattere, soprattutto quando lo si usa in uno scenario in cui altre applicazioni client possono usare lo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="a87ff-118">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="a87ff-119">Agent usa anche il nome del **carattere** per creare automaticamente i comandi per nascondere e visualizzare il carattere.</span><span class="sxs-lookup"><span data-stu-id="a87ff-119">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




