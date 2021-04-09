---
title: Proprietà FontName (oggetto Balloon)
description: Fontname (proprietà)
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118839"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="ae1e3-103">Proprietà FontName (oggetto Balloon)</span><span class="sxs-lookup"><span data-stu-id="ae1e3-103">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="ae1e3-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae1e3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ae1e3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ae1e3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ae1e3-106">Restituisce o imposta il tipo di carattere utilizzato nella parola Balloon per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-106">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="ae1e3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="ae1e3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ae1e3-108">\*Agent. \***Characters ("**_CharacterID_\*_")._ \*  \[  =  *Tipo di carattere* Balloon. fontname\]</span><span class="sxs-lookup"><span data-stu-id="ae1e3-108">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="ae1e3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ae1e3-109">Part</span></span>   | <span data-ttu-id="ae1e3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae1e3-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="ae1e3-111">*carattere*</span><span class="sxs-lookup"><span data-stu-id="ae1e3-111">*font*</span></span> | <span data-ttu-id="ae1e3-112">Valore stringa corrispondente al nome del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae1e3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae1e3-113">Remarks</span></span>

<span data-ttu-id="ae1e3-114">La proprietà [**fontname**](fontname-property.md) definisce il tipo di carattere utilizzato per visualizzare il testo nella finestra a fumetti di una stringa.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-114">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="ae1e3-115">Il valore predefinito per le impostazioni del tipo di carattere del fumetto di parole di un carattere viene impostato nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-115">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="ae1e3-116">Inoltre, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-116">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="ae1e3-117">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="ae1e3-118">Se si usa un carattere non compilato, controllare le proprietà [**fontname**](fontname-property.md) e [**FontCharSet**](fontcharset-property.md) per il carattere per determinare se sono appropriate per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-118">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="ae1e3-119">Potrebbe essere necessario impostare questi valori prima di utilizzare il metodo [**Speak**](speak-method.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="ae1e3-119">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




