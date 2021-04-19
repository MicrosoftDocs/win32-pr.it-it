---
title: Proprietà FontSize (oggetto Commands)
description: Proprietà FontSize
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300848"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="28182-103">Proprietà FontSize (oggetto Commands)</span><span class="sxs-lookup"><span data-stu-id="28182-103">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="28182-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28182-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="28182-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="28182-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="28182-106">Restituisce o imposta la dimensione del carattere utilizzata nel menu popup del carattere.</span><span class="sxs-lookup"><span data-stu-id="28182-106">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="28182-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="28182-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="28182-108">\*Agent. \***Characters ("**_CharacterID_\*_"). Punti Commands. FontSize_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="28182-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="28182-109">Parte</span><span class="sxs-lookup"><span data-stu-id="28182-109">Part</span></span>     | <span data-ttu-id="28182-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28182-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="28182-111">*Punti*</span><span class="sxs-lookup"><span data-stu-id="28182-111">*Points*</span></span> | <span data-ttu-id="28182-112">Valore long integer che specifica la dimensione del carattere in punti.</span><span class="sxs-lookup"><span data-stu-id="28182-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28182-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="28182-113">Remarks</span></span>

<span data-ttu-id="28182-114">La proprietà **FontSize** definisce la dimensione in punti del tipo di carattere utilizzato per visualizzare il testo nel menu popup del carattere.</span><span class="sxs-lookup"><span data-stu-id="28182-114">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="28182-115">Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione **LanguageID** del carattere oppure, se non è impostato, l'impostazione della lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="28182-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="28182-116">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="28182-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




