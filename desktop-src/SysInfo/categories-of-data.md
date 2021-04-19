---
description: "Prima di inserire i dati nel registro di sistema, un'applicazione deve suddividere i dati in due categorie: dati specifici del computer e dati specifici dell'utente."
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorie di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319906"
---
# <a name="categories-of-data"></a><span data-ttu-id="1d71d-103">Categorie di dati</span><span class="sxs-lookup"><span data-stu-id="1d71d-103">Categories of Data</span></span>

<span data-ttu-id="1d71d-104">Prima di inserire i dati nel registro di sistema, un'applicazione deve suddividere i dati in due categorie: dati specifici del computer e dati specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1d71d-104">Before putting data into the registry, an application should divide the data into two categories: computer-specific data and user-specific data.</span></span> <span data-ttu-id="1d71d-105">Con questa distinzione, un'applicazione può supportare più utenti e individuare i dati specifici dell'utente in una rete e usarli in posizioni diverse, permettendo dati di profilo utente indipendenti dalla posizione.</span><span class="sxs-lookup"><span data-stu-id="1d71d-105">By making this distinction, an application can support multiple users, and yet locate user-specific data over a network and use that data in different locations, allowing location-independent user profile data.</span></span> <span data-ttu-id="1d71d-106">Un profilo utente è un set di dati di configurazione salvati per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="1d71d-106">(A user profile is a set of configuration data saved for every user.)</span></span>

<span data-ttu-id="1d71d-107">Quando l'applicazione viene installata, deve registrare i dati specifici del computer sotto la chiave del computer **\_ \_ locale HKEY** .</span><span class="sxs-lookup"><span data-stu-id="1d71d-107">When the application is installed, it should record the computer-specific data under the **HKEY\_LOCAL\_MACHINE** key.</span></span> <span data-ttu-id="1d71d-108">In particolare, deve creare chiavi per il nome della società, il nome del prodotto e il numero di versione, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="1d71d-108">In particular, it should create keys for the company name, product name, and version number, as shown in the following example:</span></span>

<span data-ttu-id="1d71d-109">**HKEY \_ \_Computer locale \\ software \\**_MyCompany MyCompany \\ \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="1d71d-109">**HKEY\_LOCAL\_MACHINE\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

<span data-ttu-id="1d71d-110">Se l'applicazione supporta COM, deve registrare i dati nelle **\_ \_ \\ \\ classi del software del computer locale HKEY**.</span><span class="sxs-lookup"><span data-stu-id="1d71d-110">If the application supports COM, it should record that data under **HKEY\_LOCAL\_MACHINE\\Software\\Classes**.</span></span>

<span data-ttu-id="1d71d-111">Un'applicazione deve registrare i dati specifici dell'utente con la chiave **\_ \_ utente corrente di HKEY** , come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="1d71d-111">An application should record user-specific data under the **HKEY\_CURRENT\_USER** key, as shown in the following example:</span></span>

<span data-ttu-id="1d71d-112">**HKEY \_ \_ \\ Software \\ utente corrente**_produttore MyCompany \\ \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="1d71d-112">**HKEY\_CURRENT\_USER\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

 

 



