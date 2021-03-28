---
description: Un profilo utente obbligatorio è un tipo speciale di profilo utente mobile preconfigurato che gli amministratori possono usare per specificare le impostazioni per gli utenti.
title: Profili utente obbligatori
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524425"
---
# <a name="mandatory-user-profiles"></a><span data-ttu-id="c0e3c-103">Profili utente obbligatori</span><span class="sxs-lookup"><span data-stu-id="c0e3c-103">Mandatory User Profiles</span></span>

<span data-ttu-id="c0e3c-104">Un profilo utente obbligatorio è un tipo speciale di [profilo utente mobile](roaming-user-profiles.md) preconfigurato che gli amministratori possono usare per specificare le impostazioni per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-104">A mandatory user profile is a special type of pre-configured [roaming user profile](roaming-user-profiles.md) that administrators can use to specify settings for users.</span></span> <span data-ttu-id="c0e3c-105">Con i profili utente obbligatori, un utente può modificare il proprio desktop, ma le modifiche non vengono salvate quando l'utente si disconnette.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-105">With mandatory user profiles, a user can modify his or her desktop, but the changes are not saved when the user logs off.</span></span> <span data-ttu-id="c0e3c-106">Al successivo accesso dell'utente, verrà scaricato il profilo utente obbligatorio creato dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-106">The next time the user logs on, the mandatory user profile created by the administrator is downloaded.</span></span> <span data-ttu-id="c0e3c-107">Esistono due tipi di profili obbligatori: i profili *obbligatori normali* e i profili *Super-obbligatori* .</span><span class="sxs-lookup"><span data-stu-id="c0e3c-107">There are two types of mandatory profiles: *normal mandatory* profiles and *super-mandatory* profiles.</span></span>

<span data-ttu-id="c0e3c-108">I profili utente diventano profili obbligatori quando l'amministratore Rinomina il file NTuser. dat (hive del registro di sistema) nel server in NTuser. Man.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-108">User profiles become mandatory profiles when the administrator renames the NTuser.dat file (the registry hive) on the server to NTuser.man.</span></span> <span data-ttu-id="c0e3c-109">L'estensione. Man fa in modo che il profilo utente sia un profilo di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-109">The .man extension causes the user profile to be a read-only profile.</span></span>

<span data-ttu-id="c0e3c-110">I profili utente diventano *estremamente obbligatori* quando il nome della cartella del percorso del profilo termina con. Man; ad esempio, \\ \\ server \\ share \\ mandatoryprofile. man \\ .</span><span class="sxs-lookup"><span data-stu-id="c0e3c-110">User profiles become *super-mandatory* when the folder name of the profile path ends in .man; for example, \\\\server\\share\\mandatoryprofile.man\\.</span></span>

<span data-ttu-id="c0e3c-111">I profili utente super-obbligatori sono simili ai normali profili obbligatori, ad eccezione del caso in cui gli utenti che dispongono di profili Super obbligatori non possano accedere quando il server in cui è archiviato il profilo obbligatorio non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-111">Super-mandatory user profiles are similar to normal mandatory profiles, with the exception that users who have super-mandatory profiles cannot log on when the server that stores the mandatory profile is unavailable.</span></span> <span data-ttu-id="c0e3c-112">Gli utenti con profili obbligatori normali possono accedere con la copia memorizzata nella cache locale del profilo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-112">Users with normal mandatory profiles can log on with the locally cached copy of the mandatory profile.</span></span>

<span data-ttu-id="c0e3c-113">Solo gli amministratori di sistema possono apportare modifiche ai profili utente obbligatori.</span><span class="sxs-lookup"><span data-stu-id="c0e3c-113">Only system administrators can make changes to mandatory user profiles.</span></span>

 

 



