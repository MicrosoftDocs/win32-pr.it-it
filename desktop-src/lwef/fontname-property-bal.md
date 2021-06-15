---
title: Proprietà FontName (oggetto Balloon)
description: Informazioni sulla proprietà dell'oggetto Balloon FontName. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47e14935f913ce81b5faed5a49c3d731a73532f
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068267"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="a5d1b-104">Proprietà FontName (oggetto Balloon)</span><span class="sxs-lookup"><span data-stu-id="a5d1b-104">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="a5d1b-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a5d1b-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a5d1b-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a5d1b-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a5d1b-107">Restituisce o imposta il tipo di carattere utilizzato nel fumetto della parola per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-107">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a5d1b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a5d1b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a5d1b-109">*agent.\***Characters("**_CharacterID_*_"). Tipo di carattere Balloon.FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="a5d1b-109">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="a5d1b-110">Parte</span><span class="sxs-lookup"><span data-stu-id="a5d1b-110">Part</span></span>   | <span data-ttu-id="a5d1b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5d1b-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="a5d1b-112">*Carattere*</span><span class="sxs-lookup"><span data-stu-id="a5d1b-112">*font*</span></span> | <span data-ttu-id="a5d1b-113">Valore stringa corrispondente al nome del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5d1b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5d1b-114">Remarks</span></span>

<span data-ttu-id="a5d1b-115">La [**proprietà FontName**](fontname-property.md) definisce il tipo di carattere usato per visualizzare il testo nella finestra del fumetto di una stringa.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-115">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="a5d1b-116">Il valore predefinito per le impostazioni del carattere del fumetto di un carattere viene impostato nell'editor di caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a5d1b-117">Inoltre, l'utente può eseguire l'override delle impostazioni dei caratteri per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="a5d1b-118">Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="a5d1b-119">Se si usa un carattere che non è stato compilato, controllare le proprietà [**FontName**](fontname-property.md) e [**FontCharSet**](fontcharset-property.md) per il carattere per determinare se sono appropriate per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-119">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="a5d1b-120">Potrebbe essere necessario impostare questi valori prima di usare il [**metodo Speak**](speak-method.md) per garantire la visualizzazione del testo appropriato all'interno del fumetto della parola.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-120">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




