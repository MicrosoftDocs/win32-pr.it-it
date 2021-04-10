---
title: E (menu e altre risorse)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118855"
---
# <a name="e-menus-and-other-resources"></a><span data-ttu-id="bbf3d-103">E (menu e altre risorse)</span><span class="sxs-lookup"><span data-stu-id="bbf3d-103">E (Menus and Other Resources)</span></span>

<span data-ttu-id="bbf3d-104">[A](a.md) [B](b.md) [C](c.md) d E [F](f.md) G H [i](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="bbf3d-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bbf3d-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Menu vuoti non consentiti**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Empty menus not allowed**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-106">Una parola chiave **end** viene visualizzata prima che tutte le voci di menu siano definite nell'istruzione di [**menu**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-106">An **END** keyword appears before any menu items are defined in the [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="bbf3d-107">I menu vuoti non sono consentiti dal compilatore di risorse Microsoft Windows 32 (RC).</span><span class="sxs-lookup"><span data-stu-id="bbf3d-107">Empty menus are not permitted by Microsoft Windows 32 Resource Compiler (RC).</span></span> <span data-ttu-id="bbf3d-108">Assicurarsi che non siano presenti virgolette di apertura nell'istruzione di **menu** .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-108">Make sure that you do not have any opening quotation marks within the **MENU** statement.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**FINE prevista nella finestra di dialogo**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**END expected in Dialog**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-110">La parola chiave **end** deve essere visualizzata alla fine di un'istruzione della [**finestra di dialogo**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-110">The **END** keyword must appear at the end of a [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="bbf3d-111">Verificare che non siano presenti virgolette di apertura rimaste nell'istruzione precedente.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-111">Make sure that there are no opening quotation marks left from the preceding statement.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**FINE prevista nel menu**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END expected in menu**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-113">La parola chiave **end** deve essere visualizzata alla fine di un'istruzione di [**menu**](menu-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-113">The **END** keyword must appear at the end of a [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="bbf3d-114">Verificare che non siano presenti istruzioni **Begin** e **end** non corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-114">Make sure that there are no mismatched **BEGIN** and **END** statements.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Errore Creatingresource-nome**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Error Creatingresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-116">Il compilatore di risorse Microsoft Windows 32 (RC) non è riuscito a creare la risorsa binaria specificata (. File RES).</span><span class="sxs-lookup"><span data-stu-id="bbf3d-116">Microsoft Windows 32 Resource Compiler (RC) could not create the specified binary resource (.RES) file.</span></span> <span data-ttu-id="bbf3d-117">Assicurarsi che non venga creato in un'unità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-117">Make sure that it is not being created on a read-only drive.</span></span> <span data-ttu-id="bbf3d-118">Usare l'opzione **/v** per verificare se il file è in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-118">Use the **/v** option to find out whether the file is being created.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Prevista virgola nella tabella dei tasti di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Expected Comma in Accelerator Table**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-120">Il compilatore di risorse Microsoft Windows 32 (RC) richiede una virgola tra i parametri *Event* e *idValue* nell'istruzione [**Accelerators**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-120">Microsoft Windows 32 Resource Compiler (RC) requires a comma between the *event* and *idvalue* parameters in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Previsto nome classe di controllo**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Expected control class name**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-122">Il parametro *Class* di un'istruzione di [**controllo**](control-control.md) nell'istruzione [**Dialog**](dialog-resource.md) deve essere uno dei seguenti tipi di controllo: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** o definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-122">The *class* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement must be one of the following control types: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR**](scrollbar-control.md), **STATIC**, or user-defined.</span></span> <span data-ttu-id="bbf3d-123">Verificare che la classe sia stata digitata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-123">Make sure that the class is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Nome del tipo di carattere previsto**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Expected font face name**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-125">Il parametro *Typeface* dell'istruzione **font** nell'istruzione [**Dialog**](dialog-resource.md) deve essere una stringa di caratteri racchiusa tra virgolette doppie (").</span><span class="sxs-lookup"><span data-stu-id="bbf3d-125">The *typeface* parameter of the **FONT** statement in the [**DIALOG**](dialog-resource.md) statement must be a character string enclosed in double quotation marks (").</span></span> <span data-ttu-id="bbf3d-126">Questo parametro specifica il nome di un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-126">This parameter specifies the name of a font.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Previsto valore ID per MenuItem**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Expected ID value for Menuitem**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-128">L'istruzione [**menu**](menu-resource.md) deve contenere un'istruzione [**MenuItem**](menuitem-statement.md) , che include un Integer o una costante simbolica nel parametro *menuID* .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-128">The [**MENU**](menu-resource.md) statement must contain a [**MENUITEM**](menuitem-statement.md) statement, which has either an integer or a symbolic constant in the *MenuID* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Prevista stringa di menu**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Expected Menu String**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-130">Ogni istruzione [**MenuItem**](menuitem-statement.md) e [**popup**](popup-resource.md) deve contenere un parametro di *testo* .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-130">Each [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statement must contain a *text* parameter.</span></span> <span data-ttu-id="bbf3d-131">Questo parametro è una stringa racchiusa tra virgolette doppie (") che specifica il nome della voce di menu o del menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-131">This parameter is a string enclosed in double quotation marks (") that specifies the name of the menu item or pop-up menu.</span></span> <span data-ttu-id="bbf3d-132">Un'istruzione del **separatore MenuItem** non richiede una stringa racchiusa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-132">A **MENUITEM SEPARATOR** statement requires no quoted string.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Previsto valore del comando numerico**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Expected numeric command value**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-134">Per il compilatore di risorse di Microsoft Windows (RC) era previsto un parametro numerico *idValue* nell'istruzione [**Accelerators**](accelerators-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-134">Microsoft Windows Resource Compiler (RC) was expecting a numeric *idvalue* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span> <span data-ttu-id="bbf3d-135">Assicurarsi di aver usato un'istruzione [**\# define**](-define.md) per specificare il valore e che la costante utilizzata sia stata digitata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-135">Make sure that you have used a [**\#define**](-define.md) statement to specify the value and that the constant used is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Prevista costante numerica nella tabella di stringhe**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Expected numeric constant in string table**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-137">Una costante numerica, definita in un'istruzione [**\# define**](-define.md) , deve seguire immediatamente la parola chiave **Begin** in un'istruzione [**un'STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-137">A numeric constant, defined in a [**\#define**](-define.md) statement, must immediately follow the **BEGIN** keyword in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Dimensioni previste per i punti numerici**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Expected numeric point size**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-139">Il parametro *pointsize* dell'istruzione [**font**](font-statement.md) nell'istruzione [**Dialog**](dialog-resource.md) deve essere un valore di dimensione in punti Integer.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-139">The *pointsize* parameter of the [**FONT**](font-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer point-size value.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Prevista costante finestra di dialogo numerica**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Expected Numerical Dialog constant**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-141">Un'istruzione della [**finestra di dialogo**](dialog-resource.md) richiede valori integer per i parametri *x*, *y*, *Width* e *Height* .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-141">A [**DIALOG**](dialog-resource.md) statement requires integer values for the *x*, *y*, *width*, and *height* parameters.</span></span> <span data-ttu-id="bbf3d-142">Verificare che questi valori, inclusi dopo la parola chiave della **finestra di dialogo** , non siano negativi.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-142">Make sure that these values, which are included after the **DIALOG** keyword, are not negative.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Prevista stringa in un'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Expected String in STRINGTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-144">È prevista una stringa dopo ogni parametro numerico *stringid* in un'istruzione [**un'STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-144">A string is expected after each numeric *stringid* parameter in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Prevista stringa o comando costante Accelerator**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Expected String or Constant Accelerator command**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-146">Il compilatore di risorse di Microsoft Windows (RC) non è riuscito a determinare la chiave configurata per l'acceleratore.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-146">Microsoft Windows Resource Compiler (RC) was not able to determine which key was being set up for the accelerator.</span></span> <span data-ttu-id="bbf3d-147">Il parametro *Event* nell'istruzione [**Accelerators**](accelerators-resource.md) potrebbe non essere valido.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-147">The *event* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement might be invalid.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**È prevista una parola chiave VALUE, BLOCK o END.**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Expected VALUE, BLOCK, or END keyword.**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-149">La struttura [**VERSIONINFO**](versioninfo-resource.md) richiede una parola chiave **value**, **Block** o **end** .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-149">The [**VERSIONINFO**](versioninfo-resource.md) structure requires a **VALUE**, **BLOCK**, or **END** keyword.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Previsto numero per ID**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Expecting number for ID**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-151">È previsto un numero per il parametro *ID* di un'istruzione di [**controllo**](control-control.md) nell'istruzione della [**finestra di dialogo**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3d-151">A number is expected for the *id* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="bbf3d-152">Assicurarsi di disporre di un numero o di un'istruzione [**\# define**](-define.md) per l'identificatore del controllo.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-152">Make sure that you have a number or a [**\#define**](-define.md) statement for the control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Prevista stringa tra virgolette per la chiave**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Expecting quoted string for key**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-154">La stringa chiave che segue la parola chiave **Block** o **value** deve essere racchiusa tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="bbf3d-154">The key string following the **BLOCK** or **VALUE** keyword should be enclosed in double quotation marks.</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Prevista stringa tra virgolette nella classe della finestra di dialogo**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Expecting quoted string in dialog class**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-156">Il parametro *Class* dell'istruzione [**Class**](class-statement.md) nell'istruzione [**Dialog**](dialog-resource.md) deve essere un numero intero o una stringa racchiusa tra virgolette doppie (").</span><span class="sxs-lookup"><span data-stu-id="bbf3d-156">The *class* parameter of the [**CLASS**](class-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer or a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="bbf3d-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Prevista stringa tra virgolette nel titolo della finestra di dialogo**</span><span class="sxs-lookup"><span data-stu-id="bbf3d-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Expecting quoted string in dialog title**</span></span>
</dt> <dd>

<span data-ttu-id="bbf3d-158">Il parametro *CaptionText* dell'istruzione [**Caption**](caption-statement.md) nell'istruzione [**Dialog**](dialog-resource.md) deve essere una stringa di caratteri racchiusa tra virgolette doppie (").</span><span class="sxs-lookup"><span data-stu-id="bbf3d-158">The *captiontext* parameter of the [**CAPTION**](caption-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be a character string, enclosed in double quotation marks (").</span></span>

</dd> </dl>

 

 




