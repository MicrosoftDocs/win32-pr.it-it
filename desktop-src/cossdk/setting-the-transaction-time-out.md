---
description: È possibile impostare manualmente il timeout per le transazioni utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile configurare il timeout a livello di codice utilizzando le interfacce di amministrazione COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Impostazione della transazione Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483781"
---
# <a name="setting-the-transaction-time-out"></a><span data-ttu-id="7199d-103">Impostazione della transazione Time-Out</span><span class="sxs-lookup"><span data-stu-id="7199d-103">Setting the Transaction Time-Out</span></span>

<span data-ttu-id="7199d-104">È possibile impostare manualmente il timeout per le transazioni utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile configurare il timeout a livello di codice utilizzando le [interfacce di amministrazione com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7199d-104">You can manually set the time-out for transactions by using the Component Services administrative tool, or you can programmatically configure the time-out by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span> <span data-ttu-id="7199d-105">Il timeout può essere configurato a livello di computer locale e anche per i singoli componenti.</span><span class="sxs-lookup"><span data-stu-id="7199d-105">The time-out can be configured at the local computer level and also for individual components.</span></span>

<span data-ttu-id="7199d-106">**Per impostare il timeout della transazione per il computer locale utilizzando lo strumento di amministrazione Servizi componenti**</span><span class="sxs-lookup"><span data-stu-id="7199d-106">**To set the transaction time-out for the local computer by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="7199d-107">Nell'albero della console fare clic con il pulsante destro del mouse sul computer locale che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="7199d-107">In the console tree, right-click the local computer you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="7199d-108">Nella finestra di dialogo Proprietà computer fare clic sulla scheda **Opzioni** .</span><span class="sxs-lookup"><span data-stu-id="7199d-108">In the computer properties dialog box, click the **Options** tab.</span></span>

3.  <span data-ttu-id="7199d-109">In **timeout transazione** immettere il timeout della transazione in secondi.</span><span class="sxs-lookup"><span data-stu-id="7199d-109">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="7199d-110">Il timeout predefinito è di 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="7199d-110">The default time-out is 60 seconds.</span></span>

4.  <span data-ttu-id="7199d-111">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="7199d-111">Click **OK**.</span></span>

<span data-ttu-id="7199d-112">**Per impostare il timeout della transazione per un componente utilizzando lo strumento di amministrazione Servizi componenti**</span><span class="sxs-lookup"><span data-stu-id="7199d-112">**To set the transaction time-out for a component by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="7199d-113">Nell'albero della console fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="7199d-113">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="7199d-114">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **transazioni** .</span><span class="sxs-lookup"><span data-stu-id="7199d-114">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="7199d-115">Selezionare la casella **Sostituisci valore di timeout transazioni globali**.</span><span class="sxs-lookup"><span data-stu-id="7199d-115">Check the box labeled **Override global transaction timeout value**.</span></span>

    > [!Note]  
    > <span data-ttu-id="7199d-116">Non è possibile selezionare la casella per eseguire l'override del valore di timeout della transazione globale se il **supporto delle transazioni** è impostato su **disabilitato**, **non supportato** o **supportato**.</span><span class="sxs-lookup"><span data-stu-id="7199d-116">You cannot check the box to override the global transaction time-out value if the **Transaction support** is set to **Disabled**, **Not Supported**, or **Supported**.</span></span>

     

4.  <span data-ttu-id="7199d-117">In **timeout transazione** immettere il timeout della transazione in secondi.</span><span class="sxs-lookup"><span data-stu-id="7199d-117">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="7199d-118">Il timeout predefinito è 0 secondi, il che significa che il componente non provocherà mai il timeout della transazione.</span><span class="sxs-lookup"><span data-stu-id="7199d-118">The default time-out is 0 seconds, which means that the component will never cause the transaction to time out.</span></span>

5.  <span data-ttu-id="7199d-119">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="7199d-119">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7199d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7199d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7199d-121">Gestione delle transazioni automatiche in COM+</span><span class="sxs-lookup"><span data-stu-id="7199d-121">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



