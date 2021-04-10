---
title: Istruzione CLASS
description: Definisce la classe della finestra di dialogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menu di istruzioni di classe e altre risorse
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963016"
---
# <a name="class-statement"></a><span data-ttu-id="4db3c-104">Istruzione CLASS</span><span class="sxs-lookup"><span data-stu-id="4db3c-104">CLASS statement</span></span>

<span data-ttu-id="4db3c-105">Definisce la classe della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4db3c-105">Defines the class of the dialog box.</span></span>

<span data-ttu-id="4db3c-106">L'istruzione **Class** viene visualizzata nella sezione facoltativa prima del principale di un'istruzione della [**finestra di dialogo**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="4db3c-106">The **CLASS** statement appears in the optional section before a [**DIALOG**](dialog-resource.md) statement's main.</span></span> <span data-ttu-id="4db3c-107">Se non viene specificata alcuna classe, viene usata la classe della finestra di dialogo standard.</span><span class="sxs-lookup"><span data-stu-id="4db3c-107">If no class is given, the standard dialog class is used.</span></span>

``` syntax
CLASS class
```

<dl> <dt>

<span data-ttu-id="4db3c-108"><span id="class"></span><span id="CLASS"></span>*classe*</span><span class="sxs-lookup"><span data-stu-id="4db3c-108"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="4db3c-109">Unsigned Integer a 16 bit o una stringa racchiusa tra virgolette doppie ("), che identifica la classe della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4db3c-109">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="4db3c-110">Se la routine della finestra per la classe non elabora un messaggio inviato, deve chiamare la funzione [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) per garantire che tutti i messaggi vengano gestiti correttamente per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4db3c-110">If the window procedure for the class does not process a message sent to it, it must call the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function to ensure that all messages are handled properly for the dialog box.</span></span> <span data-ttu-id="4db3c-111">Una classe privata può utilizzare **DefDlgProc** come routine della finestra predefinita.</span><span class="sxs-lookup"><span data-stu-id="4db3c-111">A private class can use **DefDlgProc** as the default window procedure.</span></span> <span data-ttu-id="4db3c-112">La classe deve essere registrata con il membro **cbWndExtra** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) impostata su **DLGWINDOWEXTRA**.</span><span class="sxs-lookup"><span data-stu-id="4db3c-112">The class must be registered with the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure set to **DLGWINDOWEXTRA**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4db3c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4db3c-113">Remarks</span></span>

<span data-ttu-id="4db3c-114">L'istruzione di **classe** deve essere utilizzata solo con casi particolari, perché esegue l'override della normale elaborazione di una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4db3c-114">The **CLASS** statement should only be used with special cases, because it overrides the normal processing of a dialog box.</span></span> <span data-ttu-id="4db3c-115">L'istruzione **Class** converte una finestra di dialogo in una finestra della classe specificata. a seconda della classe, questo può restituire risultati non desiderati.</span><span class="sxs-lookup"><span data-stu-id="4db3c-115">The **CLASS** statement converts a dialog box to a window of the specified class; depending on the class, this could give undesirable results.</span></span> <span data-ttu-id="4db3c-116">Non usare i nomi di classe di controllo ridefiniti con questa istruzione.</span><span class="sxs-lookup"><span data-stu-id="4db3c-116">Do not use the redefined control-class names with this statement.</span></span>

## <a name="examples"></a><span data-ttu-id="4db3c-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="4db3c-117">Examples</span></span>

<span data-ttu-id="4db3c-118">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **Class** :</span><span class="sxs-lookup"><span data-stu-id="4db3c-118">The following example demonstrates the use of the **CLASS** statement:</span></span>

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a><span data-ttu-id="4db3c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4db3c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db3c-120">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="4db3c-120">**DefDlgProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="4db3c-121">**DIALOGO**</span><span class="sxs-lookup"><span data-stu-id="4db3c-121">**DIALOG**</span></span>](dialog-resource.md)
</dt> </dl>

 

 