---
title: Conformità RIGOROSa
description: Alcuni codici sorgente compilati correttamente potrebbero generare messaggi di errore quando si Abilita il controllo del tipo STRICT.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399288"
---
# <a name="strict-compliance"></a><span data-ttu-id="d37bb-103">Conformità RIGOROSa</span><span class="sxs-lookup"><span data-stu-id="d37bb-103">STRICT Compliance</span></span>

<span data-ttu-id="d37bb-104">Alcuni codici sorgente compilati correttamente potrebbero generare messaggi di errore quando si Abilita il controllo del tipo **strict** .</span><span class="sxs-lookup"><span data-stu-id="d37bb-104">Some source code that compiles successfully might produce error messages when you enable **STRICT** type checking.</span></span> <span data-ttu-id="d37bb-105">Le sezioni seguenti descrivono i requisiti minimi per la compilazione del codice quando è abilitata la funzionalità **strict** .</span><span class="sxs-lookup"><span data-stu-id="d37bb-105">The following sections describe the minimal requirements for making your code compile when **STRICT** is enabled.</span></span> <span data-ttu-id="d37bb-106">Sono consigliate procedure aggiuntive, in particolare per produrre codice portabile.</span><span class="sxs-lookup"><span data-stu-id="d37bb-106">Additional steps are recommended, especially to produce portable code.</span></span>

## <a name="general-requirements"></a><span data-ttu-id="d37bb-107">Requisiti generali</span><span class="sxs-lookup"><span data-stu-id="d37bb-107">General Requirements</span></span>

<span data-ttu-id="d37bb-108">Il requisito principale è che è necessario dichiarare i tipi di handle corretti e i puntatori a funzione anziché basarsi su tipi più generali.</span><span class="sxs-lookup"><span data-stu-id="d37bb-108">The principal requirement is that you must declare correct handle types and function pointers instead of relying on more general types.</span></span> <span data-ttu-id="d37bb-109">Non è possibile usare un tipo di handle dove ne è previsto un altro.</span><span class="sxs-lookup"><span data-stu-id="d37bb-109">You cannot use one handle type where another is expected.</span></span> <span data-ttu-id="d37bb-110">Ciò significa anche che potrebbe essere necessario modificare le dichiarazioni di funzione e utilizzare più cast di tipo.</span><span class="sxs-lookup"><span data-stu-id="d37bb-110">This also means that you may have to change function declarations and use more type casts.</span></span>

<span data-ttu-id="d37bb-111">Per ottenere risultati ottimali, è consigliabile utilizzare il tipo di **handle** generico solo quando necessario.</span><span class="sxs-lookup"><span data-stu-id="d37bb-111">For best results, the generic **HANDLE** type should be used only when necessary.</span></span>

## <a name="declaring-functions-within-your-application"></a><span data-ttu-id="d37bb-112">Dichiarazione di funzioni all'interno dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d37bb-112">Declaring Functions Within Your Application</span></span>

<span data-ttu-id="d37bb-113">Verificare che tutte le funzioni dell'applicazione siano dichiarate.</span><span class="sxs-lookup"><span data-stu-id="d37bb-113">Make sure all application functions are declared.</span></span> <span data-ttu-id="d37bb-114">L'inserimento di tutte le dichiarazioni di funzione in un file di inclusione è consigliato perché è possibile analizzare facilmente le dichiarazioni e cercare i tipi di parametro e restituiti che devono essere modificati.</span><span class="sxs-lookup"><span data-stu-id="d37bb-114">Placing all function declarations in an include file is recommended because you can easily scan your declarations and look for parameter and return types that should be changed.</span></span>

<span data-ttu-id="d37bb-115">Se si usa l'opzione del compilatore **/ZG** per creare i file di intestazione per le funzioni, tenere presente che si otterranno risultati diversi a seconda che sia stato abilitato il controllo del tipo **strict** .</span><span class="sxs-lookup"><span data-stu-id="d37bb-115">If you use the **/Zg** compiler option to create header files for your functions, remember that you will get different results depending on whether you have enabled **STRICT** type checking.</span></span> <span data-ttu-id="d37bb-116">Con **strict** disabled, tutti i tipi di handle generano lo stesso tipo di base.</span><span class="sxs-lookup"><span data-stu-id="d37bb-116">With **STRICT** disabled, all handle types generate the same base type.</span></span> <span data-ttu-id="d37bb-117">Con **strict** abilitato, generano tipi di base diversi.</span><span class="sxs-lookup"><span data-stu-id="d37bb-117">With **STRICT** enabled, they generate different base types.</span></span> <span data-ttu-id="d37bb-118">Per evitare conflitti, è necessario ricreare il file di intestazione ogni volta che si Abilita o si disabilita **strict** oppure modificare il file di intestazione per usare i tipi **HWND**, **HDC**, **handle** e così via, anziché i tipi di base.</span><span class="sxs-lookup"><span data-stu-id="d37bb-118">To avoid conflict, you need to re-create the header file each time you enable or disable **STRICT**, or edit the header file to use the types **HWND**, **HDC**, **HANDLE**, and so on, instead of the base types.</span></span>

