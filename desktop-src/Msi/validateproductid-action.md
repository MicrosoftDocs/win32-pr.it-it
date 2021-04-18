---
description: L'azione ValidateProductID imposta la proprietà ProductID sull'identificatore completo del prodotto.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Azione ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308171"
---
# <a name="validateproductid-action"></a><span data-ttu-id="b1b0e-103">Azione ValidateProductID</span><span class="sxs-lookup"><span data-stu-id="b1b0e-103">ValidateProductID Action</span></span>

<span data-ttu-id="b1b0e-104">L'azione ValidateProductID imposta la proprietà [**ProductID**](productid.md) sull'identificatore completo del prodotto.</span><span class="sxs-lookup"><span data-stu-id="b1b0e-104">The ValidateProductID action sets the [**ProductID**](productid.md) property to the full product identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b1b0e-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="b1b0e-105">Sequence Restrictions</span></span>

<span data-ttu-id="b1b0e-106">Questa azione deve essere sequenziata prima della creazione guidata interfaccia utente nella [tabella InstallUISequence](installuisequence-table.md) e prima dell' [azione RegisterUser](registeruser-action.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1b0e-106">This action must be sequenced before the user interface wizard in the [InstallUISequence table](installuisequence-table.md) and before the [RegisterUser action](registeruser-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b1b0e-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="b1b0e-107">ActionData Messages</span></span>

<span data-ttu-id="b1b0e-108">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="b1b0e-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1b0e-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1b0e-109">Remarks</span></span>

<span data-ttu-id="b1b0e-110">Il programma di installazione verifica se un prodotto è stato convalidato correttamente controllando la proprietà [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="b1b0e-110">The installer checks whether a product has validated successfully by checking the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="b1b0e-111">Il programma di installazione imposta la proprietà **ProductID** sull'identificatore completo del prodotto dopo una convalida corretta.</span><span class="sxs-lookup"><span data-stu-id="b1b0e-111">The installer sets the **ProductID** property to the full product identifier after a successful validation.</span></span> <span data-ttu-id="b1b0e-112">L'azione ValidateProductID non esegue alcuna operazione se la proprietà **ProductID** è già stata impostata da una convalida corretta o da un altro metodo.</span><span class="sxs-lookup"><span data-stu-id="b1b0e-112">The ValidateProductID action does nothing if the **ProductID** property has already been set by a successful validation or by another method.</span></span>

<span data-ttu-id="b1b0e-113">L'azione ValidateProductID restituisce sempre un esito positivo, indipendentemente dal fatto che l'identificatore del prodotto sia valido, in modo che l'identificatore del prodotto possa essere immesso nella riga di comando la prima volta che il prodotto viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1b0e-113">The ValidateProductID action always returns a success, whether or not the product identifier is valid, so that the product identifier can be entered on the command line the first time the product is run.</span></span>

<span data-ttu-id="b1b0e-114">L'identificatore del prodotto può essere convalidato senza che l'utente debba nuovamente immettere queste informazioni impostando la proprietà [**codice PIDKEY**](pidkey.md) nella riga di comando o utilizzando una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="b1b0e-114">The product identifier can be validated without having the user reenter this information by setting the [**PIDKEY**](pidkey.md) property on the command line or by using a transform.</span></span> <span data-ttu-id="b1b0e-115">La visualizzazione della finestra di dialogo in cui viene richiesto all'utente di immettere l'identificatore del prodotto può quindi essere resa condizionale alla presenza della proprietà [**ProductID**](productid.md) , che viene impostata quando la proprietà **codice PIDKEY** viene convalidata.</span><span class="sxs-lookup"><span data-stu-id="b1b0e-115">The display of the dialog box requesting the user to enter the product identifier can then be made conditional upon the presence of the [**ProductID**](productid.md) property, which is set when the **PIDKEY** property is validated.</span></span>

 

 



