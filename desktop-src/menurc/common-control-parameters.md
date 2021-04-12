---
title: Parametri di controllo comuni
description: Di seguito viene descritta la sintassi generale per un'istruzione di definizione delle risorse del controllo.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337182"
---
# <a name="common-control-parameters"></a><span data-ttu-id="bd972-103">Parametri di controllo comuni</span><span class="sxs-lookup"><span data-stu-id="bd972-103">Common Control Parameters</span></span>

<span data-ttu-id="bd972-104">Di seguito viene descritta la sintassi generale per un'istruzione di definizione delle risorse del controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-104">The following describes the general syntax for a control resource-definition statement.</span></span> <span data-ttu-id="bd972-105">Il significato di ogni parametro è riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="bd972-105">The meaning of each parameter is given below.</span></span> <span data-ttu-id="bd972-106">Occasionalmente, un'istruzione utilizzerà un parametro in modo diverso o potrebbe ignorare un parametro.</span><span class="sxs-lookup"><span data-stu-id="bd972-106">Occasionally, a statement will use a parameter differently, or may ignore a parameter.</span></span> <span data-ttu-id="bd972-107">La variazione specifica dell'istruzione è descritta nella documentazione relativa all'istruzione.</span><span class="sxs-lookup"><span data-stu-id="bd972-107">The statement-specific variation is described in the documentation for the statement.</span></span>

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span data-ttu-id="bd972-108"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="bd972-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-109">Testo da visualizzare con il controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-109">Text that is to be displayed with the control.</span></span> <span data-ttu-id="bd972-110">Il testo è posizionato all'interno del controllo o accanto al controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-110">The text is positioned within the control or adjacent to the control.</span></span>

<span data-ttu-id="bd972-111">Questo parametro deve contenere zero o più caratteri racchiusi tra virgolette doppie (").</span><span class="sxs-lookup"><span data-stu-id="bd972-111">This parameter must contain zero or more characters enclosed in double quotation marks (").</span></span> <span data-ttu-id="bd972-112">Le stringhe vengono terminate automaticamente con terminazione null e convertite in Unicode nel file di risorse risultante.</span><span class="sxs-lookup"><span data-stu-id="bd972-112">Strings are automatically null-terminated and converted to Unicode in the resulting resource file.</span></span>

<span data-ttu-id="bd972-113">Per impostazione predefinita, i caratteri elencati tra virgolette doppie sono caratteri ANSI e le sequenze di escape vengono interpretate come sequenze di escape di byte.</span><span class="sxs-lookup"><span data-stu-id="bd972-113">By default, the characters listed between the double quotation marks are ANSI characters, and escape sequences are interpreted as byte escape sequences.</span></span> <span data-ttu-id="bd972-114">Se la stringa è preceduta dal prefisso "L", la stringa è una stringa di caratteri wide e le sequenze di escape vengono interpretate come sequenze di escape da 2 byte che specificano caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="bd972-114">If the string is preceded by the "L" prefix, the string is a wide-character string and escape sequences are interpreted as 2-byte escape sequences that specify Unicode characters.</span></span> <span data-ttu-id="bd972-115">Se nel testo è richiesta una virgoletta doppia, è necessario includere due volte il segno di virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="bd972-115">If a double quotation mark is required in the text, you must include the double quotation mark twice.</span></span>

<span data-ttu-id="bd972-116">Un carattere e commerciale (&) nel testo indica che il carattere seguente viene usato come carattere mnemonico per il controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-116">An ampersand (&) character in the text indicates that the following character is used as a mnemonic character for the control.</span></span> <span data-ttu-id="bd972-117">Quando il controllo viene visualizzato, la e commerciale non viene visualizzata, ma il carattere mnemonico è sottolineato.</span><span class="sxs-lookup"><span data-stu-id="bd972-117">When the control is displayed, the ampersand is not shown, but the mnemonic character is underlined.</span></span> <span data-ttu-id="bd972-118">L'utente può scegliere il controllo premendo il tasto corrispondente al carattere mnemonico sottolineato.</span><span class="sxs-lookup"><span data-stu-id="bd972-118">The user can choose the control by pressing the key corresponding to the underlined mnemonic character.</span></span> <span data-ttu-id="bd972-119">Per utilizzare la e commerciale come carattere in una stringa, inserire due e commerciale (&&).</span><span class="sxs-lookup"><span data-stu-id="bd972-119">To use the ampersand as a character in a string, insert two ampersands (&&).</span></span>

</dd> <dt>

<span data-ttu-id="bd972-120"><span id="id"></span><span id="ID"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="bd972-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-121">Identificatore del controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-121">Control identifier.</span></span> <span data-ttu-id="bd972-122">Questo valore deve essere un Unsigned Integer a 16 bit nell'intervallo compreso tra 0 e 65.535 oppure una semplice espressione aritmetica che restituisce un valore in tale intervallo.</span><span class="sxs-lookup"><span data-stu-id="bd972-122">This value must be a 16-bit unsigned integer in the range 0 through 65,535 or a simple arithmetic expression that evaluates to a value in that range.</span></span>

</dd> <dt>

