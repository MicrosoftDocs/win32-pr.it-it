---
description: Se si sceglie di implementare la cancellazione nell'applicazione diversa da tramite l'oggetto InkOverlay, è possibile eseguire questa operazione utilizzando uno dei due metodi seguenti.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Cancellazione tramite penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401659"
---
# <a name="erasing-by-using-the-pen"></a><span data-ttu-id="1a2a3-103">Cancellazione tramite penna</span><span class="sxs-lookup"><span data-stu-id="1a2a3-103">Erasing by Using the Pen</span></span>

<span data-ttu-id="1a2a3-104">Se si sceglie di implementare la cancellazione nell'applicazione diversa da tramite l'oggetto [**InkOverlay**](inkoverlay-class.md) , è possibile eseguire questa operazione utilizzando uno dei due metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-104">If you choose to implement erasing in your application other than by using the [**InkOverlay**](inkoverlay-class.md) object, you can do so by using one of the following two methods.</span></span>

## <a name="using-the-tip-of-the-pen"></a><span data-ttu-id="1a2a3-105">Uso del suggerimento della penna</span><span class="sxs-lookup"><span data-stu-id="1a2a3-105">Using the Tip of the Pen</span></span>

<span data-ttu-id="1a2a3-106">Il suggerimento della penna del Tablet viene in genere usato per la grafia e il disegno; Tuttavia, il suggerimento può essere usato anche per cancellare l'input penna.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-106">The tip of the tablet pen is generally used for handwriting and drawing; however, the tip can also be used to erase ink.</span></span> <span data-ttu-id="1a2a3-107">A tale scopo, è necessario che l'applicazione disponga di una modalità di cancellazione che gli utenti possono utilizzare.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-107">To do so, the application must have an erase mode that users can employ.</span></span> <span data-ttu-id="1a2a3-108">In questa modalità, utilizzare hit testing per determinare l'input penna su cui si sta muovendo il cursore.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-108">In this mode, use hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="1a2a3-109">È possibile impostare la modalità di cancellazione per eliminare solo l'input penna passato dal cursore o interi tratti che intersecano il percorso del cursore, a seconda delle considerazioni sulla progettazione o sulle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-109">You can set the erase mode to delete only the ink that the cursor passes over or whole strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="1a2a3-110">Per un esempio di come usare una modalità di cancellazione per cancellare l'input penna, vedere l' [esempio di cancellazione di input penna](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1a2a3-110">For an example of how to use an erase mode to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

## <a name="using-the-top-of-the-pen"></a><span data-ttu-id="1a2a3-111">Uso della parte superiore della penna</span><span class="sxs-lookup"><span data-stu-id="1a2a3-111">Using the Top of the Pen</span></span>

