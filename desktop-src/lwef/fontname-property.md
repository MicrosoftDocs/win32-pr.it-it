---
title: Proprietà FontName (oggetto Commands)
description: Informazioni sulla proprietà dell'oggetto Comandi FontName. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068257"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="95261-104">Proprietà FontName (oggetto Commands)</span><span class="sxs-lookup"><span data-stu-id="95261-104">FontName Property (Commands Object)</span></span>

<span data-ttu-id="95261-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="95261-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="95261-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="95261-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="95261-107">Restituisce o imposta il tipo di carattere utilizzato nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="95261-107">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="95261-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="95261-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="95261-109">*agent.\***Characters("**_CharacterID_*_"). Tipo di carattere Commands.FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="95261-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="95261-110">Parte</span><span class="sxs-lookup"><span data-stu-id="95261-110">Part</span></span>   | <span data-ttu-id="95261-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95261-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="95261-112">*Carattere*</span><span class="sxs-lookup"><span data-stu-id="95261-112">*Font*</span></span> | <span data-ttu-id="95261-113">Valore stringa corrispondente al nome del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="95261-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95261-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="95261-114">Remarks</span></span>

<span data-ttu-id="95261-115">La **proprietà FontName** definisce il tipo di carattere usato per visualizzare il testo nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="95261-115">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="95261-116">Il valore predefinito per l'impostazione del tipo di carattere si basa sull'impostazione del tipo di carattere del menu per l'impostazione **LanguageID** del carattere oppure, se non è impostata, sull'impostazione dell'ID lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="95261-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="95261-117">Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="95261-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