<span data-ttu-id="d37bb-119">Qualsiasi dichiarazione di funzione copiata da Windows. h nel codice sorgente potrebbe essere stata modificata e la dichiarazione locale potrebbe non essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="d37bb-119">Any function declarations that you copied from Windows.h into your source code may have changed, and your local declaration may be out of date.</span></span> <span data-ttu-id="d37bb-120">Rimuovere la dichiarazione locale.</span><span class="sxs-lookup"><span data-stu-id="d37bb-120">Remove your local declaration.</span></span>

## <a name="types-that-require-casts"></a><span data-ttu-id="d37bb-121">Tipi che richiedono cast</span><span class="sxs-lookup"><span data-stu-id="d37bb-121">Types that Require Casts</span></span>

<span data-ttu-id="d37bb-122">Alcune funzioni dispongono di parametri o tipi restituiti generici.</span><span class="sxs-lookup"><span data-stu-id="d37bb-122">Some functions have generic return types or parameters.</span></span> <span data-ttu-id="d37bb-123">La funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) , ad esempio, restituisce dati che possono essere un numero qualsiasi di tipi, a seconda del contesto.</span><span class="sxs-lookup"><span data-stu-id="d37bb-123">For example, the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function returns data that may be any number of types, depending on the context.</span></span> <span data-ttu-id="d37bb-124">Quando si visualizza una di queste funzioni nel codice sorgente, assicurarsi di utilizzare il cast del tipo corretto e che sia il più possibile specifico.</span><span class="sxs-lookup"><span data-stu-id="d37bb-124">When you see any of these functions in your source code, make sure that you use the correct type cast and that it is as specific as possible.</span></span> <span data-ttu-id="d37bb-125">L'elenco seguente è un esempio di queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="d37bb-125">The following list is an example of these functions.</span></span>

