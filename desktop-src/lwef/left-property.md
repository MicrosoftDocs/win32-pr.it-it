---
title: Proprietà Left (oggetto characters)
description: Left (proprietà)
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300911"
---
# <a name="left-property-characters-object"></a><span data-ttu-id="a7518-103">Proprietà Left (oggetto characters)</span><span class="sxs-lookup"><span data-stu-id="a7518-103">Left Property (Characters Object)</span></span>

<span data-ttu-id="a7518-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a7518-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a7518-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a7518-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a7518-106">Restituisce o imposta il bordo sinistro del frame del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="a7518-106">Returns or sets the left edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="a7518-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a7518-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a7518-108">\*agente \***. Caratteri ("**_CharacterID_\*_")._ \*  \[  =  *Valore* a sinistra\]</span><span class="sxs-lookup"><span data-stu-id="a7518-108">*agent\***.Characters ("**_CharacterID_*_").Left_\* \[ = *value*\]</span></span>



| <span data-ttu-id="a7518-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a7518-109">Part</span></span>    | <span data-ttu-id="a7518-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7518-110">Description</span></span>                                                           |
|---------|-----------------------------------------------------------------------|
| <span data-ttu-id="a7518-111">*value*</span><span class="sxs-lookup"><span data-stu-id="a7518-111">*value*</span></span> | <span data-ttu-id="a7518-112">Valore long integer che specifica il bordo sinistro del frame del carattere.</span><span class="sxs-lookup"><span data-stu-id="a7518-112">A Long integer that specifies the left edge of the character's frame.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7518-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7518-113">Remarks</span></span>

<span data-ttu-id="a7518-114">La proprietà **Left** è sempre espressa in pixel, in relazione all'origine dello schermo (in alto a sinistra).</span><span class="sxs-lookup"><span data-stu-id="a7518-114">The **Left** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="a7518-115">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="a7518-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="a7518-116">Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a7518-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




