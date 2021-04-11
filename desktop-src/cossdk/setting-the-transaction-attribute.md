---
description: È possibile impostare manualmente gli attributi delle transazioni utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile aggiungere il supporto programmatico per le transazioni quando si scrive il componente.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Impostazione dell'attributo Transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127394"
---
# <a name="setting-the-transaction-attribute"></a><span data-ttu-id="11430-103">Impostazione dell'attributo Transaction</span><span class="sxs-lookup"><span data-stu-id="11430-103">Setting the Transaction Attribute</span></span>

<span data-ttu-id="11430-104">È possibile impostare manualmente gli attributi delle transazioni utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile aggiungere il supporto programmatico per le transazioni quando si scrive il componente.</span><span class="sxs-lookup"><span data-stu-id="11430-104">You can set transaction attributes manually by using the Component Services administrative tool, or you can add programmatic support for transactions when you write your component.</span></span>

<span data-ttu-id="11430-105">Per ulteriori informazioni sui valori degli attributi delle transazioni, vedere [Configuring Transactions](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="11430-105">For more on transaction attribute values, see [Configuring Transactions](configuring-transactions.md).</span></span>

<span data-ttu-id="11430-106">**Per impostare il valore dell'attributo utilizzando lo strumento di amministrazione Servizi componenti**</span><span class="sxs-lookup"><span data-stu-id="11430-106">**To set the attribute value by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="11430-107">Nell'albero della console fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="11430-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="11430-108">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **transazioni** .</span><span class="sxs-lookup"><span data-stu-id="11430-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="11430-109">In **supporto transazioni** selezionare l'opzione per il valore desiderato.</span><span class="sxs-lookup"><span data-stu-id="11430-109">Under **Transaction support**, select the option for the value you want.</span></span> <span data-ttu-id="11430-110">Il valore predefinito per tutti i componenti **non è supportato**.</span><span class="sxs-lookup"><span data-stu-id="11430-110">The default value for all components is **Not Supported**.</span></span>

4.  <span data-ttu-id="11430-111">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="11430-111">Click **OK**.</span></span>

<span data-ttu-id="11430-112">È necessario ripetere questa procedura per ogni componente.</span><span class="sxs-lookup"><span data-stu-id="11430-112">You must repeat this procedure for each component.</span></span>

## <a name="to-set-the-attribute-value-programmatically"></a><span data-ttu-id="11430-113">Per impostare il valore dell'attributo a livello di codice</span><span class="sxs-lookup"><span data-stu-id="11430-113">To set the attribute value programmatically</span></span>

<span data-ttu-id="11430-114">I programmatori che utilizzano Microsoft Visual Basic possono impostare l'attributo Transaction con **MTSTransactionMode**, una proprietà del modulo di classe per i progetti DLL ActiveX.</span><span class="sxs-lookup"><span data-stu-id="11430-114">Programmers using Microsoft Visual Basic can set the transaction attribute with **MTSTransactionMode**, a class module property for ActiveX DLL projects.</span></span> <span data-ttu-id="11430-115">Visual Basic esegue il mapping della selezione al valore dell'attributo di transazione COM+ equivalente e pubblica il valore nella libreria dei tipi del componente.</span><span class="sxs-lookup"><span data-stu-id="11430-115">Visual Basic maps your selection to the equivalent COM+ transaction attribute value and publishes the value in your component's type library.</span></span>

<span data-ttu-id="11430-116">Nella tabella seguente viene eseguito il mapping di ogni valore costante **MTSTransactionMode** al valore di transazione com+ equivalente.</span><span class="sxs-lookup"><span data-stu-id="11430-116">The following table maps each **MTSTransactionMode** constant value to its equivalent COM+ transaction value.</span></span>



| <span data-ttu-id="11430-117">Costante MTSTransactionMode</span><span class="sxs-lookup"><span data-stu-id="11430-117">MTSTransactionMode constant</span></span>         | <span data-ttu-id="11430-118">Valore transazione COM+</span><span class="sxs-lookup"><span data-stu-id="11430-118">COM+ transaction value</span></span>             |
|-------------------------------------|------------------------------------|
| <span data-ttu-id="11430-119">NotAnMTSObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11430-119">NotAnMTSObject (default)</span></span><br/> | <span data-ttu-id="11430-120">Disabled</span><span class="sxs-lookup"><span data-stu-id="11430-120">Disabled</span></span><br/>                |
| <span data-ttu-id="11430-121">Notransacts</span><span class="sxs-lookup"><span data-stu-id="11430-121">NoTransactions</span></span><br/>           | <span data-ttu-id="11430-122">Non supportato (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11430-122">Not Supported (default)</span></span><br/> |
| <span data-ttu-id="11430-123">RequiresTransaction</span><span class="sxs-lookup"><span data-stu-id="11430-123">RequiresTransaction</span></span> <br/>     | <span data-ttu-id="11430-124">Necessario</span><span class="sxs-lookup"><span data-stu-id="11430-124">Required</span></span><br/>                |
| <span data-ttu-id="11430-125">UsesTransaction</span><span class="sxs-lookup"><span data-stu-id="11430-125">UsesTransaction</span></span> <br/>         | <span data-ttu-id="11430-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="11430-126">Supported</span></span><br/>               |
| <span data-ttu-id="11430-127">RequiresNewTransaction</span><span class="sxs-lookup"><span data-stu-id="11430-127">RequiresNewTransaction</span></span> <br/>  | <span data-ttu-id="11430-128">RequiresNew</span><span class="sxs-lookup"><span data-stu-id="11430-128">Requires New</span></span><br/>            |



 

<span data-ttu-id="11430-129">È inoltre possibile accedere alla proprietà **MTSTransactionMode** a livello di codice tramite l'API della libreria di amministrazione com+.</span><span class="sxs-lookup"><span data-stu-id="11430-129">The **MTSTransactionMode** property can also be accessed programmatically by using the COM+ Administration Library API.</span></span>

 

 