<span data-ttu-id="1a2a3-112">Per implementare la cancellazione con la parte superiore della penna del tablet, l'applicazione deve cercare una modifica nel cursore.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-112">To implement erasing with the top of the tablet pen, your application must look for a change in the cursor.</span></span> <span data-ttu-id="1a2a3-113">Per cercare il cursore invertito, attendere l'evento [**CursorInRange**](inkoverlay-cursorinrange.md) per determinare quando il cursore si trova all'interno del contesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-113">To look for the inverted cursor, listen for the [**CursorInRange**](inkoverlay-cursorinrange.md) event to determine when the cursor is within the context of your application.</span></span> <span data-ttu-id="1a2a3-114">Quando il cursore si trova nell'intervallo, cercare la proprietà [**invertita**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sull'oggetto [**cursore**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="1a2a3-114">When the cursor is in range, look for the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span> <span data-ttu-id="1a2a3-115">Se la proprietà **invertita** è **true**, eseguire l'hit testing per determinare l'input penna su cui si sta muovendo il cursore.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-115">If the **Inverted** property is **true**, perform hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="1a2a3-116">Cancellare l'input penna o i tratti che intersecano il percorso del cursore, a seconda delle considerazioni sulla progettazione o sulle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-116">Erase either the ink or the strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="1a2a3-117">Per un esempio di come usare la parte superiore della penna per cancellare l'input penna, vedere l' [esempio di cancellazione di input penna](ink-erasing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1a2a3-117">For an example of how to use the top of the pen to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a><span data-ttu-id="1a2a3-118">Determinazione della cancellazione con la parte superiore della penna abilitata</span><span class="sxs-lookup"><span data-stu-id="1a2a3-118">Determining if Erasing with the Top of the Pen Is Enabled</span></span>

<span data-ttu-id="1a2a3-119">Gli utenti possono utilizzare la parte superiore della penna per cancellare l'input penna in applicazioni progettate per Tablet PC, se il relativo hardware specifico lo supporta.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-119">Users can use the top of the pen to erase ink in applications designed for Tablet PC, if their particular hardware allows for it.</span></span> <span data-ttu-id="1a2a3-120">Questa funzionalità è accessibile da una casella di controllo nella casella di gruppo pulsanti penna nella scheda Opzioni penna della finestra di dialogo Pannello di controllo Impostazioni Tablet e penna.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-120">This functionality is accessed by a check box in the Pen buttons group box on the Pen Options tab of the Tablet and Pen Settings control panel dialog.</span></span> <span data-ttu-id="1a2a3-121">Per rilevare se l'utente ha abilitato la cancellazione per la parte superiore della penna, controllare la seguente sottochiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="1a2a3-121">To detect if the user has enabled erasing for the top of the pen, check the following registry subkey:</span></span>

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

<span data-ttu-id="1a2a3-122">La `EraseEnable` voce della sottochiave è di tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-122">The `EraseEnable` entry of this subkey is of type **REG\_DWORD**.</span></span> <span data-ttu-id="1a2a3-123">Il valore di questa voce è 1 per Enabled oppure 0 per Disabled.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-123">The value of this entry is 1 for enabled, or 0 for disabled.</span></span> <span data-ttu-id="1a2a3-124">Altri valori sono riservati per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-124">Other values are reserved for future use.</span></span>

<span data-ttu-id="1a2a3-125">Se l'applicazione consente di usare la parte superiore della penna per la cancellazione, è consigliabile controllare e memorizzare nella cache il valore della voce EraseEnable quando:</span><span class="sxs-lookup"><span data-stu-id="1a2a3-125">If your application allows the top of the pen to be used for erasing, you should check and cache the value of the EraseEnable entry when:</span></span>

-   <span data-ttu-id="1a2a3-126">Viene avviata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-126">Your application launches.</span></span>
-   <span data-ttu-id="1a2a3-127">Ogni volta che l'applicazione riceve lo stato attivo dopo aver perso lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-127">Any time your application receives focus after losing focus.</span></span>

<span data-ttu-id="1a2a3-128">Utilizzare questo valore memorizzato nella cache per modificare il comportamento dell'applicazione in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-128">Use this cached value to modify the behavior of your application appropriately.</span></span>

<span data-ttu-id="1a2a3-129">Nell'esempio C seguente \# viene definito un `GetEraseEnabled` metodo che controlla il valore della `EraseEnable` voce della `SysEventParameters` sottochiave.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-129">The following C\# example defines a `GetEraseEnabled` method that checks the value of the `EraseEnable` entry of the `SysEventParameters` subkey.</span></span> <span data-ttu-id="1a2a3-130">Il `GetEraseEnabled` metodo restituisce **true** se il valore della voce è 1. restituisce **false** se il valore della voce è 0 oppure genera un'eccezione [InvalidOperationException](/dotnet/api/system.invalidoperationexception) se il valore della voce è diverso da 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-130">The `GetEraseEnabled` method returns **TRUE** if the value of the entry is 1; returns **FALSE** if the value of the entry is 0; or throws an [InvalidOperationException](/dotnet/api/system.invalidoperationexception) exception if the value of the entry is other than 1 or 0.</span></span> <span data-ttu-id="1a2a3-131">Il `GetEraseEnabled` metodo restituisce il valore previsto **true** se la sottochiave o la voce non è presente.</span><span class="sxs-lookup"><span data-stu-id="1a2a3-131">The `GetEraseEnabled` method returns the expected value of **TRUE** if either the subkey or the entry is not present.</span></span>


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
