---
title: Risorsa DIALOGEX
description: Definisce una finestra di dialogo. | Risorsa DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menu risorse DIALOGEX e altre risorse
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234814"
---
# <a name="dialogex-resource"></a><span data-ttu-id="b048c-105">Risorsa DIALOGEX</span><span class="sxs-lookup"><span data-stu-id="b048c-105">DIALOGEX resource</span></span>

<span data-ttu-id="b048c-106">Definisce una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-106">Defines a dialog box.</span></span> <span data-ttu-id="b048c-107">L'istruzione definisce la posizione e le dimensioni della finestra di dialogo sullo schermo nonché lo stile della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span> <span data-ttu-id="b048c-108">Definisce inoltre quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b048c-108">It also defines the following:</span></span>

-   <span data-ttu-id="b048c-109">ID della guida nella finestra di dialogo e nei controlli all'interno della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-109">Help IDs on the dialog itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="b048c-110">Utilizzare l'istruzione [**ExStyle**](exstyle-statement.md) per la finestra di dialogo e i controlli all'interno della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-110">Use of the [**EXSTYLE**](exstyle-statement.md) statement for the dialog box itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="b048c-111">Spessore del carattere e impostazioni italiche per il tipo di carattere da utilizzare nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-111">Font weight and italic settings for the font to be used in the dialog box.</span></span>
-   <span data-ttu-id="b048c-112">Dati specifici del controllo per i controlli all'interno della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-112">Control-specific data for controls within the dialog box.</span></span>
-   <span data-ttu-id="b048c-113">Uso dei nomi di classe di sistema predefiniti **BEdit**, **IEDIT** e **hedit** .</span><span class="sxs-lookup"><span data-stu-id="b048c-113">Use of the **BEDIT**, **IEDIT**, and **HEDIT** predefined system class names.</span></span>

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a><span data-ttu-id="b048c-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="b048c-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b048c-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="b048c-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-116">Nome univoco o valore di Unsigned Integer a 16 bit univoco che identifica la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-116">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-117"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b048c-117"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-118">Posizione sulla schermata del lato sinistro della finestra di dialogo, in unità di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-118">Location on the screen of the left side of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-119"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="b048c-119"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-120">Posizione sullo schermo della parte superiore della finestra di dialogo, in unità di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-120">Location on the screen of the top of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-121"><span id="width"></span><span id="WIDTH"></span>*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="b048c-121"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-122">Larghezza della finestra di dialogo, in unità di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-122">Width of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-123"><span id="height"></span><span id="HEIGHT"></span>*altezza*</span><span class="sxs-lookup"><span data-stu-id="b048c-123"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-124">Altezza della finestra di dialogo, in unità di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-124">Height of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span><span class="sxs-lookup"><span data-stu-id="b048c-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-126">Espressione numerica che indica l'ID utilizzato per identificare la finestra di dialogo durante l'elaborazione della [**\_ Guida di WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="b048c-126">Numeric expression indicating the ID used to identify the dialog box during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*</span><span class="sxs-lookup"><span data-stu-id="b048c-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-128">Opzioni per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-128">Options for the dialog box.</span></span> <span data-ttu-id="b048c-129">Questa operazione può essere costituita da zero o più delle istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b048c-129">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="b048c-130">Istruzione</span><span class="sxs-lookup"><span data-stu-id="b048c-130">Statement</span></span>                                                         | <span data-ttu-id="b048c-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b048c-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b048c-132">**Didascalia** "*testo*"</span><span class="sxs-lookup"><span data-stu-id="b048c-132">**CAPTION** "*text*"</span></span>                                              | <span data-ttu-id="b048c-133">Didascalia della finestra di dialogo se dispone di una barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="b048c-133">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="b048c-134">Per ulteriori informazioni, vedere l' [**istruzione Caption**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-134">For more information, see [**CAPTION Statement**](caption-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b048c-135">**Caratteristiche** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="b048c-135">**CHARACTERISTICS** *dword*</span></span>                                       | <span data-ttu-id="b048c-136">Valore **DWORD** definito dall'utente per l'utilizzo da strumenti di risorse.</span><span class="sxs-lookup"><span data-stu-id="b048c-136">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="b048c-137">Questo valore non viene utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b048c-137">This value is not used by the system.</span></span> <span data-ttu-id="b048c-138">Per altre informazioni, vedere [**dichiarazione di caratteristiche**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-138">For more information, see [**CHARACTERISTICS Statement**](characteristics-statement.md).</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b048c-139">_Classe_ Class</span><span class="sxs-lookup"><span data-stu-id="b048c-139">**CLASS**_class_</span></span>                                                  | <span data-ttu-id="b048c-140">Unsigned Integer a 16 bit o una stringa racchiusa tra virgolette doppie ("), che identifica la classe della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-140">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="b048c-141">Per ulteriori informazioni, vedere [**istruzione Class**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-141">For more information, see [**CLASS Statement**](class-statement.md).</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b048c-142">**ExStyle** =  *stili estesi*</span><span class="sxs-lookup"><span data-stu-id="b048c-142">**EXSTYLE**= *extended-styles*</span></span>                                    | <span data-ttu-id="b048c-143">Stile finestra esteso della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-143">Extended window style of the dialog box.</span></span> <span data-ttu-id="b048c-144">Per ulteriori informazioni, vedere l' [**istruzione EXSTYLE**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-144">For more information, see [**EXSTYLE Statement**](exstyle-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b048c-145">**Font** *pointsize*, "*Typeface*", *Weight*, *Italic*, *CharSet*</span><span class="sxs-lookup"><span data-stu-id="b048c-145">**FONT** *pointsize*, "*typeface*", *weight*, *italic*, *charset*</span></span> | <span data-ttu-id="b048c-146">Dimensioni del punto e carattere tipografico per il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="b048c-146">Point size and typeface for the font.</span></span> <span data-ttu-id="b048c-147">Per *Weight*, usare i valori \*\* \_ \* FW\* _ definiti in wingdi. h.</span><span class="sxs-lookup"><span data-stu-id="b048c-147">For *weight*, use the \**FW\_\** _ values defined in WinGDI.h.</span></span> <span data-ttu-id="b048c-148">Per _italic \*, specificare TRUE per usare un tipo di carattere corsivo; in caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="b048c-148">For _italic\*, specify TRUE to use an italic font, FALSE otherwise.</span></span> <span data-ttu-id="b048c-149">Per *CharSet*, usare il valore definito nel membro **LfCharSet** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="b048c-149">For *charset*, use the value defined in the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="b048c-150">Per ottenere il tipo di carattere definitivo per una finestra di dialogo, un'applicazione deve specificare *CharSet* insieme ad altre proprietà del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="b048c-150">To get the definitive font for a dialog box, an application should specify *charset* along with other font properties.</span></span> <span data-ttu-id="b048c-151">Per altre informazioni, vedere [**istruzione font**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-151">For more information, see [**FONT Statement**](font-statement.md).</span></span> |
| <span data-ttu-id="b048c-152"> *Lingua* lingua, *lingua*</span><span class="sxs-lookup"><span data-stu-id="b048c-152">**LANGUAGE** *language*, *sublanguage*</span></span>                            | <span data-ttu-id="b048c-153">Lingua della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-153">Language of the dialog box.</span></span> <span data-ttu-id="b048c-154">Per ulteriori informazioni, vedere [**istruzione language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-154">For more information, see [**LANGUAGE Statement**](language-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b048c-155"> *Menu* menu</span><span class="sxs-lookup"><span data-stu-id="b048c-155">**MENU** *menuname*</span></span>                                               | <span data-ttu-id="b048c-156">Menu da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b048c-156">Menu to be used.</span></span> <span data-ttu-id="b048c-157">Questo valore è il nome del menu o il relativo identificatore di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="b048c-157">This value is either the name of the menu or its integer identifier.</span></span> <span data-ttu-id="b048c-158">Per ulteriori informazioni, vedere [**istruzione di menu**](menu-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-158">For more information, see [**MENU Statement**](menu-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b048c-159"> *Stili* di stile</span><span class="sxs-lookup"><span data-stu-id="b048c-159">**STYLE** *styles*</span></span>                                                | <span data-ttu-id="b048c-160">Stili della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b048c-160">Styles of the dialog box.</span></span> <span data-ttu-id="b048c-161">Per ulteriori informazioni, vedere [**istruzione Style**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-161">For more information, see [**STYLE Statement**](style-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b048c-162"> *DWORD* versione</span><span class="sxs-lookup"><span data-stu-id="b048c-162">**VERSION** *dword*</span></span>                                               | <span data-ttu-id="b048c-163">Valore **DWORD** definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b048c-163">User-defined **DWORD** value.</span></span> <span data-ttu-id="b048c-164">Questa istruzione è destinata all'utilizzo da parte di altri strumenti di risorse e non viene utilizzata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b048c-164">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="b048c-165">Per ulteriori informazioni, vedere [**istruzione version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-165">For more information, see [**VERSION Statement**](version-statement.md).</span></span>                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="b048c-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*istruzioni di controllo*</span><span class="sxs-lookup"><span data-stu-id="b048c-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-167">Il corpo della risorsa **DIALOGEX** è costituito da un numero qualsiasi di istruzioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-167">Body of the **DIALOGEX** resource is made up of any number of control statements.</span></span> <span data-ttu-id="b048c-168">Sono disponibili quattro famiglie di istruzioni di controllo: generico, statico, pulsante e modifica.</span><span class="sxs-lookup"><span data-stu-id="b048c-168">There are four families of control statements: generic, static, button, and edit.</span></span> <span data-ttu-id="b048c-169">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b048c-169">For more information, see Remarks.</span></span>

</dd> </dl>

<span data-ttu-id="b048c-170">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b048c-170">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="b048c-171">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-171">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b048c-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="b048c-172">Remarks</span></span>

<span data-ttu-id="b048c-173">Le operazioni valide che possono essere contenute in qualsiasi espressione numerica nelle istruzioni di **DIALOGEX** sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="b048c-173">The valid operations that may be contained in any of the numeric expressions in the statements of **DIALOGEX** are as follows:</span></span>

-   <span data-ttu-id="b048c-174">Aggiungi (' +')</span><span class="sxs-lookup"><span data-stu-id="b048c-174">Add ('+')</span></span>
-   <span data-ttu-id="b048c-175">Subtract ('-')</span><span class="sxs-lookup"><span data-stu-id="b048c-175">Subtract ('-')</span></span>
-   <span data-ttu-id="b048c-176">Meno unario ('-')</span><span class="sxs-lookup"><span data-stu-id="b048c-176">Unary minus ('-')</span></span>
-   <span data-ttu-id="b048c-177">NOT unario (' ~')</span><span class="sxs-lookup"><span data-stu-id="b048c-177">Unary NOT ('~')</span></span>
-   <span data-ttu-id="b048c-178">E (' &')</span><span class="sxs-lookup"><span data-stu-id="b048c-178">AND ('&')</span></span>
-   <span data-ttu-id="b048c-179">O (' \| ')</span><span class="sxs-lookup"><span data-stu-id="b048c-179">OR ('\|')</span></span>

<span data-ttu-id="b048c-180">Il corpo della risorsa è costituito da istruzioni generiche, statiche, di controllo Button e di modifica.</span><span class="sxs-lookup"><span data-stu-id="b048c-180">The body of the resource is made up of generic, static, button, and edit control statements.</span></span> <span data-ttu-id="b048c-181">Sebbene ognuna di queste famiglie di istruzioni usi una sintassi diversa per la definizione di funzionalità specifiche dei controlli, tutti condividono una sintassi comune per definire la posizione, le dimensioni, gli stili estesi, il numero di identificazione della guida e i dati specifici del controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-181">While each of these families of statements uses a different syntax for defining specific features of its controls, they all share a common syntax for defining the position, size, extended styles, help identification number, and control-specific data.</span></span> <span data-ttu-id="b048c-182">Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-182">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

### <a name="generic-control-statements"></a><span data-ttu-id="b048c-183">Istruzioni di controllo generico</span><span class="sxs-lookup"><span data-stu-id="b048c-183">Generic Control Statements</span></span>

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span data-ttu-id="b048c-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="b048c-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-185">Testo della finestra per il controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-185">Window text for the control.</span></span> <span data-ttu-id="b048c-186">Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-186">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="b048c-187"><span id="id"></span><span id="ID"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="b048c-187"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-188">Identificatore del controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-188">Control identifier.</span></span> <span data-ttu-id="b048c-189">Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-189">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="b048c-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span><span class="sxs-lookup"><span data-stu-id="b048c-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-191">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="b048c-191">Name of the class.</span></span> <span data-ttu-id="b048c-192">Può trattarsi di una stringa racchiusa tra virgolette doppie (") o di una delle classi di sistema predefinite seguenti: **Button**, **static**, **Edit**, **ListBox**, **ScrollBar** o **ComboBox**.</span><span class="sxs-lookup"><span data-stu-id="b048c-192">This may be either a string enclosed in double quotation marks (") or one of the following predefined system classes: **BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR**, or **COMBOBOX**.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-193"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="b048c-193"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-194">Gli stili della finestra (esplicito **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lbs \_ \* *_, _* SBS \_ \* *_ e _* \_ \*** i valori di stile CBS definiti in winuser. H possono essere usati aggiungendo un'inclusione al file RC: `#include "winuser.h"` ).</span><span class="sxs-lookup"><span data-stu-id="b048c-194">Window styles (explicit **WS\_\**_, _\* BS\_\**_, _\* SS\_\*\*_, _\* ES\_\*\*_, _\* LBS\_\*\*_, _\* SBS\_\*\*_, and _\* CBS\_\*\*\* style values defined in Winuser.H can be used by adding an include to the .rc file: `#include "winuser.h"`).</span></span> <span data-ttu-id="b048c-195">Per altre informazioni, vedere [stili di finestra](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="b048c-195">For more information, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span>

</dd> </dl>

### <a name="static-control-statements"></a><span data-ttu-id="b048c-196">Istruzioni di controllo statico</span><span class="sxs-lookup"><span data-stu-id="b048c-196">Static Control Statements</span></span>

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span data-ttu-id="b048c-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span><span class="sxs-lookup"><span data-stu-id="b048c-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-198">**LTEXT**, **RTEXT** o **CTEXT**.</span><span class="sxs-lookup"><span data-stu-id="b048c-198">**LTEXT**, **RTEXT**, or **CTEXT**.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="b048c-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-200">Testo della finestra per il controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-200">Window text for the control.</span></span> <span data-ttu-id="b048c-201">Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-201">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="b048c-202"><span id="id"></span><span id="ID"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="b048c-202"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-203">Identificatore del controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-203">Control identifier.</span></span> <span data-ttu-id="b048c-204">Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-204">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="button-control-statements"></a><span data-ttu-id="b048c-205">Istruzioni di controllo Button</span><span class="sxs-lookup"><span data-stu-id="b048c-205">Button Control Statements</span></span>

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span data-ttu-id="b048c-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span><span class="sxs-lookup"><span data-stu-id="b048c-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CheckBox**, **PUSHBOX**, **pulsante**, **RadioButton**, **STATE3** o **UserButton**.</span><span class="sxs-lookup"><span data-stu-id="b048c-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3**, or **USERBUTTON**.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="b048c-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-209">Testo della finestra per il controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-209">Window text for the control.</span></span> <span data-ttu-id="b048c-210">Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-210">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="b048c-211"><span id="id"></span><span id="ID"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="b048c-211"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-212">Identificatore del controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-212">Control identifier.</span></span> <span data-ttu-id="b048c-213">Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-213">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="edit-control-statements"></a><span data-ttu-id="b048c-214">Modificare le istruzioni di controllo</span><span class="sxs-lookup"><span data-stu-id="b048c-214">Edit Control Statements</span></span>

``` syntax
editClass id
```

<dl> <dt>

<span data-ttu-id="b048c-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span><span class="sxs-lookup"><span data-stu-id="b048c-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-216">**EDITTEXT**, **BEdit**, **hedit** o **IEDIT**.</span><span class="sxs-lookup"><span data-stu-id="b048c-216">**EDITTEXT**, **BEDIT**, **HEDIT**, or **IEDIT**.</span></span>

</dd> <dt>

<span data-ttu-id="b048c-217"><span id="id"></span><span id="ID"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="b048c-217"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="b048c-218">Identificatore del controllo.</span><span class="sxs-lookup"><span data-stu-id="b048c-218">Control identifier.</span></span> <span data-ttu-id="b048c-219">Per ulteriori informazioni, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b048c-219">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="b048c-220">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b048c-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b048c-221">Utilizzo delle finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="b048c-221">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="b048c-222">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="b048c-222">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="b048c-223">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="b048c-223">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="b048c-224">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="b048c-224">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="b048c-225">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="b048c-225">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="b048c-226">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="b048c-226">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="b048c-227">**DialogBox**</span><span class="sxs-lookup"><span data-stu-id="b048c-227">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="b048c-228">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="b048c-228">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="b048c-229">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="b048c-229">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="b048c-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="b048c-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="b048c-231">MENU</span><span class="sxs-lookup"><span data-stu-id="b048c-231">MENU</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b048c-232">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="b048c-232">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="b048c-233">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="b048c-233">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="b048c-234">**Versione**</span><span class="sxs-lookup"><span data-stu-id="b048c-234">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
