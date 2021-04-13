---
title: Persistenza della configurazione
description: Persistenza della configurazione
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK, persistenza
- Windows Media Format SDK, persistenza della configurazione
- ASF (Advanced Systems Format), persistenza
- ASF (formato avanzato dei sistemi), persistenza
- ASF (Advanced Systems Format), persistenza della configurazione
- ASF (formato avanzato dei sistemi), persistenza della configurazione
- persistenza della configurazione
- persistenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398630"
---
# <a name="configuration-persistence"></a><span data-ttu-id="9ac19-111">Persistenza della configurazione</span><span class="sxs-lookup"><span data-stu-id="9ac19-111">Configuration Persistence</span></span>

<span data-ttu-id="9ac19-112">Nessuna delle proprietà abilitate per la scrittura descritte in questa documentazione viene salvata da Windows Media SDK.</span><span class="sxs-lookup"><span data-stu-id="9ac19-112">None of the write-enabled properties described in this documentation are saved by the Windows Media SDK.</span></span> <span data-ttu-id="9ac19-113">Ogni applicazione che usa l'SDK deve fornire le proprie procedure di persistenza, se necessario, e richiamare il metodo set appropriato su ogni istanza dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="9ac19-113">Each application that uses the SDK must provide its own persistence procedures as needed and invoke the appropriate set method upon each instance of the SDK.</span></span> <span data-ttu-id="9ac19-114">In questo modo, le modifiche di configurazione apportate da un'applicazione non influiscono su un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="9ac19-114">In this way, configuration changes made by one application do not affect another application.</span></span> <span data-ttu-id="9ac19-115">Ad esempio, la modifica del tempo di buffering in un lettore non influisce su un altro lettore.</span><span class="sxs-lookup"><span data-stu-id="9ac19-115">For example, changing the buffering time in one player does not affect another player.</span></span>

<span data-ttu-id="9ac19-116">L'unica eccezione a questa regola è rappresentata dalle informazioni sulle credenziali.</span><span class="sxs-lookup"><span data-stu-id="9ac19-116">The one exception to this rule is for the credentials information.</span></span> <span data-ttu-id="9ac19-117">Se l'applicazione indica, nell'output restituito dalla chiamata a **AcquireCredentials** , che le informazioni sull'ID utente e sulla password devono essere rese permanente, l'SDK Salva queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="9ac19-117">If the application indicates, in its return from the **AcquireCredentials** call, that the user ID and password information must be persisted, the SDK saves this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ac19-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ac19-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ac19-119">**Implementazione della funzionalità di rete**</span><span class="sxs-lookup"><span data-stu-id="9ac19-119">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="9ac19-120">**Interfaccia IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="9ac19-120">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