-   [<span data-ttu-id="d37bb-126">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="d37bb-126">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [<span data-ttu-id="d37bb-127">**GlobalLock**</span><span class="sxs-lookup"><span data-stu-id="d37bb-127">**GlobalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [<span data-ttu-id="d37bb-128">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="d37bb-128">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [<span data-ttu-id="d37bb-129">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="d37bb-129">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [<span data-ttu-id="d37bb-130">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="d37bb-130">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="d37bb-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d37bb-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [<span data-ttu-id="d37bb-132">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="d37bb-132">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

<span data-ttu-id="d37bb-133">Quando si chiama [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)o [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), è innanzitutto necessario eseguire il cast del risultato al **tipo \_ uint PTR**.</span><span class="sxs-lookup"><span data-stu-id="d37bb-133">When you call [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), or [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), you should first cast the result to type **UINT\_PTR**.</span></span> <span data-ttu-id="d37bb-134">È necessario eseguire una procedura simile per qualsiasi funzione che restituisce un valore **LRESULT** o **Long \_ ptr** , in cui il risultato contiene un handle.</span><span class="sxs-lookup"><span data-stu-id="d37bb-134">You need to take similar steps for any function that returns an **LRESULT** or **LONG\_PTR** value, where the result contains a handle.</span></span> <span data-ttu-id="d37bb-135">Questa operazione è necessaria per la scrittura di codice portabile, in quanto le dimensioni di un handle variano a seconda della versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="d37bb-135">This is necessary for writing portable code because the size of a handle varies, depending on the version of Windows.</span></span> <span data-ttu-id="d37bb-136">Il cast (**uint \_ ptr**) garantisce una corretta conversione.</span><span class="sxs-lookup"><span data-stu-id="d37bb-136">The (**UINT\_PTR**) cast ensures proper conversion.</span></span> <span data-ttu-id="d37bb-137">Il codice seguente illustra un esempio in cui **SendMessage** restituisce un handle a un pennello:</span><span class="sxs-lookup"><span data-stu-id="d37bb-137">The following code shows an example in which **SendMessage** returns a handle to a brush:</span></span>


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



<span data-ttu-id="d37bb-138">Il parametro **CreateWindow** e **CreateWindowEx** *HMENU* viene talvolta usato per passare un identificatore di controllo Integer (ID).</span><span class="sxs-lookup"><span data-stu-id="d37bb-138">The **CreateWindow** and **CreateWindowEx** parameter *hmenu* is sometimes used to pass an integer control identifier (ID).</span></span> <span data-ttu-id="d37bb-139">In questo caso, è necessario eseguire il cast dell'ID a un tipo **HMENU** :</span><span class="sxs-lookup"><span data-stu-id="d37bb-139">In this case, you must cast the ID to an **HMENU** type:</span></span>


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a><span data-ttu-id="d37bb-140">Ulteriori considerazioni</span><span class="sxs-lookup"><span data-stu-id="d37bb-140">Additional Considerations</span></span>

<span data-ttu-id="d37bb-141">Per sfruttare al massimo i vantaggi derivanti dal controllo **rigoroso** dei tipi, è necessario seguire altre linee guida.</span><span class="sxs-lookup"><span data-stu-id="d37bb-141">To get the most benefit from **STRICT** type checking, there are additional guidelines you should follow.</span></span> <span data-ttu-id="d37bb-142">Se si apportano le modifiche seguenti, il codice sarà più portatile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="d37bb-142">Your code will be more portable in future versions of Windows if you make the following changes.</span></span>

<span data-ttu-id="d37bb-143">I tipi **wParam**, **lParam**, **LRESULT** e **LPVOID** sono *tipi di dati polimorfici*.</span><span class="sxs-lookup"><span data-stu-id="d37bb-143">The types **WPARAM**, **LPARAM**, **LRESULT**, and **LPVOID** are *polymorphic data types*.</span></span> <span data-ttu-id="d37bb-144">Contengono diversi tipi di dati in momenti diversi, anche quando è abilitato il controllo di tipo **strict** .</span><span class="sxs-lookup"><span data-stu-id="d37bb-144">They hold different kinds of data at different times, even when **STRICT** type checking is enabled.</span></span> <span data-ttu-id="d37bb-145">Per sfruttare i vantaggi del controllo dei tipi, è consigliabile eseguire il cast dei valori di questi tipi il prima possibile.</span><span class="sxs-lookup"><span data-stu-id="d37bb-145">To get the benefit of type checking, you should cast values of these types as soon as possible.</span></span> <span data-ttu-id="d37bb-146">Si noti che i cracker del messaggio riesegue automaticamente il cast di *wParam* e *lParam* in modo portatile.</span><span class="sxs-lookup"><span data-stu-id="d37bb-146">(Note that message crackers automatically recast *wParam* and *lParam* for you in a portable way.)</span></span>

<span data-ttu-id="d37bb-147">Prestare particolare attenzione per distinguere i tipi **hmodule** e **HINSTANCE** .</span><span class="sxs-lookup"><span data-stu-id="d37bb-147">Take special care to distinguish **HMODULE** and **HINSTANCE** types.</span></span> <span data-ttu-id="d37bb-148">Anche se **strict** è abilitato, vengono definiti come lo stesso tipo di base.</span><span class="sxs-lookup"><span data-stu-id="d37bb-148">Even with **STRICT** enabled, they are defined as the same base type.</span></span> <span data-ttu-id="d37bb-149">La maggior parte delle funzioni di gestione dei moduli kernel usa tipi **HINSTANCE** , ma esistono alcune funzioni che restituiscono o accettano solo tipi **hmodule** .</span><span class="sxs-lookup"><span data-stu-id="d37bb-149">Most kernel module management functions use **HINSTANCE** types, but there are a few functions that return or accept only **HMODULE** types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d37bb-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d37bb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d37bb-151">Disabilitazione di STRICT</span><span class="sxs-lookup"><span data-stu-id="d37bb-151">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="d37bb-152">Abilitazione di STRICT</span><span class="sxs-lookup"><span data-stu-id="d37bb-152">Enabling STRICT</span></span>](enabling-strict.md)
</dt> </dl>

 

 