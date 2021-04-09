---
description: Se il criterio di sistema per utente è impostato su &\# 0034; 1&\# 0034;, gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non possono utilizzare la finestra di dialogo Sfoglia per visualizzare le origini multimediali, ad esempio CD-ROM, per le origini di altri prodotti installabili.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968844"
---
# <a name="disablemedia"></a><span data-ttu-id="82d38-103">DisableMedia</span><span class="sxs-lookup"><span data-stu-id="82d38-103">DisableMedia</span></span>

<span data-ttu-id="82d38-104">Se il [criterio di sistema](system-policy.md) per utente è impostato su "1", per gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non è possibile utilizzare la finestra di dialogo Sfoglia per visualizzare le origini dei file multimediali, ad esempio CD-ROM, per le origini di altri prodotti installabili.</span><span class="sxs-lookup"><span data-stu-id="82d38-104">If this per-user [system policy](system-policy.md) is set to "1", users and administrators running a maintenance installation of one product are prevented from using the Browse Dialog to browse media sources, such as CD-ROM, for the sources of other installable products.</span></span> <span data-ttu-id="82d38-105">L'esplorazione di altri prodotti viene impedita indipendentemente dal fatto che l'installazione venga eseguita con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="82d38-105">Browsing for other products is prevented regardless of whether the installation is done with elevated privileges.</span></span> <span data-ttu-id="82d38-106">È comunque possibile che l'utente reinstalli il prodotto da un supporto se l'utente dispone di un'origine multimediale correttamente etichettata.</span><span class="sxs-lookup"><span data-stu-id="82d38-106">It is still possible for the user to reinstall the product from media if the user has a correctly labeled media source.</span></span>

## <a name="registry-key"></a><span data-ttu-id="82d38-107">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="82d38-107">Registry Key</span></span>

<span data-ttu-id="82d38-108">**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="82d38-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="82d38-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="82d38-109">Data Type</span></span>

<span data-ttu-id="82d38-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="82d38-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="82d38-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="82d38-111">Remarks</span></span>

<span data-ttu-id="82d38-112">Si noti che la proprietà [**DISABLEMEDIA**](-disablemedia.md) ha un effetto diverso rispetto al criterio DISABLEMEDIA.</span><span class="sxs-lookup"><span data-stu-id="82d38-112">Note that the [**DISABLEMEDIA**](-disablemedia.md) property has a different effect than the DisableMedia policy.</span></span> <span data-ttu-id="82d38-113">Se si imposta il criterio di sistema DisableMedia, viene disabilitato solo l'esplorazione delle origini multimediali.</span><span class="sxs-lookup"><span data-stu-id="82d38-113">Setting the DisableMedia system policy, only disables browsing to media sources.</span></span> <span data-ttu-id="82d38-114">L'impostazione della proprietà **DISABLEMEDIA** impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="82d38-114">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="82d38-115">Se l'esplorazione è abilitata, tuttavia, un utente può comunque passare a un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="82d38-115">If browsing is enabled however, a user may still browse to a media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82d38-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82d38-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82d38-117">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="82d38-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



