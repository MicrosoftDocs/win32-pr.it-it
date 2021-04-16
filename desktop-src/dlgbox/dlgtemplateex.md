---
title: Struttura DLGTEMPLATEEX
description: Un modello di finestra di dialogo esteso inizia con un'intestazione DLGTEMPLATEEX che descrive la finestra di dialogo e specifica il numero di controlli nella finestra di dialogo.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Finestre di dialogo struttura DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518352"
---
# <a name="dlgtemplateex-structure"></a><span data-ttu-id="e9f9e-104">Struttura DLGTEMPLATEEX</span><span class="sxs-lookup"><span data-stu-id="e9f9e-104">DLGTEMPLATEEX structure</span></span>

<span data-ttu-id="e9f9e-105">Un modello di finestra di dialogo esteso inizia con un'intestazione **DLGTEMPLATEEX** che descrive la finestra di dialogo e specifica il numero di controlli nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-105">An extended dialog box template begins with a **DLGTEMPLATEEX** header that describes the dialog box and specifies the number of controls in the dialog box.</span></span> <span data-ttu-id="e9f9e-106">Per ogni controllo in una finestra di dialogo, un modello di finestra di dialogo esteso ha un blocco di dati che usa il formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) per descrivere il controllo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-106">For each control in a dialog box, an extended dialog box template has a block of data that uses the [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) format to describe the control.</span></span>

<span data-ttu-id="e9f9e-107">La struttura **DLGTEMPLATEEX** non è definita in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-107">The **DLGTEMPLATEEX** structure is not defined in any standard header file.</span></span> <span data-ttu-id="e9f9e-108">La definizione della struttura è disponibile qui per spiegare il formato di un modello esteso per una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-108">The structure definition is provided here to explain the format of an extended template for a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f9e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f9e-109">Syntax</span></span>


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="e9f9e-110">Members</span><span class="sxs-lookup"><span data-stu-id="e9f9e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9f9e-111">**dlgVer**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-111">**dlgVer**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-112">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-112">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-113">Numero di versione del modello della finestra di dialogo estesa.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-113">The version number of the extended dialog box template.</span></span> <span data-ttu-id="e9f9e-114">Questo membro deve essere impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-114">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-115">**URL REST**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-115">**signature**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-116">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-117">Indica se un modello è un modello di finestra di dialogo esteso.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-117">Indicates whether a template is an extended dialog box template.</span></span> <span data-ttu-id="e9f9e-118">Se **Signature** è 0xFFFF, si tratta di un modello di finestra di dialogo esteso.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-118">If **signature** is 0xFFFF, this is an extended dialog box template.</span></span> <span data-ttu-id="e9f9e-119">In questo caso, il membro **dlgVer** specifica il numero di versione del modello.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-119">In this case, the **dlgVer** member specifies the template version number.</span></span> <span data-ttu-id="e9f9e-120">Se **Signature** è un valore diverso da 0xFFFF, si tratta di un modello di finestra di dialogo standard che usa le strutture [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) e [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="e9f9e-120">If **signature** is any value other than 0xFFFF, this is a standard dialog box template that uses the [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) and [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-121">**helpID**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-121">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-123">Identificatore del contesto della Guida per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-123">The help context identifier for the dialog box window.</span></span> <span data-ttu-id="e9f9e-124">Quando il sistema invia un messaggio della [**\_ Guida WM**](../shell/wm-help.md) , questo valore viene passato nel membro **wContextId** della struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="e9f9e-124">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes this value in the **wContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-125">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-125">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-126">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-127">Stili estesi di Windows.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-127">The extended windows styles.</span></span> <span data-ttu-id="e9f9e-128">Questo membro non viene utilizzato durante la creazione di finestre di dialogo, ma le applicazioni che utilizzano i modelli di finestra di dialogo possono utilizzarlo per creare altri tipi di finestre.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-128">This member is not used when creating dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="e9f9e-129">Per un elenco di valori, vedere [**stili finestra estesa**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="e9f9e-129">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-130">**style**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-130">**style**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-131">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-132">Stile della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-132">The style of the dialog box.</span></span> <span data-ttu-id="e9f9e-133">Questo membro può essere una combinazione di valori di [stile della finestra](/windows/desktop/winmsg/window-styles) e di valori di stile della finestra di [dialogo](dialog-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="e9f9e-133">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) and [dialog box style values](dialog-box-styles.md).</span></span>

