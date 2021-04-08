---
description: È possibile impostare manualmente il livello di isolamento delle transazioni dei componenti utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile configurare a livello di codice il livello di isolamento delle transazioni per un componente utilizzando le interfacce di amministrazione COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Impostazione del livello di isolamento delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748842"
---
# <a name="setting-the-transaction-isolation-level"></a><span data-ttu-id="73e2d-103">Impostazione del livello di isolamento delle transazioni</span><span class="sxs-lookup"><span data-stu-id="73e2d-103">Setting the Transaction Isolation Level</span></span>

<span data-ttu-id="73e2d-104">È possibile impostare manualmente il livello di isolamento delle transazioni dei componenti utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile configurare a livello di codice il livello di isolamento delle transazioni per un componente utilizzando le [interfacce di amministrazione com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="73e2d-104">You can manually set the transaction isolation level of components by using the Component Services administrative tool, or you can programmatically configure the transaction isolation level for a component by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span>

<span data-ttu-id="73e2d-105">Per ulteriori informazioni sui livelli di isolamento delle transazioni, vedere [configurazione dei livelli di isolamento delle transazioni](configuring-transaction-isolation-levels.md).</span><span class="sxs-lookup"><span data-stu-id="73e2d-105">For more on transaction isolation levels, see [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md).</span></span>

<span data-ttu-id="73e2d-106">**Per impostare il livello di isolamento della transazione utilizzando lo strumento di amministrazione Servizi componenti**</span><span class="sxs-lookup"><span data-stu-id="73e2d-106">**To set the transaction isolation level by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="73e2d-107">Nell'albero della console fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="73e2d-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="73e2d-108">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **transazioni** .</span><span class="sxs-lookup"><span data-stu-id="73e2d-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="73e2d-109">In **livello di isolamento transazione** selezionare il valore desiderato dalla casella di riepilogo a discesa.</span><span class="sxs-lookup"><span data-stu-id="73e2d-109">Under **Transaction Isolation Level**, select the value you want from the drop-down box.</span></span> <span data-ttu-id="73e2d-110">Il valore predefinito per tutti i componenti viene **serializzato**.</span><span class="sxs-lookup"><span data-stu-id="73e2d-110">The default value for all components is **Serialized**.</span></span>

    > [!Note]  
    > <span data-ttu-id="73e2d-111">Se è selezionato **disabilitato** o **non supportato** in **supporto transazioni**, non è possibile impostare il livello di isolamento della transazione.</span><span class="sxs-lookup"><span data-stu-id="73e2d-111">If either **Disabled** or **Not Supported** is selected under **Transaction support**, you cannot set the transaction isolation level.</span></span>

     

4.  <span data-ttu-id="73e2d-112">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="73e2d-112">Click **OK**.</span></span>

<span data-ttu-id="73e2d-113">È necessario ripetere questa procedura per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="73e2d-113">You must repeat this procedure for each component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73e2d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73e2d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73e2d-115">Configurazione di livelli di isolamento delle transazioni</span><span class="sxs-lookup"><span data-stu-id="73e2d-115">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



