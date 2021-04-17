---
title: Risorsa ACCELERAtori
description: Definisce uno o più acceleratori per un'applicazione. Un acceleratore è una sequenza di tasti definita dall'applicazione per fornire all'utente un modo rapido per eseguire un'attività.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menu risorse ACCELERAtori e altre risorse
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516750"
---
# <a name="accelerators-resource"></a><span data-ttu-id="3beaa-105">Risorsa ACCELERAtori</span><span class="sxs-lookup"><span data-stu-id="3beaa-105">ACCELERATORS resource</span></span>

<span data-ttu-id="3beaa-106">Definisce uno o più acceleratori per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3beaa-106">Defines one or more accelerators for an application.</span></span> <span data-ttu-id="3beaa-107">Un acceleratore è una sequenza di tasti definita dall'applicazione per fornire all'utente un modo rapido per eseguire un'attività.</span><span class="sxs-lookup"><span data-stu-id="3beaa-107">An accelerator is a keystroke defined by the application to give the user a quick way to perform a task.</span></span>

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a><span data-ttu-id="3beaa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3beaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3beaa-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span><span class="sxs-lookup"><span data-stu-id="3beaa-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span></span>
</dt> <dd>

<span data-ttu-id="3beaa-110">Nome univoco o valore Unsigned Integer a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3beaa-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3beaa-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*</span><span class="sxs-lookup"><span data-stu-id="3beaa-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="3beaa-112">Zero o più delle istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3beaa-112">Zero or more of the following statements.</span></span>



