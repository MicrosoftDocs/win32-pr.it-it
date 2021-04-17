---
title: Proprietà Name (oggetto characters)
description: Proprietà Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474837"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="d5fdc-103">Proprietà Name (oggetto characters)</span><span class="sxs-lookup"><span data-stu-id="d5fdc-103">Name Property (Characters Object)</span></span>

<span data-ttu-id="d5fdc-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d5fdc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d5fdc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d5fdc-106">Restituisce o imposta una stringa che specifica il nome predefinito del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-106">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="d5fdc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="d5fdc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d5fdc-108">\*agente \***. Caratteri ("**_CharacterID_\*_")._ \*  \[  =  *Stringa* nome\]</span><span class="sxs-lookup"><span data-stu-id="d5fdc-108">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="d5fdc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d5fdc-109">Part</span></span>     | <span data-ttu-id="d5fdc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5fdc-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fdc-111">*string*</span><span class="sxs-lookup"><span data-stu-id="d5fdc-111">*string*</span></span> | <span data-ttu-id="d5fdc-112">Valore stringa corrispondente al nome del carattere (nell'impostazione della lingua corrente).</span><span class="sxs-lookup"><span data-stu-id="d5fdc-112">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5fdc-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5fdc-113">Remarks</span></span>

<span data-ttu-id="d5fdc-114">Il **nome** di un carattere può dipendere dall'impostazione [**LanguageID**](languageid-property.md) del carattere.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-114">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="d5fdc-115">Il nome di un carattere in una lingua può essere diverso o usare caratteri diversi rispetto a un altro.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="d5fdc-116">Il **nome** predefinito del carattere per una lingua specifica viene definito quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-116">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="d5fdc-117">Evitare di rinominare un carattere, soprattutto quando viene usato in uno scenario in cui altre applicazioni client possono usare lo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-117">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="d5fdc-118">Inoltre, Agent usa il **nome** del carattere per creare automaticamente i comandi per nascondere e visualizzare il carattere.</span><span class="sxs-lookup"><span data-stu-id="d5fdc-118">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




