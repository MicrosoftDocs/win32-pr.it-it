---
description: Flag coerenti e done
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Flag coerenti e done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524370"
---
# <a name="consistent-and-done-flags"></a><span data-ttu-id="33bfe-103">Flag coerenti e done</span><span class="sxs-lookup"><span data-stu-id="33bfe-103">Consistent and Done Flags</span></span>

<span data-ttu-id="33bfe-104">COM+ crea sempre un oggetto di contesto prima di attivare un oggetto transazionale.</span><span class="sxs-lookup"><span data-stu-id="33bfe-104">COM+ always creates a context object before activating a transactional object.</span></span> <span data-ttu-id="33bfe-105">L'oggetto context include informazioni correlate agli oggetti, ad esempio l'autore e il relativo identificatore di transazione.</span><span class="sxs-lookup"><span data-stu-id="33bfe-105">The context object holds object-related information, such as its creator and its transaction identifier.</span></span> <span data-ttu-id="33bfe-106">Ogni oggetto Context contiene anche un *flag coerente* e un *flag done*.</span><span class="sxs-lookup"><span data-stu-id="33bfe-106">Each context object also contains a *consistent flag* and a *done flag*.</span></span> <span data-ttu-id="33bfe-107">Insieme a questi flag viene determinato lo stato dell'oggetto transazionale.</span><span class="sxs-lookup"><span data-stu-id="33bfe-107">Together these flags determine the status of the transactional object.</span></span>

<span data-ttu-id="33bfe-108">Il flag coerente indica che l'oggetto transazionale è coerente o incoerente.</span><span class="sxs-lookup"><span data-stu-id="33bfe-108">The consistent flag indicates that the transactional object is either consistent or inconsistent.</span></span> <span data-ttu-id="33bfe-109">I dettagli specifici di ciò che rende coerente lo stato di un oggetto sono al programmatore.</span><span class="sxs-lookup"><span data-stu-id="33bfe-109">The specific details of what makes an object's state consistent is up to the programmer.</span></span> <span data-ttu-id="33bfe-110">Quando una chiamata al metodo imposta questo flag su true, l'oggetto è coerente.</span><span class="sxs-lookup"><span data-stu-id="33bfe-110">When a method call sets this flag to True, the object is consistent.</span></span> <span data-ttu-id="33bfe-111">False indica che l'oggetto è incoerente.</span><span class="sxs-lookup"><span data-stu-id="33bfe-111">False indicates that the object is inconsistent.</span></span> <span data-ttu-id="33bfe-112">COM+ imposta il flag su true quando crea un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33bfe-112">COM+ sets the flag to True when it creates an object instance.</span></span> <span data-ttu-id="33bfe-113">Un oggetto coerente è pronto per procedere con la transazione.</span><span class="sxs-lookup"><span data-stu-id="33bfe-113">A consistent object is ready to proceed with the transaction.</span></span> <span data-ttu-id="33bfe-114">Mentre un oggetto rimane attivo, le chiamate al metodo successive possono cambiare ripetutamente il flag coerente da true a false e viceversa.</span><span class="sxs-lookup"><span data-stu-id="33bfe-114">While an object remains active, subsequent method calls can repeatedly switch the consistent flag from True to False and vice versa.</span></span>

<span data-ttu-id="33bfe-115">Il flag done determina la durata di una transazione.</span><span class="sxs-lookup"><span data-stu-id="33bfe-115">The done flag determines the duration of a transaction.</span></span> <span data-ttu-id="33bfe-116">Quando una chiamata al metodo restituisce, COM+ controlla il flag done.</span><span class="sxs-lookup"><span data-stu-id="33bfe-116">When a method call returns, COM+ inspects the done flag.</span></span> <span data-ttu-id="33bfe-117">Se il metodo imposta questo flag su true, COM+ disattiva l'oggetto e annota il flag coerente.</span><span class="sxs-lookup"><span data-stu-id="33bfe-117">If the method sets this flag to True, COM+ deactivates the object and notes the consistent flag.</span></span> <span data-ttu-id="33bfe-118">Quando il flag done è false, COM+ non disattiva l'oggetto né annota il flag coerente.</span><span class="sxs-lookup"><span data-stu-id="33bfe-118">When the done flag is False, COM+ neither deactivates the object nor notes the consistent flag.</span></span> <span data-ttu-id="33bfe-119">COM+ imposta il flag done su false quando crea un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33bfe-119">COM+ sets the done flag to False when it creates an object instance.</span></span>

<span data-ttu-id="33bfe-120">Il flag coerente esegue il cast di un voto per eseguire il commit o interrompere la transazione in cui viene eseguita e il flag done finalizza il voto.</span><span class="sxs-lookup"><span data-stu-id="33bfe-120">The consistent flag casts a vote to commit or abort the transaction in which it executes, and the done flag finalizes the vote.</span></span> <span data-ttu-id="33bfe-121">COM+ controlla il flag coerente quando il flag done è impostato su true in una chiamata al metodo return o quando l'oggetto viene disattivato.</span><span class="sxs-lookup"><span data-stu-id="33bfe-121">COM+ inspects the consistent flag when the done flag is set to True on a method call return or when the object deactivates.</span></span> <span data-ttu-id="33bfe-122">Sebbene un flag coerente di un oggetto possa essere modificato ripetutamente all'interno di ogni chiamata al metodo, solo l'ultima modifica viene conteggiata.</span><span class="sxs-lookup"><span data-stu-id="33bfe-122">Although an object's consistent flag can change repeatedly within each method call, only the last change counts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33bfe-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33bfe-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33bfe-124">Gestione delle transazioni automatiche in COM+</span><span class="sxs-lookup"><span data-stu-id="33bfe-124">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[<span data-ttu-id="33bfe-125">Impostazione dei flag coerenti e done</span><span class="sxs-lookup"><span data-stu-id="33bfe-125">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



