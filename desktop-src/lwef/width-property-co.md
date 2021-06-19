---
title: Proprietà Width (oggetto Characters)
description: Informazioni sulla proprietà Width dell'oggetto Characters, che restituisce o imposta la larghezza del frame per il carattere specificato.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395127"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="a642b-103">Proprietà Width (oggetto Characters)</span><span class="sxs-lookup"><span data-stu-id="a642b-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="a642b-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a642b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a642b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a642b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a642b-106">Restituisce o imposta la larghezza del frame per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="a642b-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a642b-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a642b-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="a642b-108">*agent\***. Caratteri ("**_CharacterID_*_"). Valore_ \*  \[ =  *larghezza*\]</span><span class="sxs-lookup"><span data-stu-id="a642b-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="a642b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a642b-109">Part</span></span>    | <span data-ttu-id="a642b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a642b-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="a642b-111">*value*</span><span class="sxs-lookup"><span data-stu-id="a642b-111">*value*</span></span> | <span data-ttu-id="a642b-112">Valore Long Integer che specifica la larghezza del frame del carattere.</span><span class="sxs-lookup"><span data-stu-id="a642b-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a642b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a642b-113">Remarks</span></span>

<span data-ttu-id="a642b-114">La [**proprietà Width**](width-property.md) è sempre espressa in pixel.</span><span class="sxs-lookup"><span data-stu-id="a642b-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="a642b-115">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="a642b-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="a642b-116">Anche se il carattere viene visualizzato in una finestra di area di forma irregolare, la posizione del carattere si basa sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor di caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a642b-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




