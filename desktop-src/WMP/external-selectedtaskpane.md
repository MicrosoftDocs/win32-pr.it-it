---
title: External. SelectedTaskPane
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà SelectedTaskPane specifica o Recupera il riquadro attività attualmente selezionato.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- Media Player di Windows External. SelectedTaskPane
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324542"
---
# <a name="externalselectedtaskpane"></a><span data-ttu-id="3ecdf-106">External. SelectedTaskPane</span><span class="sxs-lookup"><span data-stu-id="3ecdf-106">External.SelectedTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="3ecdf-107">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="3ecdf-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3ecdf-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3ecdf-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3ecdf-109">La proprietà **SelectedTaskPane** specifica o Recupera il riquadro attività attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="3ecdf-109">The **SelectedTaskPane** property specifies or retrieves the currently selected task pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ecdf-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ecdf-110">Syntax</span></span>

<span data-ttu-id="3ecdf-111">Window. External. SelectedTaskPane = *servicetask*</span><span class="sxs-lookup"><span data-stu-id="3ecdf-111">window.external.SelectedTaskPane = *servicetask*</span></span>

## <a name="possible-values"></a><span data-ttu-id="3ecdf-112">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3ecdf-112">Possible Values</span></span>

<span data-ttu-id="3ecdf-113">Questa proprietà è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3ecdf-113">This property is a read/write **String**.</span></span> <span data-ttu-id="3ecdf-114">I valori possibili sono "ServiceTask1", "ServiceTask2" e "ServiceTask3".</span><span class="sxs-lookup"><span data-stu-id="3ecdf-114">Possible values are "ServiceTask1", "ServiceTask2", and "ServiceTask3".</span></span>

## <a name="remarks"></a><span data-ttu-id="3ecdf-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ecdf-115">Remarks</span></span>

<span data-ttu-id="3ecdf-116">Se si specifica un valore per questa proprietà, viene evidenziato il pulsante relativo a tale riquadro.</span><span class="sxs-lookup"><span data-stu-id="3ecdf-116">Specifying a value for this property highlights the button for that pane.</span></span> <span data-ttu-id="3ecdf-117">Non rende attivo il riquadro attività specificato.</span><span class="sxs-lookup"><span data-stu-id="3ecdf-117">It does not make the specified task pane active.</span></span> <span data-ttu-id="3ecdf-118">È necessario specificare un valore per questa proprietà per impostare il pulsante del riquadro attività corrente per la pagina Web quando viene caricata la pagina per assicurarsi che il pulsante riquadro attività corretto sia attivo.</span><span class="sxs-lookup"><span data-stu-id="3ecdf-118">You should specify a value for this property to set the current task pane button for your webpage when the page loads to ensure that the correct task pane button is active.</span></span>

<span data-ttu-id="3ecdf-119">Per rendere attivo uno specifico riquadro attività, utilizzare il metodo **NavigateTaskPaneURL** .</span><span class="sxs-lookup"><span data-stu-id="3ecdf-119">To make a particular task pane the active one, use the **NavigateTaskPaneURL** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecdf-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ecdf-120">Requirements</span></span>



| <span data-ttu-id="3ecdf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ecdf-121">Requirement</span></span> | <span data-ttu-id="3ecdf-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3ecdf-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ecdf-123">Versione</span><span class="sxs-lookup"><span data-stu-id="3ecdf-123">Version</span></span><br/> | <span data-ttu-id="3ecdf-124">Windows Media Player 10 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3ecdf-124">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="3ecdf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3ecdf-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3ecdf-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ecdf-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ecdf-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ecdf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecdf-128">**Oggetto esterno per i negozi di tipo 2 online**</span><span class="sxs-lookup"><span data-stu-id="3ecdf-128">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="3ecdf-129">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="3ecdf-129">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





