---
title: Tipi di utente sconosciuti
description: Tipi di utente sconosciuti
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339398"
---
# <a name="unknown-user-types"></a><span data-ttu-id="5c3d0-103">Tipi di utente sconosciuti</span><span class="sxs-lookup"><span data-stu-id="5c3d0-103">Unknown User Types</span></span>

<span data-ttu-id="5c3d0-104">È possibile semplificare la localizzazione dei prodotti aggiungendo la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-104">You can ease product localization by adding the following registry key:</span></span>

<span data-ttu-id="5c3d0-105">**HKEY \_ \_Computer locali \\ software \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *UserType*</span><span class="sxs-lookup"><span data-stu-id="5c3d0-105">**HKEY\_LOCAL\_MACHINES\\SOFTWARE\\Microsoft\\OLE2**\\**UnknownUserType** = *usertype*</span></span>

<span data-ttu-id="5c3d0-106">Questa chiave consente alle funzioni di restituire una stringa specificata anziché un valore predefinito "Unknown", consentendo ai localizzatori di specificare un tipo di utente di una lingua diversa.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-106">This key allows functions to return a specified string rather than a default value of "Unknown", enabling localizers to specify a user type of a different language.</span></span>

<span data-ttu-id="5c3d0-107">L'implementazione del gestore predefinito COM di [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) esamina il registro di sistema chiamando [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="5c3d0-107">The COM default handler's implementation of [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examines the registry by calling [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span> <span data-ttu-id="5c3d0-108">Se la classe dell'oggetto non viene trovata nel registro di sistema, viene restituito il tipo di utente dall'istanza [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-108">If the object's class is not found in the registry, the user type from the object's [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) instance is returned.</span></span> <span data-ttu-id="5c3d0-109">Se la classe non viene trovata nell'istanza di **IStorage** dell'oggetto, viene restituita la stringa "Unknown".</span><span class="sxs-lookup"><span data-stu-id="5c3d0-109">If the class is not found in the object's **IStorage** instance, the string "Unknown" is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c3d0-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c3d0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c3d0-111">Registrazione di applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="5c3d0-111">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 