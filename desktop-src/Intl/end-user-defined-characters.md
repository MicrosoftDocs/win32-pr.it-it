---
description: I caratteri definiti dall'utente finale (EUDC) nei set di caratteri a doppio byte (DBCS) e nei caratteri PUA (private use area) in Unicode sono caratteri personalizzati.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caratteri dell'area uso privato e definiti dall'utente finale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348141"
---
# <a name="end-user-defined-and-private-use-area-characters"></a><span data-ttu-id="c6766-103">Caratteri dell'area uso privato e definiti dall'utente finale</span><span class="sxs-lookup"><span data-stu-id="c6766-103">End-User-Defined and Private Use Area Characters</span></span>

<span data-ttu-id="c6766-104">I caratteri definiti dall'utente finale (EUDC) nei [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS) e nei caratteri PUA (private use area) in [Unicode](unicode.md) sono caratteri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="c6766-104">End-user-defined characters (EUDC) in [double-byte character sets](double-byte-character-sets.md) (DBCSs) and private use area (PUA) characters in [Unicode](unicode.md) are custom characters.</span></span> <span data-ttu-id="c6766-105">Possono essere definiti e implementati da un utente finale o da un'altra parte, ad esempio un produttore di apparecchiature, un gruppo di utenti, un corpo del governo o una società di progettazione dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="c6766-105">They can be defined and implemented either by an end user or by another party, such as an equipment manufacturer, a user group, a government body, or a font design company.</span></span> <span data-ttu-id="c6766-106">Il loro utilizzo consente agli utenti di creare nomi e altre parole utilizzando caratteri non disponibili nei tipi di carattere standard e della stampante.</span><span class="sxs-lookup"><span data-stu-id="c6766-106">Their use enables users to form names and other words using characters that are not available in standard screen and printer fonts.</span></span>

<span data-ttu-id="c6766-107">I caratteri EUDC e PUA possono essere assegnati in modo diverso o non assegnati in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="c6766-107">The EUDC and PUA characters can be assigned differently, or not assigned at all, on different computers.</span></span> <span data-ttu-id="c6766-108">Alcune tabelle codici includono estensioni che riutilizzano l'intervallo di EUDC e queste estensioni possono essere in conflitto tra loro.</span><span class="sxs-lookup"><span data-stu-id="c6766-108">Some code pages have extensions that reuse the EUDC range, and these extensions can conflict with each other.</span></span> <span data-ttu-id="c6766-109">In altri casi, un produttore potrebbe fornire un set di caratteri personalizzato in uno di questi intervalli.</span><span class="sxs-lookup"><span data-stu-id="c6766-109">In other cases, a manufacturer might provide a custom set of characters in one of these ranges.</span></span> <span data-ttu-id="c6766-110">Inoltre, i gruppi di utenti possono tentare di fornire caratteri aggiuntivi in PUA.</span><span class="sxs-lookup"><span data-stu-id="c6766-110">Additionally, user groups can attempt to provide additional characters in the PUA.</span></span> <span data-ttu-id="c6766-111">Diverse combinazioni di questi casi possono causare conflitti.</span><span class="sxs-lookup"><span data-stu-id="c6766-111">Different combinations of these cases can cause conflict.</span></span> <span data-ttu-id="c6766-112">Quando si creano applicazioni che si basano su caratteri EUDC o PUA, è necessario tenere presenti le interpretazioni in conflitto di un singolo punto di codice.</span><span class="sxs-lookup"><span data-stu-id="c6766-112">When creating applications that rely on EUDC or PUA characters, you should keep in mind the conflicting interpretations of an individual code point.</span></span>

<span data-ttu-id="c6766-113">Negli argomenti seguenti vengono illustrati i tipi di carattere che supportano EUDCs, nonché l'accesso e la gestione di questi caratteri:</span><span class="sxs-lookup"><span data-stu-id="c6766-113">The following topics discuss the fonts that support EUDCs, and access and management for these characters:</span></span>

-   [<span data-ttu-id="c6766-114">Set di caratteri e tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="c6766-114">Character Sets and Fonts</span></span>](character-sets-and-fonts.md)
-   [<span data-ttu-id="c6766-115">Voci del registro di sistema EUDC</span><span class="sxs-lookup"><span data-stu-id="c6766-115">EUDC Registry Entries</span></span>](eudc-registry-entries.md)

## <a name="related-topics"></a><span data-ttu-id="c6766-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6766-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6766-117">Informazioni sui set di caratteri e Unicode</span><span class="sxs-lookup"><span data-stu-id="c6766-117">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



