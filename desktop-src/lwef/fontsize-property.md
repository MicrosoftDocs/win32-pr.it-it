---
title: Proprietà FontSize (oggetto Commands)
description: Informazioni sulla proprietà dell'oggetto Comandi FontSize. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068208"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="70780-104">Proprietà FontSize (oggetto Commands)</span><span class="sxs-lookup"><span data-stu-id="70780-104">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="70780-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70780-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="70780-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="70780-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="70780-107">Restituisce o imposta la dimensione del carattere utilizzata nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="70780-107">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="70780-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="70780-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="70780-109">*agent.\***Characters("**_CharacterID_*_"). Commands.FontSize_ \*  \[  =  *Points*\]</span><span class="sxs-lookup"><span data-stu-id="70780-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="70780-110">Parte</span><span class="sxs-lookup"><span data-stu-id="70780-110">Part</span></span>     | <span data-ttu-id="70780-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70780-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="70780-112">*Punti*</span><span class="sxs-lookup"><span data-stu-id="70780-112">*Points*</span></span> | <span data-ttu-id="70780-113">Valore Long Integer che specifica la dimensione del carattere in punti.</span><span class="sxs-lookup"><span data-stu-id="70780-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70780-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="70780-114">Remarks</span></span>

<span data-ttu-id="70780-115">La **proprietà FontSize** definisce le dimensioni in punti del tipo di carattere usato per visualizzare il testo nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="70780-115">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="70780-116">Il valore predefinito per l'impostazione del tipo di carattere si basa sull'impostazione del tipo di carattere del menu per l'impostazione **LanguageID** del carattere o, se non è impostata, sull'impostazione della lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="70780-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="70780-117">Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="70780-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