<span data-ttu-id="e9f9e-134">Se **lo stile** include lo stile della finestra di dialogo DS **\_ sefont** o **DS \_ SHELLFONT** , l'intestazione **DLGTEMPLATEEX** del modello della finestra di dialogo estesa contiene quattro membri aggiuntivi ( **pointsize**, **Weight**, **Italic** e **Typeface**) che descrivono il tipo di carattere da utilizzare per il testo nell'area client e i controlli della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-134">If **style** includes the **DS\_SETFONT** or **DS\_SHELLFONT** dialog box style, the **DLGTEMPLATEEX** header of the extended dialog box template contains four additional members ( **pointsize**, **weight**, **italic**, and **typeface**) that describe the font to use for the text in the client area and controls of the dialog box.</span></span> <span data-ttu-id="e9f9e-135">Se possibile, il sistema crea un tipo di carattere in base ai valori specificati in questi membri.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-135">If possible, the system creates a font according to the values specified in these members.</span></span> <span data-ttu-id="e9f9e-136">Quindi, il sistema invia un messaggio di [**\_ tipo carattere di tipo WM**](/windows/desktop/winmsg/wm-setfont) alla finestra di dialogo e a ogni controllo per fornire un handle al tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-136">Then the system sends a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to the dialog box and to each control to provide a handle to the font.</span></span>

