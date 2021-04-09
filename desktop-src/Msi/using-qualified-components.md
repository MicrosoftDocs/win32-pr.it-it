---
description: I componenti qualificati sono un metodo di riferimento indiretto e possono essere usati per raggruppare componenti con funzionalità parallele in categorie.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Utilizzo di componenti qualificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129358"
---
# <a name="using-qualified-components"></a><span data-ttu-id="786df-103">Utilizzo di componenti qualificati</span><span class="sxs-lookup"><span data-stu-id="786df-103">Using Qualified Components</span></span>

<span data-ttu-id="786df-104">I componenti qualificati sono un metodo di riferimento indiretto e possono essere usati per raggruppare componenti con funzionalità parallele in categorie.</span><span class="sxs-lookup"><span data-stu-id="786df-104">Qualified components are a method of indirection and can be used to group components with parallel functionality into categories.</span></span>

<span data-ttu-id="786df-105">Per restituire il percorso completo e installare un [componente completo](qualified-components.md), chiamare [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) o [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span><span class="sxs-lookup"><span data-stu-id="786df-105">To return the full path and install a [qualified component](qualified-components.md), call [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span></span>

<span data-ttu-id="786df-106">Per enumerare tutti i qualificatori del componente completo e le stringhe descrittive, chiamare [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="786df-106">To enumerate all of the qualified component qualifiers and descriptive strings, call [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

<span data-ttu-id="786df-107">**Per raggruppare i componenti in una categoria di componenti qualificati**</span><span class="sxs-lookup"><span data-stu-id="786df-107">**To group components together into a qualified-component category**</span></span>

1.  <span data-ttu-id="786df-108">È necessario che nella [tabella](component-table.md) dei componenti sia presente un record per ogni componente incluso nella nuova categoria di componenti qualificati.</span><span class="sxs-lookup"><span data-stu-id="786df-108">There must be a record in the [Component table](component-table.md) for each component that is included in the new category of qualified components.</span></span> <span data-ttu-id="786df-109">Modificare i campi nella tabella dei componenti come per i componenti ordinari.</span><span class="sxs-lookup"><span data-stu-id="786df-109">Author the fields in the Component table the same as for ordinary components.</span></span> <span data-ttu-id="786df-110">Si noti che ogni componente qualificato deve avere un GUID ID componente univoco immesso nella colonna ComponentId della tabella Component.</span><span class="sxs-lookup"><span data-stu-id="786df-110">Note that each qualified component must have a unique component ID GUID entered in the ComponentId column of the Component table.</span></span>
2.  <span data-ttu-id="786df-111">Genera una stringa di testo qualificatore per ogni componente completo.</span><span class="sxs-lookup"><span data-stu-id="786df-111">Generate a qualifier text string for each qualified component.</span></span> <span data-ttu-id="786df-112">Il qualificatore deve essere una stringa di testo univoca che può essere generata facilmente durante la ricerca di un componente completo.</span><span class="sxs-lookup"><span data-stu-id="786df-112">The qualifier must be unique text string that can be easily generated when searching for a qualified component.</span></span> <span data-ttu-id="786df-113">Se, ad esempio, i componenti della categoria vengono qualificati in base alla lingua, l'identificatore delle impostazioni locali (LCID) numerico è una stringa di qualificatore ragionevole.</span><span class="sxs-lookup"><span data-stu-id="786df-113">For example, if the components in the category are being qualified by language, the numeric locale identifier (LCID) is a reasonable qualifier string.</span></span>
3.  <span data-ttu-id="786df-114">Aggiungere un record nella [tabella PublishComponent](publishcomponent-table.md) per ogni componente completo.</span><span class="sxs-lookup"><span data-stu-id="786df-114">Add a record in the [PublishComponent table](publishcomponent-table.md) for each qualified component.</span></span> <span data-ttu-id="786df-115">Immettere gli identificatori dei componenti completi dalla colonna componente della tabella Component nella \_ colonna Component della tabella PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="786df-115">Enter the qualified-component identifiers from the Component column of the Component table into the Component\_ column of the PublishComponent table.</span></span> <span data-ttu-id="786df-116">Immettere le stringhe di qualificatore per ogni componente qualificato nella colonna qualificatore.</span><span class="sxs-lookup"><span data-stu-id="786df-116">Enter the qualifier strings for each qualified component into the Qualifier column.</span></span> <span data-ttu-id="786df-117">Immettere una stringa localizzata da visualizzare all'utente e descrivere il componente qualificato nella colonna AppData facoltativa.</span><span class="sxs-lookup"><span data-stu-id="786df-117">Enter a localized string to be displayed to the user and describing the qualified component into the optional AppData column.</span></span> <span data-ttu-id="786df-118">È necessario inserire nel campo AppData una stringa esplicativa, ad esempio "dizionario francese", anziché solo l'identificatore LCID numerico.</span><span class="sxs-lookup"><span data-stu-id="786df-118">An explanatory string should be put in the AppData field, such as "French Dictionary," rather than just the numeric LCID.</span></span> <span data-ttu-id="786df-119">Immettere il nome della funzionalità che utilizza questo componente nella \_ colonna feature.</span><span class="sxs-lookup"><span data-stu-id="786df-119">Enter the name of the feature that uses this component into the Feature\_ column.</span></span> <span data-ttu-id="786df-120">L'identificatore di funzionalità in questo campo deve essere elencato anche nella colonna feature della [tabella Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="786df-120">The feature identifier in this field must also be listed in the Feature column of the [Feature table](feature-table.md).</span></span>
4.  <span data-ttu-id="786df-121">Genera un GUID di categoria per questa categoria di componenti qualificati.</span><span class="sxs-lookup"><span data-stu-id="786df-121">Generate a category GUID for this category of qualified components.</span></span> <span data-ttu-id="786df-122">Deve essere un [GUID](guid.md)valido.</span><span class="sxs-lookup"><span data-stu-id="786df-122">This must be a valid [GUID](guid.md).</span></span> <span data-ttu-id="786df-123">Se si usa un'utilità come GUIDGEN per generare il GUID, assicurarsi che contenga solo lettere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="786df-123">If you use a utility such as GUIDGEN to generate the GUID be sure that it contains only uppercase letters.</span></span> <span data-ttu-id="786df-124">Per ogni componente qualificato in questa categoria, immettere il GUID della categoria nel campo ComponentId della [tabella PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="786df-124">For every qualified component in this category, enter the category GUID into the ComponentId field of the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="786df-125">Nell'esempio seguente viene illustrato il modo in cui viene creata la categoria "modelli FAX" di componenti qualificati nelle tabelle componente, funzionalità e PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="786df-125">The following example illustrates how the "FAX Templates" category of qualified components are authored into the Component, Feature, and PublishComponent tables.</span></span>

[<span data-ttu-id="786df-126">Tabella PublishComponent</span><span class="sxs-lookup"><span data-stu-id="786df-126">PublishComponent table</span></span>](publishcomponent-table.md)



| <span data-ttu-id="786df-127">ComponentId</span><span class="sxs-lookup"><span data-stu-id="786df-127">ComponentId</span></span>                  | <span data-ttu-id="786df-128">Qualifier</span><span class="sxs-lookup"><span data-stu-id="786df-128">Qualifier</span></span> | <span data-ttu-id="786df-129">AppData</span><span class="sxs-lookup"><span data-stu-id="786df-129">AppData</span></span>             | <span data-ttu-id="786df-130">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="786df-130">Feature\_</span></span>   | <span data-ttu-id="786df-131">Componente\_</span><span class="sxs-lookup"><span data-stu-id="786df-131">Component\_</span></span>    |
|------------------------------|-----------|---------------------|-------------|----------------|
| <span data-ttu-id="786df-132">{GUID categoria modello FAX}</span><span class="sxs-lookup"><span data-stu-id="786df-132">{FAX Template Category GUID}</span></span> | <span data-ttu-id="786df-133">1033</span><span class="sxs-lookup"><span data-stu-id="786df-133">1033</span></span>      | <span data-ttu-id="786df-134">Modello di inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="786df-134">US English template</span></span> | <span data-ttu-id="786df-135">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="786df-135">FAXTemplate</span></span> | <span data-ttu-id="786df-136">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="786df-136">FAXTemplateENU</span></span> |
|                              | <span data-ttu-id="786df-137">1041</span><span class="sxs-lookup"><span data-stu-id="786df-137">1041</span></span>      | <span data-ttu-id="786df-138">Modello giapponese</span><span class="sxs-lookup"><span data-stu-id="786df-138">Japanese template</span></span>   | <span data-ttu-id="786df-139">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="786df-139">FAXTemplate</span></span> | <span data-ttu-id="786df-140">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="786df-140">FAXTemplateJPN</span></span> |
|                              | <span data-ttu-id="786df-141">1054</span><span class="sxs-lookup"><span data-stu-id="786df-141">1054</span></span>      | <span data-ttu-id="786df-142">Modello tailandese</span><span class="sxs-lookup"><span data-stu-id="786df-142">Thai template</span></span>       | <span data-ttu-id="786df-143">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="786df-143">FAXTemplate</span></span> | <span data-ttu-id="786df-144">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="786df-144">FAXTemplateTHA</span></span> |
|                              | <span data-ttu-id="786df-145">1031</span><span class="sxs-lookup"><span data-stu-id="786df-145">1031</span></span>      | <span data-ttu-id="786df-146">Modello tedesco</span><span class="sxs-lookup"><span data-stu-id="786df-146">German template</span></span>     | <span data-ttu-id="786df-147">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="786df-147">FAXTemplate</span></span> | <span data-ttu-id="786df-148">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="786df-148">FAXTemplateDEU</span></span> |



 

<span data-ttu-id="786df-149">[Tabella componenti](component-table.md) (tabella parziale)</span><span class="sxs-lookup"><span data-stu-id="786df-149">[Component table](component-table.md) (partial table)</span></span>



| <span data-ttu-id="786df-150">Componente</span><span class="sxs-lookup"><span data-stu-id="786df-150">Component</span></span>      | <span data-ttu-id="786df-151">ComponentId</span><span class="sxs-lookup"><span data-stu-id="786df-151">ComponentId</span></span>                                  |
|----------------|----------------------------------------------|
| <span data-ttu-id="786df-152">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="786df-152">FAXTemplateENU</span></span> | <span data-ttu-id="786df-153">{*Modello Fax (Inglese Stati Uniti) GUID componente*}</span><span class="sxs-lookup"><span data-stu-id="786df-153">{*FAX Template (US English) component GUID*}</span></span> |
| <span data-ttu-id="786df-154">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="786df-154">FAXTemplateJPN</span></span> | <span data-ttu-id="786df-155">{*GUID componente (giapponese) del modello Fax*}</span><span class="sxs-lookup"><span data-stu-id="786df-155">{*FAX Template (Japanese) component GUID*}</span></span>   |
| <span data-ttu-id="786df-156">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="786df-156">FAXTemplateTHA</span></span> | <span data-ttu-id="786df-157">{*GUID del componente del modello Fax (Thai)*}</span><span class="sxs-lookup"><span data-stu-id="786df-157">{*FAX Template (Thai) component GUID*}</span></span>       |
| <span data-ttu-id="786df-158">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="786df-158">FAXTemplateDEU</span></span> | <span data-ttu-id="786df-159">{*Modello Fax (tedesco) GUID componente*}</span><span class="sxs-lookup"><span data-stu-id="786df-159">{*FAX Template (German) component GUID*}</span></span>     |



 

<span data-ttu-id="786df-160">[Tabella Feature](feature-table.md) (tabella parziale)</span><span class="sxs-lookup"><span data-stu-id="786df-160">[Feature table](feature-table.md) (partial table)</span></span>



| <span data-ttu-id="786df-161">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="786df-161">Feature</span></span>     |
|-------------|
| <span data-ttu-id="786df-162">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="786df-162">FAXTemplate</span></span> |
| <span data-ttu-id="786df-163">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="786df-163">FAXTemplate</span></span> |
| <span data-ttu-id="786df-164">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="786df-164">FAXTemplate</span></span> |
| <span data-ttu-id="786df-165">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="786df-165">FAXTemplate</span></span> |



 

 

 



