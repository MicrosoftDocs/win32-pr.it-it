---
title: Oggetti incorporati (COM)
description: Oggetti incorporati
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118798"
---
# <a name="embedded-objects-com"></a><span data-ttu-id="eb19b-103">Oggetti incorporati (COM)</span><span class="sxs-lookup"><span data-stu-id="eb19b-103">Embedded Objects (COM)</span></span>

<span data-ttu-id="eb19b-104">Un oggetto incorporato viene memorizzato fisicamente nel documento composto insieme a tutte le informazioni necessarie per la gestione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb19b-104">An embedded object is physically stored in the compound document, along with all the information needed to manage the object.</span></span> <span data-ttu-id="eb19b-105">In altre parole, l'oggetto incorporato è effettivamente una parte del documento composto in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="eb19b-105">In other words, the embedded object is actually a part of the compound document in which it resides.</span></span> <span data-ttu-id="eb19b-106">Questa disposizione presenta alcuni svantaggi.</span><span class="sxs-lookup"><span data-stu-id="eb19b-106">This arrangement has a couple of disadvantages.</span></span> <span data-ttu-id="eb19b-107">In primo luogo, un documento composto contenente oggetti incorporati sarà maggiore di uno contenente gli stessi oggetti dei collegamenti.</span><span class="sxs-lookup"><span data-stu-id="eb19b-107">First, a compound document containing embedded objects will be larger than one containing the same objects as links.</span></span> <span data-ttu-id="eb19b-108">In secondo luogo, le modifiche apportate all'origine di un oggetto incorporato non verranno replicate automaticamente nella copia incorporata e le modifiche apportate alla copia incorporata non verranno riflesse nell'origine, come avviene con un collegamento.</span><span class="sxs-lookup"><span data-stu-id="eb19b-108">Second, changes made to the source of an embedded object will not be automatically replicated in the embedded copy, and changes in the embedded copy will not be reflected in the source, as they are with a link.</span></span>

<span data-ttu-id="eb19b-109">Tuttavia, per determinati scopi, l'incorporamento offre diversi vantaggi rispetto ai collegamenti.</span><span class="sxs-lookup"><span data-stu-id="eb19b-109">Still, for certain purposes, embedding offers several advantages over links.</span></span> <span data-ttu-id="eb19b-110">In primo luogo, gli utenti possono trasferire i documenti composti con oggetti incorporati ad altri computer o altri percorsi nello stesso computer senza suddividere un collegamento.</span><span class="sxs-lookup"><span data-stu-id="eb19b-110">First, users can transfer compound documents with embedded objects to other computers, or other locations on the same computer, without breaking a link.</span></span> <span data-ttu-id="eb19b-111">In secondo luogo, gli utenti possono modificare gli oggetti incorporati senza modificare il contenuto dell'originale.</span><span class="sxs-lookup"><span data-stu-id="eb19b-111">Second, users can edit embedded objects without changing the content of the original.</span></span> <span data-ttu-id="eb19b-112">In alcuni casi, questa separazione è esattamente ciò che è necessario.</span><span class="sxs-lookup"><span data-stu-id="eb19b-112">Sometimes, this separation is precisely what is required.</span></span> <span data-ttu-id="eb19b-113">Terzo, gli oggetti incorporati possono essere attivati sul posto, ovvero l'utente può modificare o manipolare l'oggetto senza dover lavorare in una finestra separata da quella del contenitore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb19b-113">Third, embedded objects can be activated in place, meaning that the user can edit or otherwise manipulate the object without having to work in a separate window from that of the object's container.</span></span> <span data-ttu-id="eb19b-114">Al contrario, quando l'oggetto viene attivato, l'interfaccia utente dell'applicazione contenitore cambia per esporre gli strumenti necessari per la gestione o la modifica dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="eb19b-114">Instead, when the object is activated, the container application's user interface changes to expose those tools that are necessary to manage or modify the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb19b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb19b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb19b-116">Creazione di oggetti collegati e incorporati da dati esistenti</span><span class="sxs-lookup"><span data-stu-id="eb19b-116">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




