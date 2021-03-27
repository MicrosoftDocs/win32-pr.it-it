---
description: Notifica inviata all'oggetto di callback di visualizzazione per specificare i percorsi e gli eventi che devono essere registrati per gli eventi di notifica delle modifiche.
title: Messaggio SFVM_GETNOTIFY (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232336"
---
# <a name="sfvm_getnotify-message"></a><span data-ttu-id="d39f0-103">\_Messaggio GETNOTIFY SFVM</span><span class="sxs-lookup"><span data-stu-id="d39f0-103">SFVM\_GETNOTIFY message</span></span>

<span data-ttu-id="d39f0-104">Notifica inviata all'oggetto di callback di visualizzazione per specificare i percorsi e gli eventi che devono essere registrati per gli eventi di notifica delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="d39f0-104">Notification sent to the view callback object to specify the locations and events that should be registered for change notification events.</span></span> <span data-ttu-id="d39f0-105">Una volta registrate, quando si verifica una modifica in in questi percorsi o eventi, viene inviata una notifica all'oggetto di callback della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d39f0-105">Once they are registered, when a change occurs in on of these locations or events, the view callback object is notified.</span></span> <span data-ttu-id="d39f0-106">Questi eventi vengono inviati al callback di visualizzazione tramite [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) e vengono quindi gestiti dalla vista.</span><span class="sxs-lookup"><span data-stu-id="d39f0-106">These events are sent to the view callback through [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) and are then handled by the view.</span></span>


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a><span data-ttu-id="d39f0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d39f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d39f0-108">*PIDL* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d39f0-108">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d39f0-109">Puntatore a un IDList assoluto di un elemento per il quale la visualizzazione deve essere registrata per ricevere una notifica delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="d39f0-109">A pointer to an absolute IDList of an item for which the view should register to be notified of changes.</span></span> <span data-ttu-id="d39f0-110">In genere, si tratta dello stesso IDList della posizione visualizzata, ma può trattarsi di un altro percorso.</span><span class="sxs-lookup"><span data-stu-id="d39f0-110">Typically, this is the same as the IDList of the location being viewed, but it can be another location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d39f0-111">La durata di questo valore è di proprietà dell'oggetto di callback della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d39f0-111">The lifetime of this value is owned by the view callback object.</span></span> <span data-ttu-id="d39f0-112">È responsabilità dell'oggetto View callback creare e quindi liberare questo valore quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="d39f0-112">It is the responsibility of the view callback object to create and then free this value when it is no longer needed.</span></span> <span data-ttu-id="d39f0-113">Per questo è necessario che l'oggetto View callback memorizzi questo valore.</span><span class="sxs-lookup"><span data-stu-id="d39f0-113">This requires that the view callback object stores this value.</span></span> <span data-ttu-id="d39f0-114">In genere, il valore può essere archiviato nel membro **\_ pidlMonitor** dell'oggetto View callback.</span><span class="sxs-lookup"><span data-stu-id="d39f0-114">Usually, the value can be stored in the **\_pidlMonitor** member of the view callback object.</span></span> <span data-ttu-id="d39f0-115">Le regole di proprietà per il valore restituito tramite *PIDL* sono non standard e richiedono particolare attenzione.</span><span class="sxs-lookup"><span data-stu-id="d39f0-115">The ownership rules for the value returned through *pidl* are nonstandard and require special care.</span></span> <span data-ttu-id="d39f0-116">L'oggetto di callback della visualizzazione deve essere proprietario di questo valore e assicurarsi che non venga liberato fino a quando l'oggetto di callback della visualizzazione non viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="d39f0-116">The view callback object must own this value and ensure that it is not freed until the view callback object itself is destroyed.</span></span>

 

</dd> <dt>

<span data-ttu-id="d39f0-117">*Levent* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d39f0-117">*lEvents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d39f0-118">Valore che contiene uno o più valori SHCNE.</span><span class="sxs-lookup"><span data-stu-id="d39f0-118">A value that contains one or more SHCNE values.</span></span> <span data-ttu-id="d39f0-119">Per un elenco dei valori possibili, vedere [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) .</span><span class="sxs-lookup"><span data-stu-id="d39f0-119">See [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) for a list of possible values.</span></span> <span data-ttu-id="d39f0-120">L'oggetto View callback viene registrato per ricevere un messaggio [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) quando si verifica uno degli eventi associati.</span><span class="sxs-lookup"><span data-stu-id="d39f0-120">The view callback object will register to receive an [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) message when any of the associated events occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d39f0-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d39f0-121">Return value</span></span>

<span data-ttu-id="d39f0-122">Ignorato, ma deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d39f0-122">Ignored, but should return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d39f0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d39f0-123">Remarks</span></span>

<span data-ttu-id="d39f0-124">Se il messaggio di callback non restituisce un valore diverso da zero per IDList o mask eventi, la vista non verrà registrata per le notifiche di modifica.</span><span class="sxs-lookup"><span data-stu-id="d39f0-124">If this callback message does not return a nonzero value for either the IDList or the events mask then the view will not register for change notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="d39f0-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="d39f0-125">Examples</span></span>

<span data-ttu-id="d39f0-126">Nell'esempio seguente viene illustrata un'implementazione di esempio del codice del gestore della funzione di callback View per **SFVM \_ GetNotify**.</span><span class="sxs-lookup"><span data-stu-id="d39f0-126">The following sample shows an example implementation of the view callback function's handler code for **SFVM\_GETNOTIFY**.</span></span>


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a><span data-ttu-id="d39f0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d39f0-127">Requirements</span></span>



| <span data-ttu-id="d39f0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d39f0-128">Requirement</span></span> | <span data-ttu-id="d39f0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d39f0-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d39f0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d39f0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d39f0-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d39f0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d39f0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d39f0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d39f0-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d39f0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d39f0-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d39f0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d39f0-135"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d39f0-135"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d39f0-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d39f0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39f0-137">**\_QUERYFSNOTIFY SFVM**</span><span class="sxs-lookup"><span data-stu-id="d39f0-137">**SFVM\_QUERYFSNOTIFY**</span></span>](sfvm-queryfsnotify.md)
</dt> <dt>

[<span data-ttu-id="d39f0-138">**IShellFolderViewCB::MessageSFVCB**</span><span class="sxs-lookup"><span data-stu-id="d39f0-138">**IShellFolderViewCB::MessageSFVCB**</span></span>](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
