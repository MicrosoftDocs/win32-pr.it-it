---
description: Se viene impostato questo flag di bit, i tipi di carattere vengono creati utilizzando la tabella codici dell'interfaccia utente predefinita dell'utente. Se il flag di bit non è impostato, i tipi di carattere vengono creati utilizzando la tabella codici del database.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Attributo di controllo UsersLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310966"
---
# <a name="userslanguage-control-attribute"></a><span data-ttu-id="95956-104">Attributo di controllo UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="95956-104">UsersLanguage Control Attribute</span></span>

<span data-ttu-id="95956-105">Se viene impostato questo flag di bit, i tipi di carattere vengono creati utilizzando la tabella codici dell'interfaccia utente predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="95956-105">If this bit flag is set, fonts are created using the user's default UI code page.</span></span> <span data-ttu-id="95956-106">Se il flag di bit non è impostato, i tipi di carattere vengono creati utilizzando la tabella codici del database.</span><span class="sxs-lookup"><span data-stu-id="95956-106">If the bit flag is not set, fonts are created using the database code page.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="95956-107">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="95956-107">Valid Controls</span></span>

[<span data-ttu-id="95956-108">Text</span><span class="sxs-lookup"><span data-stu-id="95956-108">Text</span></span>](text-control.md)

 

[<span data-ttu-id="95956-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="95956-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="95956-110">ComboBox</span><span class="sxs-lookup"><span data-stu-id="95956-110">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="95956-111">Valore</span><span class="sxs-lookup"><span data-stu-id="95956-111">Value</span></span>



| <span data-ttu-id="95956-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="95956-112">Decimal</span></span> | <span data-ttu-id="95956-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="95956-113">Hexadecimal</span></span> | <span data-ttu-id="95956-114">Costante</span><span class="sxs-lookup"><span data-stu-id="95956-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="95956-115">1048576</span><span class="sxs-lookup"><span data-stu-id="95956-115">1048576</span></span> | <span data-ttu-id="95956-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="95956-116">0x00100000</span></span>  | <span data-ttu-id="95956-117">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="95956-117">**msidbControlAttributesUsersLanguage**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="95956-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="95956-118">Remarks</span></span>

<span data-ttu-id="95956-119">Questo attributo di controllo può essere usato per visualizzare il testo immesso dall'utente in un controllo [Edit](edit-control.md) o [PathEdit](pathedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="95956-119">This control attribute can be used to display text that the user has entered into an [Edit](edit-control.md) or [PathEdit](pathedit-control.md) control.</span></span>

<span data-ttu-id="95956-120">Il controllo di modifica, il controllo PathEdit, il [controllo Directory](directorylist-control.md) e il [controllo DirectoryCombo](directorycombo-control.md) utilizzano sempre i tipi di carattere creati nella tabella codici dell'interfaccia utente predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="95956-120">The Edit control, PathEdit control, [DirectoryList control](directorylist-control.md) and [DirectoryCombo control](directorycombo-control.md) always use the fonts created in the user's default UI code page.</span></span> <span data-ttu-id="95956-121">Questo può causare problemi se nel sistema operativo sono state installate altre lingue.</span><span class="sxs-lookup"><span data-stu-id="95956-121">This can cause problems if additional languages have been installed on the operating system.</span></span> <span data-ttu-id="95956-122">In questo caso, i tipi di carattere nel computer potrebbero non essere in grado di rappresentare tutti i caratteri nelle lingue aggiunte.</span><span class="sxs-lookup"><span data-stu-id="95956-122">In this case, the fonts on the computer may not be able to represent all the characters in the added languages.</span></span> <span data-ttu-id="95956-123">Per determinare quali tipi di carattere è possibile usare, cercare i valori in **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SYSTEMLINK**.</span><span class="sxs-lookup"><span data-stu-id="95956-123">To determine what fonts can be used, look up the values in **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\FontLink\\SystemLink**.</span></span>

<span data-ttu-id="95956-124">Per altre informazioni, vedere [controllare gli attributi](control-attributes.md) e i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="95956-124">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



