---
description: Un componente con almeno un'interfaccia accodabile è un componente accodabile.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Creazione di componenti accodabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401435"
---
# <a name="creating-queuable-components"></a><span data-ttu-id="643c8-103">Creazione di componenti accodabili</span><span class="sxs-lookup"><span data-stu-id="643c8-103">Creating Queuable Components</span></span>

<span data-ttu-id="643c8-104">Un componente con almeno un'interfaccia accodabile è un *componente accodabile*.</span><span class="sxs-lookup"><span data-stu-id="643c8-104">A component with at least one queuable interface is a *queuable component*.</span></span> <span data-ttu-id="643c8-105">Affinché un componente venga richiamato da una coda, le interfacce devono essere contrassegnate come accodabili e il componente deve essere installato in un'applicazione in coda.</span><span class="sxs-lookup"><span data-stu-id="643c8-105">For a component to be invoked by a queue, the interfaces must be marked as queuable and the component must be installed in a queued application.</span></span> <span data-ttu-id="643c8-106">Un componente accodabile, tuttavia, può essere un componente di un'applicazione non accodata.</span><span class="sxs-lookup"><span data-stu-id="643c8-106">However, a queuable component can be a component of a non-queued application.</span></span>

<span data-ttu-id="643c8-107">Un'interfaccia accodabile deve contenere solo parametri in, senza parametri out e valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="643c8-107">A queuable interface must contain only in parameters—no out parameters and no return values.</span></span> <span data-ttu-id="643c8-108">Queste caratteristiche vengono verificate analizzando le informazioni sul tipo durante l'installazione del componente.</span><span class="sxs-lookup"><span data-stu-id="643c8-108">These characteristics are verified by analyzing the type information during component installation.</span></span> <span data-ttu-id="643c8-109">Se l'interfaccia non è accodabile, non è possibile attivare la coda dell'applicazione contenente il componente.</span><span class="sxs-lookup"><span data-stu-id="643c8-109">If the interface is not queuable, the queue of the application containing the component cannot be activated.</span></span>

<span data-ttu-id="643c8-110">Per specificare un'interfaccia COM+ come accodabile, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="643c8-110">To specify a COM+ interface as queuable, use the following steps:</span></span>

1.  <span data-ttu-id="643c8-111">Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.</span><span class="sxs-lookup"><span data-stu-id="643c8-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="643c8-112">Aprire la cartella **interfacce** del componente dell'applicazione com+ che si desidera rendere accodabile.</span><span class="sxs-lookup"><span data-stu-id="643c8-112">Open the **Interfaces** folder of the component of the COM+ application that you want to make queuable.</span></span>

3.  <span data-ttu-id="643c8-113">Fare clic con il pulsante destro del mouse sull'interfaccia che si desidera contrassegnare come accodabile, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="643c8-113">Right-click the interface that you want to mark as queuable, and then click **Properties**.</span></span>

4.  <span data-ttu-id="643c8-114">Selezionare la scheda **Accodamento** nella finestra di dialogo Proprietà.</span><span class="sxs-lookup"><span data-stu-id="643c8-114">Select the **Queuing** tab in the properties dialog.</span></span>

5.  <span data-ttu-id="643c8-115">Attivare la casella di controllo con l'etichetta **accodata**.</span><span class="sxs-lookup"><span data-stu-id="643c8-115">Activate the check box labeled **Queued**.</span></span>

    > [!Note]  
    > <span data-ttu-id="643c8-116">Se la casella di controllo in **coda** è disabilitata, l'interfaccia non soddisfa i vincoli accodabili descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="643c8-116">If the **Queued** check box is grayed out, the interface does not satisfy the queuable constraints described above.</span></span>

     

6.  <span data-ttu-id="643c8-117">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="643c8-117">Click **OK**.</span></span>

    <span data-ttu-id="643c8-118">È possibile identificare un componente accodabile aggiungendo la macro dell'attributo QUEUEable alla sezione Interface del file di origine IDL (Interface Definition Language) per tutte le interfacce che sono accodabili.</span><span class="sxs-lookup"><span data-stu-id="643c8-118">A queuable component can be identified as such by adding the QUEUEABLE attribute macro to the Interface section of the Interface Definition Language (IDL) source file for all interfaces that are queuable.</span></span>

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a><span data-ttu-id="643c8-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="643c8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="643c8-120">Creazione di code di componenti</span><span class="sxs-lookup"><span data-stu-id="643c8-120">Creating Component Queues</span></span>](creating-component-queues.md)
</dt> <dt>

[<span data-ttu-id="643c8-121">Sviluppo di componenti in coda</span><span class="sxs-lookup"><span data-stu-id="643c8-121">Developing Queued Components</span></span>](developing-queued-components.md)
</dt> </dl>

 

 