| <span data-ttu-id="3beaa-113">Istruzione</span><span class="sxs-lookup"><span data-stu-id="3beaa-113">Statement</span></span>                                                        | <span data-ttu-id="3beaa-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3beaa-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3beaa-115">[**Caratteristiche**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="3beaa-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="3beaa-116">Informazioni definite dall'utente su una risorsa che possono essere usate da strumenti per la lettura e la scrittura di file di risorse.</span><span class="sxs-lookup"><span data-stu-id="3beaa-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="3beaa-117">Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="3beaa-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="3beaa-118">[](language-statement.md) *Lingua* lingua, *lingua*</span><span class="sxs-lookup"><span data-stu-id="3beaa-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="3beaa-119">Specifica la lingua per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3beaa-119">Specifies the language for the resource.</span></span> <span data-ttu-id="3beaa-120">Per ulteriori informazioni, vedere [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="3beaa-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="3beaa-121">[](version-statement.md) *DWORD* versione</span><span class="sxs-lookup"><span data-stu-id="3beaa-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="3beaa-122">Numero di versione definito dall'utente per la risorsa che può essere usato da strumenti che leggono e scrivono file di risorse.</span><span class="sxs-lookup"><span data-stu-id="3beaa-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="3beaa-123">Per ulteriori informazioni, vedere [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="3beaa-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="3beaa-124"><span id="event"></span><span id="EVENT"></span>*evento*</span><span class="sxs-lookup"><span data-stu-id="3beaa-124"><span id="event"></span><span id="EVENT"></span>*event*</span></span>
</dt> <dd>

<span data-ttu-id="3beaa-125">Sequenza di tasti da utilizzare come tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3beaa-125">Keystroke to be used as an accelerator.</span></span> <span data-ttu-id="3beaa-126">Può essere uno dei tipi di carattere seguenti.</span><span class="sxs-lookup"><span data-stu-id="3beaa-126">It can be any one of the following character types.</span></span>



| <span data-ttu-id="3beaa-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="3beaa-127">Type</span></span>                    | <span data-ttu-id="3beaa-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3beaa-128">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3beaa-129">"*char*"</span><span class="sxs-lookup"><span data-stu-id="3beaa-129">"*char*"</span></span>                | <span data-ttu-id="3beaa-130">Carattere singolo racchiuso tra virgolette doppie (").</span><span class="sxs-lookup"><span data-stu-id="3beaa-130">A single character enclosed in double quotation marks (").</span></span> <span data-ttu-id="3beaa-131">Il carattere può essere preceduto da un accento circonflesso (^), vale a dire che il carattere è un carattere di controllo.</span><span class="sxs-lookup"><span data-stu-id="3beaa-131">The character can be preceded by a caret (^), meaning that the character is a control character.</span></span>                                                                                  |
| <span data-ttu-id="3beaa-132">*Carattere*</span><span class="sxs-lookup"><span data-stu-id="3beaa-132">*Character*</span></span>             | <span data-ttu-id="3beaa-133">Valore integer che rappresenta un carattere.</span><span class="sxs-lookup"><span data-stu-id="3beaa-133">An integer value representing a character.</span></span> <span data-ttu-id="3beaa-134">Il parametro di *tipo* deve essere **ASCII**.</span><span class="sxs-lookup"><span data-stu-id="3beaa-134">The *type* parameter must be **ASCII**.</span></span>                                                                                                                                                           |
| <span data-ttu-id="3beaa-135">*carattere chiave virtuale*</span><span class="sxs-lookup"><span data-stu-id="3beaa-135">*virtual-key character*</span></span> | <span data-ttu-id="3beaa-136">Valore integer che rappresenta una chiave virtuale.</span><span class="sxs-lookup"><span data-stu-id="3beaa-136">An integer value representing a virtual key.</span></span> <span data-ttu-id="3beaa-137">È possibile specificare la chiave virtuale per le chiavi alfanumeriche inserendo la lettera o il numero maiuscolo tra virgolette doppie (ad esempio, "9" o "C").</span><span class="sxs-lookup"><span data-stu-id="3beaa-137">The virtual key for alphanumeric keys can be specified by placing the uppercase letter or number in double quotation marks (for example, "9" or "C").</span></span> <span data-ttu-id="3beaa-138">Il parametro di *tipo* deve essere **VIRTKEY**.</span><span class="sxs-lookup"><span data-stu-id="3beaa-138">The *type* parameter must be **VIRTKEY**.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3beaa-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idValue*</span><span class="sxs-lookup"><span data-stu-id="3beaa-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span></span>
</dt> <dd>

<span data-ttu-id="3beaa-140">valore Unsigned Integer a 16 bit che identifica il tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3beaa-140">a 16-bit unsigned integer value that identifies the accelerator.</span></span>

</dd> <dt>

<span data-ttu-id="3beaa-141"><span id="type"></span><span id="TYPE"></span>*tipo*</span><span class="sxs-lookup"><span data-stu-id="3beaa-141"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="3beaa-142">Obbligatorio solo quando il parametro dell' *evento* è un *carattere o un* carattere di *chiave virtuale*.</span><span class="sxs-lookup"><span data-stu-id="3beaa-142">Required only when the *event* parameter is a *character* or a *virtual-key character*.</span></span> <span data-ttu-id="3beaa-143">Il parametro di *tipo* specifica **ASCII** o **VIRTKEY**; il valore integer dell' *evento* viene interpretato di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="3beaa-143">The *type* parameter specifies either **ASCII** or **VIRTKEY**; the integer value of *event* is interpreted accordingly.</span></span> <span data-ttu-id="3beaa-144">Quando si specifica **VIRTKEY** e l' *evento* contiene una stringa, l' *evento* deve essere in maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="3beaa-144">When **VIRTKEY** is specified and *event* contains a string, *event* must be uppercase.</span></span>

</dd> <dt>

<span data-ttu-id="3beaa-145"><span id="options"></span><span id="OPTIONS"></span>*Opzioni*</span><span class="sxs-lookup"><span data-stu-id="3beaa-145"><span id="options"></span><span id="OPTIONS"></span>*options*</span></span>
</dt> <dd>

<span data-ttu-id="3beaa-146">opzioni che definiscono il tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3beaa-146">options that define the accelerator.</span></span> <span data-ttu-id="3beaa-147">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3beaa-147">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3beaa-148">Opzione</span><span class="sxs-lookup"><span data-stu-id="3beaa-148">Option</span></span>                             | <span data-ttu-id="3beaa-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3beaa-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3beaa-150">**Noinverte**</span><span class="sxs-lookup"><span data-stu-id="3beaa-150">**NOINVERT**</span></span>                       | <span data-ttu-id="3beaa-151">Specifica che non viene evidenziata alcuna voce di menu di primo livello quando si usa l'acceleratore.</span><span class="sxs-lookup"><span data-stu-id="3beaa-151">Specifies that no top-level menu item is highlighted when the accelerator is used.</span></span> <span data-ttu-id="3beaa-152">Questa operazione è utile quando si definiscono acceleratori per azioni quali lo scorrimento che non corrispondono a una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="3beaa-152">This is useful when defining accelerators for actions such as scrolling that do not correspond to a menu item.</span></span> <span data-ttu-id="3beaa-153">Se si omette **NOinverted** , una voce di menu di primo livello verrà evidenziata (se possibile) quando si utilizza l'acceleratore.</span><span class="sxs-lookup"><span data-stu-id="3beaa-153">If **NOINVERT** is omitted, a top-level menu item will be highlighted (if possible) when the accelerator is used.</span></span> <span data-ttu-id="3beaa-154">Questo attributo è obsoleto e viene mantenuto solo per compatibilità con le versioni precedenti dei file di risorse progettati per Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3beaa-154">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span> |
| <span data-ttu-id="3beaa-155">**ALT**</span><span class="sxs-lookup"><span data-stu-id="3beaa-155">**ALT**</span></span>                            | <span data-ttu-id="3beaa-156">Determina l'attivazione del tasto di scelta rapida solo se il tasto ALT è premuto.</span><span class="sxs-lookup"><span data-stu-id="3beaa-156">Causes the accelerator to be activated only if the ALT key is down.</span></span> <span data-ttu-id="3beaa-157">Si applica solo alle chiavi virtuali.</span><span class="sxs-lookup"><span data-stu-id="3beaa-157">Applies only to virtual keys.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3beaa-158">**MAIUSC**</span><span class="sxs-lookup"><span data-stu-id="3beaa-158">**SHIFT**</span></span>                          | <span data-ttu-id="3beaa-159">Determina l'attivazione dell'acceleratore solo se il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="3beaa-159">Causes the accelerator to be activated only if the SHIFT key is down.</span></span> <span data-ttu-id="3beaa-160">Si applica solo alle chiavi virtuali</span><span class="sxs-lookup"><span data-stu-id="3beaa-160">Applies only to virtual keys</span></span>                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3beaa-161">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="3beaa-161">**CONTROL**</span></span>](control-control.md) | <span data-ttu-id="3beaa-162">Definisce il carattere come carattere di controllo. l'acceleratore viene attivato solo se la chiave del controllo è inattiva.</span><span class="sxs-lookup"><span data-stu-id="3beaa-162">Defines the character as a control character (the accelerator is only activated if the CONTROL key is down).</span></span> <span data-ttu-id="3beaa-163">Questa operazione ha lo stesso effetto dell'uso di un accento circonflesso (^) prima del carattere di accelerazione nel parametro dell' *evento* .</span><span class="sxs-lookup"><span data-stu-id="3beaa-163">This has the same effect as using a caret (^) before the accelerator character in the *event* parameter.</span></span> <span data-ttu-id="3beaa-164">Si applica solo alle chiavi virtuali</span><span class="sxs-lookup"><span data-stu-id="3beaa-164">Applies only to virtual keys</span></span>                                                                                                                                                                                           |



 

</dd> </dl>

<span data-ttu-id="3beaa-165">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="3beaa-165">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3beaa-166">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3beaa-166">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3beaa-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="3beaa-167">Remarks</span></span>

<span data-ttu-id="3beaa-168">La funzione [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) viene usata per convertire i messaggi acceleratore dalla coda dell'applicazione in messaggi [**WM \_ Command**](./wm-command.md) o [**WM \_ SYSCOMMAND**](./wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="3beaa-168">The [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function is used to translate accelerator messages from the application queue into [**WM\_COMMAND**](./wm-command.md) or [**WM\_SYSCOMMAND**](./wm-syscommand.md) messages.</span></span>

## <a name="examples"></a><span data-ttu-id="3beaa-169">Esempio</span><span class="sxs-lookup"><span data-stu-id="3beaa-169">Examples</span></span>

<span data-ttu-id="3beaa-170">Nell'esempio seguente viene illustrato l'utilizzo dei tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3beaa-170">The following example demonstrates the use of accelerator keys.</span></span>

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a><span data-ttu-id="3beaa-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3beaa-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3beaa-172">Uso di tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="3beaa-172">Using Keyboard Accelerators</span></span>](./using-keyboard-accelerators.md)
</dt> <dt>

[<span data-ttu-id="3beaa-173">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="3beaa-173">**TranslateAccelerator**</span></span>](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="3beaa-174">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="3beaa-174">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="3beaa-175">**DIALOGO**</span><span class="sxs-lookup"><span data-stu-id="3beaa-175">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="3beaa-176">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="3beaa-176">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="3beaa-177">**MENU**</span><span class="sxs-lookup"><span data-stu-id="3beaa-177">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="3beaa-178">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="3beaa-178">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="3beaa-179">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="3beaa-179">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="3beaa-180">**Versione**</span><span class="sxs-lookup"><span data-stu-id="3beaa-180">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 