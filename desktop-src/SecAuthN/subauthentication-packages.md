---
description: I pacchetti di autenticazione forniti con Windows supportano la personalizzazione usando i pacchetti di autenticazione.
ms.assetid: e1f202c2-8574-4193-a99a-3922a4446013
title: Pacchetti di sottoautenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f0d96a971c35d33002bdab8a23cb5e59207193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309986"
---
# <a name="subauthentication-packages"></a><span data-ttu-id="49bd4-103">Pacchetti di sottoautenticazione</span><span class="sxs-lookup"><span data-stu-id="49bd4-103">Subauthentication Packages</span></span>

<span data-ttu-id="49bd4-104">I [*pacchetti di autenticazione*](../secgloss/a-gly.md) forniti con Windows supportano la personalizzazione usando i [*pacchetti di autenticazione*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="49bd4-104">The [*authentication packages*](../secgloss/a-gly.md) provided with Windows support customization using [*subauthentication packages*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="49bd4-105">Un pacchetto di sottoautenticazione è una DLL che integra o sostituisce parte dei criteri di autenticazione e di convalida utilizzati dal pacchetto di autenticazione principale.</span><span class="sxs-lookup"><span data-stu-id="49bd4-105">A subauthentication package is a DLL that supplements or replaces part of the authentication and validation criteria used by the main authentication package.</span></span> <span data-ttu-id="49bd4-106">Ad esempio, un particolare server può fornire un pacchetto di sottoautenticazione che convalida la password di un utente con un algoritmo diverso o specifica restrizioni per la workstation in un formato diverso.</span><span class="sxs-lookup"><span data-stu-id="49bd4-106">For example, a particular server might supply a subauthentication package that validates a user's password with a different algorithm or specifies workstation restrictions in a different format.</span></span>

<span data-ttu-id="49bd4-107">Per ulteriori informazioni sui pacchetti di sottoautenticazione, vedere l'esempio di subauth installato con Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="49bd4-107">For more information about subauthentication packages, see the SubAuth sample installed with the Platform Software Development Kit (SDK).</span></span>

 

 
