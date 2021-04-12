---
title: Autenticazione (AD DS)
description: Ogni oggetto in Active Directory Domain Services dispone di un descrittore di sicurezza univoco che definisce le autorizzazioni di accesso necessarie per leggere o aggiornare l'oggetto o le sue singole proprietà.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, associazione, autenticazione
- Binding autenticazione AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472699"
---
# <a name="authentication-ad-ds"></a><span data-ttu-id="555d5-105">Autenticazione (AD DS)</span><span class="sxs-lookup"><span data-stu-id="555d5-105">Authentication (AD DS)</span></span>

<span data-ttu-id="555d5-106">Ogni oggetto in Active Directory Domain Services dispone di un descrittore di sicurezza univoco che definisce le autorizzazioni di accesso necessarie per leggere o aggiornare l'oggetto o le sue singole proprietà.</span><span class="sxs-lookup"><span data-stu-id="555d5-106">Every object in Active Directory Domain Services has a unique security descriptor that defines the access permissions that are required to read or update the object or its individual properties.</span></span> <span data-ttu-id="555d5-107">I privilegi di accesso sono determinati dai diritti concessi per l'appartenenza a un account utente o a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="555d5-107">Access privileges are determined by the rights granted to a user's account or group memberships.</span></span>

<span data-ttu-id="555d5-108">Quando un'applicazione viene associata a un oggetto nella directory, i privilegi di accesso dell'applicazione a tale oggetto sono basati sul contesto utente specificato durante l'operazione di associazione.</span><span class="sxs-lookup"><span data-stu-id="555d5-108">When an application binds to an object in the directory, the access privileges that the application has to that object are based on the user context specified during the bind operation.</span></span> <span data-ttu-id="555d5-109">Per le funzioni e i metodi di associazione [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), un'applicazione può usare in modo implicito le credenziali del chiamante, specificare in modo esplicito le credenziali di un account utente oppure usare un contesto utente non autenticato (Guest).</span><span class="sxs-lookup"><span data-stu-id="555d5-109">For the binding functions and methods [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), an application can implicitly use the credentials of the caller, explicitly specify the credentials of a user account, or use an unauthenticated user context (Guest).</span></span>

 

 