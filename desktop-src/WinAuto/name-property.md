---
title: Proprietà Name
description: La proprietà Name è una stringa utilizzata dai client per identificare, trovare o annunciare un oggetto per l'utente. Tutti gli oggetti supportano la proprietà Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298314"
---
# <a name="name-property"></a><span data-ttu-id="88c95-104">Proprietà Name</span><span class="sxs-lookup"><span data-stu-id="88c95-104">Name Property</span></span>

<span data-ttu-id="88c95-105">La proprietà **Name** è una stringa utilizzata dai client per identificare, trovare o annunciare un oggetto per l'utente.</span><span class="sxs-lookup"><span data-stu-id="88c95-105">The **Name** property is a string used by clients to identify, find, or announce an object for the user.</span></span> <span data-ttu-id="88c95-106">Tutti gli oggetti supportano la proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="88c95-106">All objects support the **Name** property.</span></span>

<span data-ttu-id="88c95-107">Il testo di un controllo Button, ad esempio, è il nome, mentre il nome di una casella di riepilogo o di un controllo di modifica è il testo statico che precede immediatamente il controllo nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="88c95-107">For example, the text on a button control is its name, while the name for a list box or edit control is the static text that immediately precedes the control in the tabbing order.</span></span> <span data-ttu-id="88c95-108">Anche gli oggetti grafici che non visualizzano un nome forniscono testo quando vengono sottoposti a query per la proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="88c95-108">Even graphic objects that do not display a name provide text when queried for the **Name** property.</span></span>

<span data-ttu-id="88c95-109">La proprietà **Name** viene recuperata chiamando [**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span><span class="sxs-lookup"><span data-stu-id="88c95-109">The **Name** property is retrieved by calling [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span></span>

## <a name="selecting-names"></a><span data-ttu-id="88c95-110">Selezione dei nomi</span><span class="sxs-lookup"><span data-stu-id="88c95-110">Selecting Names</span></span>

<span data-ttu-id="88c95-111">Il nome di un oggetto dovrebbe essere intuitivo per consentire agli utenti di comprendere il significato o lo scopo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="88c95-111">An object's name should be intuitive so that users understand the object's meaning or purpose.</span></span> <span data-ttu-id="88c95-112">Inoltre, la proprietà **Name** deve essere univoca rispetto agli oggetti di pari livello nell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="88c95-112">Also, the **Name** property should be unique relative to any sibling objects in the parent.</span></span>

<span data-ttu-id="88c95-113">La navigazione all'interno delle tabelle presenta problemi particolarmente complessi per alcuni utenti.</span><span class="sxs-lookup"><span data-stu-id="88c95-113">Navigation within tables presents especially difficult problems for some users.</span></span> <span data-ttu-id="88c95-114">Gli sviluppatori di server devono pertanto rendere i nomi delle celle di tabella più descrittivi possibili.</span><span class="sxs-lookup"><span data-stu-id="88c95-114">Therefore, server developers should make table cell names as descriptive as possible.</span></span> <span data-ttu-id="88c95-115">Ad esempio, è possibile creare un nome di cella combinando i nomi della riga e della colonna occupata, ad esempio "a1".</span><span class="sxs-lookup"><span data-stu-id="88c95-115">For example, you could create a cell name by combining the names of the row and column it occupies, such as "A1."</span></span> <span data-ttu-id="88c95-116">Tuttavia, in genere è preferibile usare nomi più descrittivi, ad esempio "Nancy, February", dove "Nancy" è la riga corrente e "February" è la colonna corrente.</span><span class="sxs-lookup"><span data-stu-id="88c95-116">However, it is generally better to use more descriptive names, such as "Nancy, February" where "Nancy" is the current row and "February" is the current column.</span></span>

## <a name="delegating-requests"></a><span data-ttu-id="88c95-117">Delega di richieste</span><span class="sxs-lookup"><span data-stu-id="88c95-117">Delegating Requests</span></span>

<span data-ttu-id="88c95-118">Se un oggetto non ha accesso alla proprietà **Name** , delega le richieste al relativo elemento padre, identificandosi in base al relativo ID figlio.</span><span class="sxs-lookup"><span data-stu-id="88c95-118">If an object does not have access to its **Name** property, it delegates requests to its parent, identifying itself by its child ID.</span></span> <span data-ttu-id="88c95-119">Se, ad esempio, un client chiama la proprietà **Name** di un controllo di modifica, il controllo di modifica delega la query al relativo elemento padre, che restituisce il valore del controllo testo statico che etichetta il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="88c95-119">For example, if a client calls an edit control's **Name** property, the edit control delegates the query to its parent, which returns the value of the static text control that labels the edit control.</span></span>

 

 