<span data-ttu-id="e9f9e-137">Per ulteriori informazioni, vedere [tipi di carattere della finestra di dialogo](about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="e9f9e-137">For more information, see [Dialog Box Fonts](about-dialog-boxes.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-138">**cDlgItems**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-138">**cDlgItems**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-139">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-140">Numero di controlli nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-140">The number of controls in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-141">**x**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-141">**x**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-142">Tipo: **short**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-142">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-143">Coordinata x, in unità della finestra di dialogo, dell'angolo superiore sinistro della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-143">The x-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-144">**y**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-144">**y**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-145">Tipo: **short**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-145">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-146">Coordinata y, in unità della finestra di dialogo, dell'angolo superiore sinistro della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-146">The y-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-147">**CX**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-147">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-148">Tipo: **short**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-148">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-149">Larghezza, in unità della finestra di dialogo, della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-149">The width, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-150">**CY**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-150">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-151">Tipo: **short**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-151">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-152">Altezza, in unità della finestra di dialogo, della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-152">The height, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-153">**menu**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-153">**menu**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-154">Tipo: **SZ \_ o \_ ORD**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-154">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-155">Matrice a lunghezza variabile di elementi a 16 bit che identifica una risorsa di menu per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-155">A variable-length array of 16-bit elements that identifies a menu resource for the dialog box.</span></span> <span data-ttu-id="e9f9e-156">Se il primo elemento di questa matrice è 0x0000, alla finestra di dialogo non è associato alcun menu e la matrice non contiene altri elementi.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-156">If the first element of this array is 0x0000, the dialog box has no menu and the array has no other elements.</span></span> <span data-ttu-id="e9f9e-157">Se il primo elemento è 0xFFFF, la matrice contiene un elemento aggiuntivo che specifica il valore ordinale di una risorsa di menu in un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-157">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a menu resource in an executable file.</span></span> <span data-ttu-id="e9f9e-158">Se il primo elemento ha un altro valore, il sistema considera la matrice come una stringa Unicode con terminazione null che specifica il nome di una risorsa di menu in un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-158">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a menu resource in an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-159">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-159">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-160">Tipo: **SZ \_ o \_ ORD**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-160">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-161">Matrice a lunghezza variabile di elementi a 16 bit che identifica la classe della finestra della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-161">A variable-length array of 16-bit elements that identifies the window class of the dialog box.</span></span> <span data-ttu-id="e9f9e-162">Se il primo elemento della matrice è 0x0000, il sistema utilizza la classe della finestra di dialogo predefinita per la finestra di dialogo e la matrice non contiene altri elementi.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-162">If the first element of the array is 0x0000, the system uses the predefined dialog box class for the dialog box and the array has no other elements.</span></span> <span data-ttu-id="e9f9e-163">Se il primo elemento è 0xFFFF, la matrice contiene un elemento aggiuntivo che specifica il valore ordinale di una classe di finestra di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-163">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system window class.</span></span> <span data-ttu-id="e9f9e-164">Se il primo elemento ha un altro valore, il sistema considera la matrice come una stringa Unicode con terminazione null che specifica il nome di una classe di finestre registrate.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-164">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-165">**title**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-165">**title**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-166">Tipo: **WCHAR \[ titleLen \]**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-166">Type: **WCHAR\[titleLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-167">Titolo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-167">The title of the dialog box.</span></span> <span data-ttu-id="e9f9e-168">Se il primo elemento di questa matrice è 0x0000, la finestra di dialogo non ha alcun titolo e la matrice non contiene altri elementi.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-168">If the first element of this array is 0x0000, the dialog box has no title and the array has no other elements.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-169">**pointsize**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-169">**pointsize**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-170">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-170">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-171">Dimensioni in punti del tipo di carattere da utilizzare per il testo nella finestra di dialogo e i relativi controlli.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-171">The point size of the font to use for the text in the dialog box and its controls.</span></span>

<span data-ttu-id="e9f9e-172">Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-172">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-173">**weight**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-173">**weight**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-174">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-174">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-175">Spessore del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-175">The weight of the font.</span></span> <span data-ttu-id="e9f9e-176">Si noti che, anche se può essere uno qualsiasi dei valori elencati per il membro **lfWeight** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , qualsiasi valore usato verrà automaticamente modificato in **FW \_ Normal**.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-176">Note that, although this can be any of the values listed for the **lfWeight** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure, any value that is used will be automatically changed to **FW\_NORMAL**.</span></span>

<span data-ttu-id="e9f9e-177">Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-177">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-178">**corsivo**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-178">**italic**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-179">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-179">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-180">Indica se il tipo di carattere è in corsivo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-180">Indicates whether the font is italic.</span></span> <span data-ttu-id="e9f9e-181">Se questo valore è **true**, il tipo di carattere è in corsivo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-181">If this value is **TRUE**, the font is italic.</span></span>

<span data-ttu-id="e9f9e-182">Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-182">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-183">**charset**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-183">**charset**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-184">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-184">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-185">Set di caratteri da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-185">The character set to be used.</span></span> <span data-ttu-id="e9f9e-186">Per ulteriori informazioni, vedere il membro **lfCharSet** di [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span><span class="sxs-lookup"><span data-stu-id="e9f9e-186">For more information, see the **lfcharset** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span></span>

<span data-ttu-id="e9f9e-187">Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-187">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="e9f9e-188">**carattere tipografico**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-188">**typeface**</span></span>
</dt> <dd>

<span data-ttu-id="e9f9e-189">Tipo: **WCHAR \[ stringLen \]**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-189">Type: **WCHAR\[stringLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="e9f9e-190">Nome del carattere tipografico per il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-190">The name of the typeface for the font.</span></span>

<span data-ttu-id="e9f9e-191">Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-191">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9f9e-192">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9f9e-192">Remarks</span></span>

<span data-ttu-id="e9f9e-193">È possibile utilizzare un modello di finestra di dialogo esteso anziché un modello di finestra di dialogo standard nelle funzioni [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)e [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .</span><span class="sxs-lookup"><span data-stu-id="e9f9e-193">You can use an extended dialog box template instead of a standard dialog box template in the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta), and [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) functions.</span></span>

<span data-ttu-id="e9f9e-194">La seguente intestazione **DLGTEMPLATEEX** in un modello di finestra di dialogo esteso è costituita da una o più strutture [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) che descrivono i controlli della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-194">Following the **DLGTEMPLATEEX** header in an extended dialog box template is one or more [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structures that describe the controls of the dialog box.</span></span> <span data-ttu-id="e9f9e-195">Il membro **cDlgItems** della struttura **DLGITEMTEMPLATEEX** specifica il numero di strutture **DLGITEMTEMPLATEEX** che seguono nel modello.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-195">The **cDlgItems** member of the **DLGITEMTEMPLATEEX** structure specifies the number of **DLGITEMTEMPLATEEX** structures that follow in the template.</span></span>

<span data-ttu-id="e9f9e-196">Ogni struttura [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) del modello deve essere allineata in un limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e9f9e-196">Each [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structure in the template must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="e9f9e-197">Se il membro dello **stile** specifica lo stile DS **\_ sefont** o **DS \_ SHELLFONT** , la prima struttura **DLGITEMTEMPLATEEX** inizia sul primo limite **DWORD** dopo la stringa del **carattere tipografico** .</span><span class="sxs-lookup"><span data-stu-id="e9f9e-197">If the **style** member specifies the **DS\_SETFONT** or **DS\_SHELLFONT** style, the first **DLGITEMTEMPLATEEX** structure begins on the first **DWORD** boundary after the **typeface** string.</span></span> <span data-ttu-id="e9f9e-198">Se questi stili non vengono specificati, la prima struttura inizia sul primo limite **DWORD** dopo la stringa del **titolo** .</span><span class="sxs-lookup"><span data-stu-id="e9f9e-198">If these styles are not specified, the first structure begins on the first **DWORD** boundary after the **title** string.</span></span>

<span data-ttu-id="e9f9e-199">Le matrici **menu**, **WindowClass**, **title** e **Typeface** devono essere allineate sui limiti di **parola** .</span><span class="sxs-lookup"><span data-stu-id="e9f9e-199">The **menu**, **windowClass**, **title**, and **typeface** arrays must be aligned on **WORD** boundaries.</span></span>

<span data-ttu-id="e9f9e-200">Se si specificano stringhe di caratteri nelle matrici **menu**, **WindowClass**, **title** e **Typeface** , è necessario utilizzare stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-200">If you specify character strings in the **menu**, **windowClass**, **title**, and **typeface** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="e9f9e-201">Utilizzare la funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) per generare queste stringhe Unicode dalle stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-201">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="e9f9e-202">I membri **x**, **y**, **CX** e **CY** specificano i valori nelle unità della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e9f9e-202">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="e9f9e-203">È possibile convertire questi valori in unità schermo (pixel) utilizzando la funzione [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="e9f9e-203">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f9e-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f9e-204">Requirements</span></span>



| <span data-ttu-id="e9f9e-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f9e-205">Requirement</span></span> | <span data-ttu-id="e9f9e-206">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f9e-206">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e9f9e-207">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f9e-207">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f9e-208">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9f9e-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e9f9e-209">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f9e-209">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f9e-210">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9f9e-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e9f9e-211">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f9e-211">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9f9e-212">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-212">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9f9e-213">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-213">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="e9f9e-214">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-214">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="e9f9e-215">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-215">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="e9f9e-216">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-216">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="e9f9e-217">**DLGITEMTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-217">**DLGITEMTEMPLATEEX**</span></span>](dlgitemtemplateex.md)
</dt> <dt>

[<span data-ttu-id="e9f9e-218">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-218">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="e9f9e-219">**\_tipo di carattere WM**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-219">**WM\_SETFONT**</span></span>](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

<span data-ttu-id="e9f9e-220">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e9f9e-221">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="e9f9e-221">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="e9f9e-222">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-222">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e9f9e-223">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-223">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="e9f9e-224">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="e9f9e-224">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

