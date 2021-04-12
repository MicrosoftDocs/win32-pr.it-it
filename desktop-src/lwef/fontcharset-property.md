---
title: Proprietà FontCharSet
description: Proprietà FontCharSet
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331951"
---
# <a name="fontcharset-property"></a><span data-ttu-id="173fe-103">Proprietà FontCharSet</span><span class="sxs-lookup"><span data-stu-id="173fe-103">FontCharSet Property</span></span>

<span data-ttu-id="173fe-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="173fe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="173fe-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="173fe-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="173fe-106">Restituisce o imposta il set di caratteri per il tipo di carattere visualizzato nell'aerostato di parola del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="173fe-106">Returns or sets the character set for the font displayed in the specified character's word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="173fe-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="173fe-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="173fe-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). Valore di Balloon. FontCharSet* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="173fe-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.FontCharSet*\* \[ = *value*\]</span></span>



| <span data-ttu-id="173fe-109">Parte</span><span class="sxs-lookup"><span data-stu-id="173fe-109">Part</span></span>    | <span data-ttu-id="173fe-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="173fe-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="173fe-111">*value*</span><span class="sxs-lookup"><span data-stu-id="173fe-111">*value*</span></span> | <span data-ttu-id="173fe-112">Valore intero che specifica il set di caratteri utilizzato dal tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="173fe-112">An integer value that specifies the character set used by the font.</span></span> <span data-ttu-id="173fe-113">Di seguito sono riportate alcune impostazioni comuni per valore: 0 caratteri Windows standard (ANSI).</span><span class="sxs-lookup"><span data-stu-id="173fe-113">The following are some common settings for value: 0 Standard Windows characters (ANSI).</span></span><br/> <span data-ttu-id="173fe-114">1 set di caratteri predefinito.</span><span class="sxs-lookup"><span data-stu-id="173fe-114">1 Default character set.</span></span><br/> <span data-ttu-id="173fe-115">2 il set di caratteri del simbolo.</span><span class="sxs-lookup"><span data-stu-id="173fe-115">2 The symbol character set.</span></span><br/> <span data-ttu-id="173fe-116">128 DBCS (Double byte character set) univoco per la versione giapponese di Windows.</span><span class="sxs-lookup"><span data-stu-id="173fe-116">128 Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span><br/> <span data-ttu-id="173fe-117">129 DBCS (Double byte character set) univoco per la versione coreana di Windows.</span><span class="sxs-lookup"><span data-stu-id="173fe-117">129 Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span><br/> <span data-ttu-id="173fe-118">134 DBCS (Double byte character set) univoco per la versione in cinese semplificato di Windows.</span><span class="sxs-lookup"><span data-stu-id="173fe-118">134 Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span><br/> <span data-ttu-id="173fe-119">136 DBCS (Double byte character set) univoco per la versione cinese tradizionale di Windows.</span><span class="sxs-lookup"><span data-stu-id="173fe-119">136 Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span><br/> <span data-ttu-id="173fe-120">255 caratteri estesi normalmente visualizzati dalle applicazioni Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="173fe-120">255 Extended characters normally displayed by Microsoft MS-DOS applications.</span></span><br/> <span data-ttu-id="173fe-121">Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="173fe-121">For other character set values, consult the Platform SDK documentation.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="173fe-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="173fe-122">Remarks</span></span>

<span data-ttu-id="173fe-123">Il valore predefinito per il set di caratteri del fumetto di parole di un carattere viene impostato nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="173fe-123">The default value for the character set of a character's word balloon is set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="173fe-124">Inoltre, l'utente può eseguire l'override delle impostazioni del set di caratteri per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="173fe-124">In addition, the user can override the character-set settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="173fe-125">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="173fe-125">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="173fe-126">Se si usa un carattere non compilato, controllare le proprietà [**fontname**](fontname-property.md) e **FontCharSet** per il carattere per determinare se sono appropriate per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="173fe-126">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and **FontCharSet** properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="173fe-127">Potrebbe essere necessario impostare questi valori prima di utilizzare il metodo [**Speak**](speak-method.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="173fe-127">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="173fe-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="173fe-128">See Also</span></span>

[<span data-ttu-id="173fe-129">**Fontname (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="173fe-129">**FontName property**</span></span>](fontname-property.md)


 

 





