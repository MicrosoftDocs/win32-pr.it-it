---
description: La tabella MsiShortcutProperty consente al programma di installazione di Window di impostare le proprietà per i collegamenti che sono anche oggetti della shell di Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Tabella MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529797"
---
# <a name="msishortcutproperty-table"></a><span data-ttu-id="ef262-103">Tabella MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="ef262-103">MsiShortcutProperty Table</span></span>

<span data-ttu-id="ef262-104">La tabella MsiShortcutProperty consente al programma di installazione di Window di impostare le proprietà per i collegamenti che sono anche oggetti della [Shell di Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ef262-104">The MsiShortcutProperty table enables Window Installer to set properties for shortcuts that are also [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) objects.</span></span> <span data-ttu-id="ef262-105">A partire da Windows Vista e Windows Server 2008, la shell di Windows fornisce un'interfaccia IPropertyStore per gli oggetti della shell, ad esempio i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="ef262-105">Beginning with Windows Vista and Windows Server 2008 the Windows Shell provides an IPropertyStore Interface for shell objects such as shortcuts.</span></span> <span data-ttu-id="ef262-106">Un pacchetto Windows Installer 5,0 in esecuzione in Windows Server 2008 R2 o Windows 7 può impostare queste proprietà quando viene installato il collegamento.</span><span class="sxs-lookup"><span data-stu-id="ef262-106">A Windows Installer 5.0 package running on Windows Server 2008 R2 or Windows 7 can set these properties when the shortcut is installed.</span></span>

<span data-ttu-id="ef262-107">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="ef262-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="ef262-108">Questa tabella è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="ef262-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="ef262-109">La tabella MsiShortcutProperty include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="ef262-109">The MsiShortcutProperty table has the following columns.</span></span>



| <span data-ttu-id="ef262-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="ef262-110">Column</span></span>              | <span data-ttu-id="ef262-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef262-111">Type</span></span>                         | <span data-ttu-id="ef262-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="ef262-112">Key</span></span> | <span data-ttu-id="ef262-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="ef262-113">Nullable</span></span> |
|---------------------|------------------------------|-----|----------|
| <span data-ttu-id="ef262-114">MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="ef262-114">MsiShortcutProperty</span></span> | [<span data-ttu-id="ef262-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="ef262-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="ef262-116">S</span><span class="sxs-lookup"><span data-stu-id="ef262-116">Y</span></span>   | <span data-ttu-id="ef262-117">N</span><span class="sxs-lookup"><span data-stu-id="ef262-117">N</span></span>        |
| <span data-ttu-id="ef262-118">Tasto di scelta rapida\_</span><span class="sxs-lookup"><span data-stu-id="ef262-118">Shortcut\_</span></span>          | [<span data-ttu-id="ef262-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="ef262-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="ef262-120">N</span><span class="sxs-lookup"><span data-stu-id="ef262-120">N</span></span>   | <span data-ttu-id="ef262-121">N</span><span class="sxs-lookup"><span data-stu-id="ef262-121">N</span></span>        |
| <span data-ttu-id="ef262-122">PropertyKey</span><span class="sxs-lookup"><span data-stu-id="ef262-122">PropertyKey</span></span>         | [<span data-ttu-id="ef262-123">Formattato</span><span class="sxs-lookup"><span data-stu-id="ef262-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ef262-124">N</span><span class="sxs-lookup"><span data-stu-id="ef262-124">N</span></span>   | <span data-ttu-id="ef262-125">N</span><span class="sxs-lookup"><span data-stu-id="ef262-125">N</span></span>        |
| <span data-ttu-id="ef262-126">PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="ef262-126">PropVariantValue</span></span>    | [<span data-ttu-id="ef262-127">Formattato</span><span class="sxs-lookup"><span data-stu-id="ef262-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="ef262-128">N</span><span class="sxs-lookup"><span data-stu-id="ef262-128">N</span></span>   | <span data-ttu-id="ef262-129">N</span><span class="sxs-lookup"><span data-stu-id="ef262-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ef262-130">Colonne</span><span class="sxs-lookup"><span data-stu-id="ef262-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ef262-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="ef262-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span></span>
</dt> <dd>

<span data-ttu-id="ef262-132">Identificatore univoco per questa riga della tabella MsiShortcutProperty.</span><span class="sxs-lookup"><span data-stu-id="ef262-132">Unique identifier for this row of the MsiShortcutProperty table.</span></span>

</dd> <dt>

<span data-ttu-id="ef262-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Collegamento\_</span><span class="sxs-lookup"><span data-stu-id="ef262-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Shortcut\_</span></span>
</dt> <dd>

<span data-ttu-id="ef262-134">Chiave nella tabella dei [collegamenti](shortcut-table.md) che identifica il collegamento con una proprietà impostata.</span><span class="sxs-lookup"><span data-stu-id="ef262-134">A key into the [Shortcut](shortcut-table.md) table that identifies the shortcut having a property set.</span></span>

</dd> <dt>

<span data-ttu-id="ef262-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span><span class="sxs-lookup"><span data-stu-id="ef262-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span></span>
</dt> <dd>

<span data-ttu-id="ef262-136">Valore stringa che fornisce informazioni per la struttura [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) .</span><span class="sxs-lookup"><span data-stu-id="ef262-136">A string value that provides information for the [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure.</span></span> <span data-ttu-id="ef262-137">Le informazioni contenute in questo campo devono fare riferimento al nome canonico di una proprietà registrata con il sistema di proprietà di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef262-137">The information in this field must refer to the canonical name of a property registered with the Windows property system.</span></span> <span data-ttu-id="ef262-138">Per ulteriori informazioni sul sistema di proprietà di Windows, vedere [Cenni preliminari sul sistema di proprietà](/previous-versions//bb776909(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef262-138">For more information about the Windows property system, see the [Property System Overview](/previous-versions//bb776909(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ef262-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="ef262-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span></span>
</dt> <dd>

<span data-ttu-id="ef262-140">Valore stringa che fornisce informazioni per la struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="ef262-140">A string value that provides information for the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

</dd> </dl>

<span data-ttu-id="ef262-141">È possibile impostare più proprietà in un collegamento.</span><span class="sxs-lookup"><span data-stu-id="ef262-141">Multiple properties can be set on a shortcut.</span></span> <span data-ttu-id="ef262-142">Se la stessa proprietà viene impostata più volte nello stesso collegamento, il valore viene impostato in un ordine non specificato.</span><span class="sxs-lookup"><span data-stu-id="ef262-142">If the same property is set multiple times on the same shortcut the value is set in an unspecified order.</span></span>

<span data-ttu-id="ef262-143">Windows Installer possibile impostare le proprietà dei tasti di scelta rapida solo quando si installa o si reinstalla il collegamento.</span><span class="sxs-lookup"><span data-stu-id="ef262-143">Windows Installer can set shortcut properties only when the shortcut is installed or reinstalled.</span></span> <span data-ttu-id="ef262-144">Una patch che non reinstalla un collegamento che è già stato installato non aggiorna le proprietà del collegamento.</span><span class="sxs-lookup"><span data-stu-id="ef262-144">A patch that does not reinstall a shortcut that has already been installed does not update the shortcut's properties.</span></span> <span data-ttu-id="ef262-145">Una patch può aggiornare le proprietà includendo una tabella dei [collegamenti](shortcut-table.md) nel pacchetto di patch e reinstallando il collegamento.</span><span class="sxs-lookup"><span data-stu-id="ef262-145">A patch can update the properties by including a [Shortcut](shortcut-table.md) table in the patch package and reinstalling the shortcut.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef262-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef262-146">Remarks</span></span>

<span data-ttu-id="ef262-147">[Windows Installer messaggio di errore](windows-installer-error-messages.md) 1946 viene restituito come avviso e l'installazione continua, se Windows Installer non è in grado di impostare una proprietà di collegamento specificata nella tabella MsiShortcutProperty.</span><span class="sxs-lookup"><span data-stu-id="ef262-147">[Windows Installer Error Message](windows-installer-error-messages.md) 1946 is returned as a warning, and the installation continues, if Windows Installer is unable to set a shortcut property specified in the MsiShortcutProperty table.</span></span>

## <a name="validation"></a><span data-ttu-id="ef262-148">Convalida</span><span class="sxs-lookup"><span data-stu-id="ef262-148">Validation</span></span>

<dl>

[<span data-ttu-id="ef262-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="ef262-149">ICE03</span></span>](ice03.md)  
</dl>

 

 
