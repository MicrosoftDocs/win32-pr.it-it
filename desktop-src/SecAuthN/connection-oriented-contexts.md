---
description: Con un contesto orientato alla connessione, il chiamante della funzione è responsabile della formattazione dei messaggi. Il chiamante si basa sul pacchetto di sicurezza per autenticare le connessioni e per garantire l'integrità di parti specifiche del messaggio.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Contesti di Connection-Oriented
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131054"
---
# <a name="connection-oriented-contexts"></a><span data-ttu-id="1b004-104">Contesti di Connection-Oriented</span><span class="sxs-lookup"><span data-stu-id="1b004-104">Connection-Oriented Contexts</span></span>

<span data-ttu-id="1b004-105">Con un [*contesto*](/windows/desktop/SecGloss/c-gly)orientato alla connessione, il chiamante della funzione è responsabile della formattazione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="1b004-105">With a connection-oriented [*context*](/windows/desktop/SecGloss/c-gly), the function's caller is responsible for formatting messages.</span></span> <span data-ttu-id="1b004-106">Il chiamante si basa sul [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) per autenticare le connessioni e per garantire l'integrità di parti specifiche del messaggio.</span><span class="sxs-lookup"><span data-stu-id="1b004-106">The caller relies on the [*security package*](/windows/desktop/SecGloss/s-gly) to authenticate connections and to ensure the integrity of specific parts of the message.</span></span>

<span data-ttu-id="1b004-107">La maggior parte delle opzioni di contesto sono disponibili per i contesti orientati alla connessione.</span><span class="sxs-lookup"><span data-stu-id="1b004-107">Most context options are available to connection-oriented contexts.</span></span> <span data-ttu-id="1b004-108">Queste opzioni includono l'autenticazione reciproca, il rilevamento della riproduzione e il rilevamento delle sequenze, come descritto in [requisiti di contesto](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1b004-108">These options include mutual authentication, replay detection, and sequence detection, as described in [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="1b004-109">Un pacchetto di sicurezza imposta il \_ flag \_ di connessione del flag SECPKG per indicare che supporta la semantica orientata alla connessione.</span><span class="sxs-lookup"><span data-stu-id="1b004-109">A security package sets the SECPKG\_FLAG\_CONNECTION flag to indicate that it supports connection-oriented semantics.</span></span>

 

 
