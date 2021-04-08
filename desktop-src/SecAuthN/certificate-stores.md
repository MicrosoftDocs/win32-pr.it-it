---
description: I certificati client e server devono essere archiviati in un archivio certificati accessibile dal processo dell'applicazione.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049769"
---
# <a name="certificate-stores"></a><span data-ttu-id="19877-103">Archivi certificati</span><span class="sxs-lookup"><span data-stu-id="19877-103">Certificate Stores</span></span>

<span data-ttu-id="19877-104">I certificati [*client*](/windows/desktop/SecGloss/c-gly) e [*Server*](/windows/desktop/SecGloss/s-gly) devono essere archiviati in un [*archivio certificati*](/windows/desktop/SecGloss/c-gly) accessibile dal processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19877-104">Both [*client*](/windows/desktop/SecGloss/c-gly) and [*server certificates*](/windows/desktop/SecGloss/s-gly) must be stored in a [*certificate store*](/windows/desktop/SecGloss/c-gly) accessible by the application process.</span></span> <span data-ttu-id="19877-105">In genere, si tratta dell'archivio My, noto anche come archivio personale.</span><span class="sxs-lookup"><span data-stu-id="19877-105">Typically, this is the My store, also known as the personal store.</span></span> <span data-ttu-id="19877-106">Le applicazioni client, ad esempio Internet Explorer, utilizzano in genere l'archivio personale dell'utente corrente, mentre i server come Internet Information Services (IIS) utilizzano il sistema My Store del computer locale.</span><span class="sxs-lookup"><span data-stu-id="19877-106">Client applications such as Internet Explorer normally use the My store of the current user while servers such as Internet Information Services (IIS) use the system My store of the local computer.</span></span>

<span data-ttu-id="19877-107">L'archivio radice e l'archivio [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA) vengono usati quando Schannel o un'applicazione compila una catena di certificati da inviare al computer remoto.</span><span class="sxs-lookup"><span data-stu-id="19877-107">The Root store and the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) store are used when Schannel or an application builds a certificate chain to be sent to the remote computer.</span></span> <span data-ttu-id="19877-108">Questi archivi vengono usati per convalidare una catena di certificati ricevuta.</span><span class="sxs-lookup"><span data-stu-id="19877-108">These stores are used to validate a received certificate chain.</span></span> <span data-ttu-id="19877-109">Per altre informazioni, vedere [esecuzione dell'autenticazione con Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="19877-109">For more information, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