<span data-ttu-id="bd972-123"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="bd972-123"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-124">Coordinata X del lato sinistro del controllo rispetto al lato sinistro della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bd972-124">X-coordinate of the left side of the control relative to the left side of the dialog box.</span></span> <span data-ttu-id="bd972-125">Questo valore deve essere un Unsigned Integer a 16 bit nell'intervallo compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="bd972-125">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="bd972-126">La coordinata si trova in unità di dialogo ed è relativa all'origine della finestra di dialogo, della finestra o del controllo contenente il controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="bd972-126">The coordinate is in dialog units and is relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="bd972-127"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="bd972-127"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-128">Coordinata Y del lato superiore del controllo rispetto alla parte superiore della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bd972-128">Y-coordinate of the top side of the control relative to the top of the dialog box.</span></span> <span data-ttu-id="bd972-129">Questo valore deve essere un Unsigned Integer a 16 bit nell'intervallo compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="bd972-129">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="bd972-130">La coordinata è espressa in unità di dialogo relative all'origine della finestra di dialogo, della finestra o del controllo contenente il controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="bd972-130">The coordinate is in dialog units relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="bd972-131"><span id="width"></span><span id="WIDTH"></span>*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="bd972-131"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-132">Larghezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-132">Width of the control.</span></span> <span data-ttu-id="bd972-133">Questo valore deve essere un Unsigned Integer a 16 bit compreso nell'intervallo da 1 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="bd972-133">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="bd972-134">La larghezza è in unità da 1 a 4 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bd972-134">The width is in 1/4-character units.</span></span>

</dd> <dt>

<span data-ttu-id="bd972-135"><span id="height"></span><span id="HEIGHT"></span>*altezza*</span><span class="sxs-lookup"><span data-stu-id="bd972-135"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-136">Altezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-136">Height of the control.</span></span> <span data-ttu-id="bd972-137">Questo valore deve essere un Unsigned Integer a 16 bit compreso nell'intervallo da 1 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="bd972-137">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="bd972-138">L'altezza è in unità di 1/8 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bd972-138">The height is in 1/8-character units.</span></span>

</dd> <dt>

<span data-ttu-id="bd972-139"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="bd972-139"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-140">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-140">Control styles.</span></span> <span data-ttu-id="bd972-141">Utilizzare l'operatore OR bit \| per bit () per combinare gli stili.</span><span class="sxs-lookup"><span data-stu-id="bd972-141">Use the bitwise OR (\|) operator to combine styles.</span></span> <span data-ttu-id="bd972-142">Per altre informazioni, vedere [stili di finestra](../winmsg/window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="bd972-142">For more information, see [Window Styles](../winmsg/window-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd972-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*stile esteso*</span><span class="sxs-lookup"><span data-stu-id="bd972-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-144">Stili estesi della finestra.</span><span class="sxs-lookup"><span data-stu-id="bd972-144">Extended window styles.</span></span> <span data-ttu-id="bd972-145">È necessario specificare *lo stile* per specificare il *tipo esteso*.</span><span class="sxs-lookup"><span data-stu-id="bd972-145">You must specify *style* to specify *extended-style*.</span></span> <span data-ttu-id="bd972-146">Per ulteriori informazioni, vedere [**ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="bd972-146">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd972-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span><span class="sxs-lookup"><span data-stu-id="bd972-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-148">Espressione numerica che indica l'ID utilizzato per identificare il controllo durante l'elaborazione della [**\_ Guida WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="bd972-148">Numeric expression indicating the ID used to identify the control during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="bd972-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span><span class="sxs-lookup"><span data-stu-id="bd972-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span></span>
</dt> <dd>

<span data-ttu-id="bd972-150">Dati specifici del controllo per il controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-150">Control-specific data for the control.</span></span> <span data-ttu-id="bd972-151">Quando viene creata una finestra di dialogo e viene creato un controllo in tale finestra di dialogo con dati specifici del controllo, viene passato un puntatore a tali dati nella routine della finestra del controllo tramite il valore *lParam* del messaggio [**WM \_ create**](../winmsg/wm-create.md) per il controllo.</span><span class="sxs-lookup"><span data-stu-id="bd972-151">When a dialog is created, and a control in that dialog which has control-specific data is created, a pointer to that data is passed into the control's window procedure through the *lParam* of the [**WM\_CREATE**](../winmsg/wm-create.md) message for that control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd972-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd972-152">Remarks</span></span>

<span data-ttu-id="bd972-153">Le unità di dialogo orizzontali sono 1/4 dell'unità della larghezza di base della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bd972-153">Horizontal dialog units are 1/4 of the dialog base width unit.</span></span> <span data-ttu-id="bd972-154">Le unità verticali sono 1/8 dell'unità di altezza di base della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bd972-154">Vertical units are 1/8 of the dialog base height unit.</span></span> <span data-ttu-id="bd972-155">Le unità di base della finestra di dialogo correnti vengono calcolate in base all'altezza e alla larghezza del tipo di carattere del sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="bd972-155">The current dialog base units are computed from the height and width of the current system font.</span></span> <span data-ttu-id="bd972-156">La funzione [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) restituisce le unità di base della finestra di dialogo in pixel.</span><span class="sxs-lookup"><span data-stu-id="bd972-156">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="bd972-157">Le coordinate sono relative all'origine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bd972-157">The coordinates are relative to the origin of the dialog box.</span></span>

 

 