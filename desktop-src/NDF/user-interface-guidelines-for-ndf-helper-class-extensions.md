---
title: Linee guida dell'interfaccia utente per le estensioni della classe helper NDF
description: Quando si compila la classe helper, è necessario creare il testo per aiutare l'utente a comprendere la ragione di un evento imprevisto e le possibili operazioni di ripristino che possono essere eseguite.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104335407"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a><span data-ttu-id="b9b8a-103">Linee guida dell'interfaccia utente per le estensioni della classe helper NDF</span><span class="sxs-lookup"><span data-stu-id="b9b8a-103">UI guidelines for NDF helper class extensions</span></span>

<span data-ttu-id="b9b8a-104">Quando si compila la classe helper, è necessario creare il testo per aiutare l'utente a comprendere la ragione di un evento imprevisto e le possibili operazioni di ripristino che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-104">When building your helper class, you will need to create text to help the user understand the cause of an incident and the possible repair steps which can be taken.</span></span>

## <a name="root-cause-and-repair"></a><span data-ttu-id="b9b8a-105">Causa radice e ripristino</span><span class="sxs-lookup"><span data-stu-id="b9b8a-105">Root Cause and Repair</span></span>

<span data-ttu-id="b9b8a-106">Quando si verifica un evento imprevisto, viene visualizzata una finestra di dialogo che informa l'utente di cosa è accaduto.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-106">When an incident occurs, a dialog box will appear to inform the user about what has happened.</span></span> <span data-ttu-id="b9b8a-107">Il testo creato verrà visualizzato in due aree separate.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-107">The text that you create will appear in two separate areas.</span></span>

-   <span data-ttu-id="b9b8a-108">**Causa radice**: breve descrizione della causa del problema.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-108">**Root Cause**: A brief description of the cause of the issue.</span></span> <span data-ttu-id="b9b8a-109">Contiene informazioni che consentono a un amministratore o a un utente avanzato di risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-109">Contains information to help an administrator or advanced user troubleshoot the problem.</span></span>
-   <span data-ttu-id="b9b8a-110">**Correzione**: espande la causa radice per fornire altri dettagli sui passaggi che possono essere eseguiti da un utente senza troppo tempo.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-110">**Repair**: Expands on the root cause to provide more details about the steps that a user can take, without getting too lengthy.</span></span>

<span data-ttu-id="b9b8a-111">Ogni causa radice o correzione deve avere un titolo e una descrizione.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-111">Each root cause or repair should have a title and a description.</span></span> <span data-ttu-id="b9b8a-112">Tutto il testo prima del primo \\ carattere "n" verrà usato per il titolo.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-112">All text before the first "\\n" character will be used for the title.</span></span> <span data-ttu-id="b9b8a-113">Per la descrizione verrà usato tutto il testo che segue il primo \\ carattere "n", comprese le interruzioni di riga successive.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-113">All text following the first "\\n" character (including any subsequent line breaks) will be used for the description.</span></span>

## <a name="title-guidelines"></a><span data-ttu-id="b9b8a-114">Linee guida sul titolo</span><span class="sxs-lookup"><span data-stu-id="b9b8a-114">Title Guidelines</span></span>

<span data-ttu-id="b9b8a-115">Il titolo di una causa radice o di un ripristino deve attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9b8a-115">The title of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="b9b8a-116">Deve avere una lunghezza inferiore a 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-116">Must be 128 characters or fewer.</span></span> <span data-ttu-id="b9b8a-117">(è consigliato 40 caratteri o meno).</span><span class="sxs-lookup"><span data-stu-id="b9b8a-117">(40 characters or less is recommended.)</span></span>
-   <span data-ttu-id="b9b8a-118">Non deve terminare con un punto.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-118">Should not end with a period.</span></span>

## <a name="description-guidelines"></a><span data-ttu-id="b9b8a-119">Linee guida per la descrizione</span><span class="sxs-lookup"><span data-stu-id="b9b8a-119">Description Guidelines</span></span>

<span data-ttu-id="b9b8a-120">La descrizione di una causa radice o di un ripristino deve attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9b8a-120">The description of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="b9b8a-121">Deve avere una lunghezza inferiore a 512 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-121">Must be 512 characters or fewer.</span></span>
-   <span data-ttu-id="b9b8a-122">Ogni frase deve terminare con un punto.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-122">Each sentence should end with a period.</span></span>
-   <span data-ttu-id="b9b8a-123">Il \\ carattere "n" può essere utilizzato per creare un'interruzioni di riga nella descrizione.</span><span class="sxs-lookup"><span data-stu-id="b9b8a-123">The "\\n" character may be used to create a line break in the description.</span></span>

 

 




