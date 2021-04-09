---
description: ICE90 Invia un avviso se rileva che la directory di un collegamento è stata specificata come proprietà pubblica.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880869"
---
# <a name="ice90"></a><span data-ttu-id="0c8c3-103">ICE90</span><span class="sxs-lookup"><span data-stu-id="0c8c3-103">ICE90</span></span>

<span data-ttu-id="0c8c3-104">ICE90 Invia un avviso se rileva che la directory di un collegamento è stata specificata come proprietà pubblica.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-104">ICE90 posts a warning if it finds that a shortcut's directory has been specified as a public property.</span></span> <span data-ttu-id="0c8c3-105">I nomi delle [proprietà pubbliche](public-properties.md) sono scritti in lettere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-105">The names of [Public Properties](public-properties.md) are written in uppercase letters.</span></span> <span data-ttu-id="0c8c3-106">Un collegamento specificato da una proprietà pubblica potrebbe non funzionare se il valore della proprietà [**ALLUSERS**](allusers.md) cambia.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-106">A shortcut specified by a public property may not work if the value of the [**ALLUSERS**](allusers.md) property changes.</span></span>

<span data-ttu-id="0c8c3-107">Questa azione personalizzata ICE convalida la tabella dei collegamenti e usa la tabella di directory.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-107">This ICE custom action validates the Shortcut table and uses the Directory table.</span></span> <span data-ttu-id="0c8c3-108">Se la tabella di directory non è presente, restituisce senza convalidare la tabella dei collegamenti e non invia alcun errore o avviso.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-108">If the Directory table is not present, it returns without validating the Shortcut table and posts no errors or warnings.</span></span>

## <a name="result"></a><span data-ttu-id="0c8c3-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="0c8c3-109">Result</span></span>

<span data-ttu-id="0c8c3-110">ICE90 invia il seguente avviso.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-110">ICE90 posts the following warning.</span></span>



| <span data-ttu-id="0c8c3-111">Errore ICE90</span><span class="sxs-lookup"><span data-stu-id="0c8c3-111">ICE90 error</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="0c8c3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c8c3-112">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0c8c3-113">Il collegamento ' \[ 1 \] ' contiene una directory che è una proprietà pubblica (tutti i limiti) ed è sotto la directory del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-113">The shortcut '\[1\]' has a directory that is a public property (ALL CAPS) and is under user profile directory.</span></span> <span data-ttu-id="0c8c3-114">Ciò comporta un problema se il valore della proprietà [**ALLUSERS**](allusers.md) cambia nella sequenza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-114">This results in a problem if the value of the [**ALLUSERS**](allusers.md) property changes in the UI sequence.</span></span> | <span data-ttu-id="0c8c3-115">La directory di un collegamento è stata specificata come proprietà pubblica.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-115">A shortcut's directory has been specified as a public property.</span></span> |



 

## <a name="example"></a><span data-ttu-id="0c8c3-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="0c8c3-116">Example</span></span>

<span data-ttu-id="0c8c3-117">ICE90 segnala l'avviso seguente per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="0c8c3-117">ICE90 reports the following warning for the example:</span></span>

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

<span data-ttu-id="0c8c3-118">In questo esempio, MYDIR è in un profilo utente.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-118">In this example, MYDIR is under a users profile.</span></span> <span data-ttu-id="0c8c3-119">ICE90 Invia un avviso perché il percorso della directory di destinazione è specificato da una proprietà pubblica, MYDIR.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-119">ICE90 posts a warning because the location of the target directory is specified by a public property, MYDIR.</span></span> <span data-ttu-id="0c8c3-120">Un utente può modificare la proprietà MYDIR o [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="0c8c3-120">A user may change MYDIR or [**ALLUSERS**](allusers.md) property.</span></span> <span data-ttu-id="0c8c3-121">Se **ALLUSERS** è impostato per il [contesto di installazione](installation-context.md)per computer e mydir è sotto un profilo utenti, il file di collegamento in mydir viene copiato nel profilo "tutti gli utenti" e non in un profilo utente specifico.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-121">If **ALLUSERS** is set for the per-machine [installation context](installation-context.md), and MYDIR is under a users profile, the shortcut file in MYDIR are copied under the "All Users" profile and not a particular user's profile.</span></span> <span data-ttu-id="0c8c3-122">Se **ALLUSERS** è impostato per il contesto di installazione per utente, il file di collegamento in mydir viene copiato nel profilo di un utente specifico e non è disponibile per altri utenti.</span><span class="sxs-lookup"><span data-stu-id="0c8c3-122">If **ALLUSERS** is set for the per-user installation context, the shortcut file in MYDIR is copied into a particular user's profile and is not available to other users.</span></span>

<span data-ttu-id="0c8c3-123">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0c8c3-123">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="0c8c3-124">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="0c8c3-124">Shortcut</span></span>  | <span data-ttu-id="0c8c3-125">Directory\_</span><span class="sxs-lookup"><span data-stu-id="0c8c3-125">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="0c8c3-126">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="0c8c3-126">Shortcut1</span></span> | <span data-ttu-id="0c8c3-127">MYDIR</span><span class="sxs-lookup"><span data-stu-id="0c8c3-127">MYDIR</span></span>       |



 

<span data-ttu-id="0c8c3-128">[Tabella directory](directory-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0c8c3-128">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="0c8c3-129">Directory</span><span class="sxs-lookup"><span data-stu-id="0c8c3-129">Directory</span></span> | <span data-ttu-id="0c8c3-130">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="0c8c3-130">Directory\_Parent</span></span> |
|-----------|-------------------|
| <span data-ttu-id="0c8c3-131">MYDIR</span><span class="sxs-lookup"><span data-stu-id="0c8c3-131">MYDIR</span></span>     | <span data-ttu-id="0c8c3-132">ProgramMenuFolder</span><span class="sxs-lookup"><span data-stu-id="0c8c3-132">ProgramMenuFolder</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0c8c3-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c8c3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c8c3-134">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="0c8c3-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



