---
description: L'azione RemoveRegistryValues può rimuovere solo i valori dal registro di sistema che sono stati creati nella tabella del registro di sistema o nella tabella RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Azione RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313803"
---
# <a name="removeregistryvalues-action"></a><span data-ttu-id="24ff1-103">Azione RemoveRegistryValues</span><span class="sxs-lookup"><span data-stu-id="24ff1-103">RemoveRegistryValues Action</span></span>

<span data-ttu-id="24ff1-104">L'azione RemoveRegistryValues può rimuovere solo i valori dal registro di sistema che sono stati creati nella [tabella del registro](registry-table.md) di sistema o nella [tabella RemoveRegistry](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="24ff1-104">The RemoveRegistryValues action can only remove values from the system registry that have been authored into the [Registry table](registry-table.md) or the [RemoveRegistry table](removeregistry-table.md).</span></span> <span data-ttu-id="24ff1-105">Questa azione rimuove un valore del registro di sistema che è stato creato nella tabella del registro di sistema se il componente associato è stato installato localmente o come eseguito dall'origine ed è ora impostato per la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="24ff1-105">This action removes a registry value that has been authored into the Registry table if the associated component was installed locally or as run from source and is now set to be uninstalled.</span></span> <span data-ttu-id="24ff1-106">Questa azione rimuove un valore del registro di sistema che è stato creato nella tabella RemoveRegistry se il componente associato è impostato per essere installato localmente o come eseguito dall'origine.</span><span class="sxs-lookup"><span data-stu-id="24ff1-106">This action removes a registry value that has been authored into the RemoveRegistry table if the associated component is set to be installed locally or as run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="24ff1-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="24ff1-107">Sequence Restrictions</span></span>

<span data-ttu-id="24ff1-108">L'azione [InstallValidate](installvalidate-action.md) deve essere chiamata prima di chiamare RemoveRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="24ff1-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveRegistryValues.</span></span> <span data-ttu-id="24ff1-109">Se viene usata un'azione [WriteRegistryValori consente](writeregistryvalues-action.md) , deve provenire dopo RemoveRegistryValues.</span><span class="sxs-lookup"><span data-stu-id="24ff1-109">If a [WriteRegistryValues](writeregistryvalues-action.md) action is used, it must come after RemoveRegistryValues.</span></span> <span data-ttu-id="24ff1-110">RemoveRegistryValues deve essere precedente a [UnregisterMIMEInfo](unregistermimeinfo-action.md) o [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="24ff1-110">RemoveRegistryValues must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) or [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span></span>

<span data-ttu-id="24ff1-111">È possibile utilizzare un'azione personalizzata per aggiungere righe alla [tabella del registro di sistema](registry-table.md) durante un'installazione, una disinstallazione o una transazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="24ff1-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="24ff1-112">Queste righe non vengono mantenute nella tabella del registro di sistema e le informazioni sono disponibili solo durante la transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="24ff1-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="24ff1-113">L'azione personalizzata deve pertanto essere eseguita in ogni installazione, disinstallazione o ripristino della transazione che richiede le informazioni contenute in queste righe aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="24ff1-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="24ff1-114">L'azione personalizzata deve precedere le azioni RemoveRegistryValues e [WriteRegistryValori consente](writeregistryvalues-action.md) nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="24ff1-114">The custom action must come before the RemoveRegistryValues and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="24ff1-115">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="24ff1-115">ActionData Messages</span></span>



| <span data-ttu-id="24ff1-116">Campo</span><span class="sxs-lookup"><span data-stu-id="24ff1-116">Field</span></span> | <span data-ttu-id="24ff1-117">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="24ff1-117">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="24ff1-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="24ff1-118">\[1\]</span></span> | <span data-ttu-id="24ff1-119">Percorso del registro di sistema della chiave del valore del registro di sistema rimosso.</span><span class="sxs-lookup"><span data-stu-id="24ff1-119">Registry path to key of removed registry value.</span></span>     |
| <span data-ttu-id="24ff1-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="24ff1-120">\[2\]</span></span> | <span data-ttu-id="24ff1-121">Stringa formattata di nome del valore del registro di sistema rimosso.</span><span class="sxs-lookup"><span data-stu-id="24ff1-121">Formatted string of name of removed registry value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="24ff1-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="24ff1-122">Remarks</span></span>

<span data-ttu-id="24ff1-123">Per rimuovere un valore del registro di sistema, registrare il valore nella colonna valore della tabella del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="24ff1-123">To remove a registry value, record the value in the Value column of the Registry table.</span></span> <span data-ttu-id="24ff1-124">Se l'azione WriteRegistryValori consente ha collegato le \_ \_ stringhe reg multisz al valore nella [tabella del registro di sistema](registry-table.md), l'azione RemoveRegistryValues rimuove solo le stringhe dal valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="24ff1-124">If the WriteRegistryValues action has attached REG\_MULTI\_SZ strings to the value in the [Registry table](registry-table.md), then the RemoveRegistryValues action removes only those strings from the registry value.</span></span>

 

 



