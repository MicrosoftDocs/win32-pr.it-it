---
title: Avvio con misurazioni
description: Avvio con misurazioni
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314342"
---
# <a name="measured-boot"></a><span data-ttu-id="d1cba-103">Avvio con misurazioni</span><span class="sxs-lookup"><span data-stu-id="d1cba-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="d1cba-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="d1cba-104">Platforms</span></span>

 <span data-ttu-id="d1cba-105">**Client** - Windows 8</span><span class="sxs-lookup"><span data-stu-id="d1cba-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="d1cba-106">**Server** - Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1cba-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="d1cba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1cba-107">Description</span></span>

<span data-ttu-id="d1cba-108">Poiché il software antimalware (AM) è diventato sempre più in grado di rilevare malware di runtime, anche gli utenti malintenzionati stanno diventando più esperti nella creazione di rootkit che possono nascondersi dal rilevamento.</span><span class="sxs-lookup"><span data-stu-id="d1cba-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="d1cba-109">Il rilevamento di malware che inizia all'inizio del ciclo di avvio è una sfida che la maggior parte dei fornitori am affronta con attenzione.</span><span class="sxs-lookup"><span data-stu-id="d1cba-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="d1cba-110">In genere, creano attacchi di sistema che non sono supportati dal sistema operativo host e possono effettivamente comportare il posizionamento del computer in uno stato instabile.</span><span class="sxs-lookup"><span data-stu-id="d1cba-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="d1cba-111">Fino a questo punto, Windows non ha fornito un modo efficace per am per rilevare e risolvere queste minacce di avvio anticipato.</span><span class="sxs-lookup"><span data-stu-id="d1cba-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="d1cba-112">Windows 8 introduce una nuova funzionalità denominata avvio con misurazioni, che misura ogni componente, dal firmware verso l'alto fino ai driver di avvio, archivia tali misurazioni nel Trusted Platform Module (TPM) nel computer e quindi rende disponibile un log che può essere testato in remoto per verificare lo stato di avvio del client.</span><span class="sxs-lookup"><span data-stu-id="d1cba-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d1cba-113">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="d1cba-113">Manifestation</span></span>

<span data-ttu-id="d1cba-114">La avvio con misurazioni offre al software AM un log attendibile (resistente allo spoofing e alla manomissione) di tutti i componenti di avvio avviati prima del software AM.</span><span class="sxs-lookup"><span data-stu-id="d1cba-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="d1cba-115">Il software AM può usare il log per determinare se i componenti evasi prima di esso sono attendibili o se sono infetti da malware.</span><span class="sxs-lookup"><span data-stu-id="d1cba-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="d1cba-116">Il software AM nel computer locale può inviare il log a un server remoto per la valutazione.</span><span class="sxs-lookup"><span data-stu-id="d1cba-116">The AM software on the local machine can send the log to a remote server for evaluation.</span></span> <span data-ttu-id="d1cba-117">Il server remoto può avviare azioni di correzione interagendo con il software nel client o tramite meccanismi fuori banda, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="d1cba-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="d1cba-118">Mitigazione</span><span class="sxs-lookup"><span data-stu-id="d1cba-118">Mitigation</span></span>

<span data-ttu-id="d1cba-119">Negli scenari aziendali, l'amministratore di sistema ha il controllo avvio con misurazioni vengono usate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="d1cba-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="d1cba-120">Negli scenari degli utenti finali, ad esempio nel settore bancario online, il consumer deve acconsentire esplicitamente all'uso avvio con misurazioni per il servizio specifico.</span><span class="sxs-lookup"><span data-stu-id="d1cba-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="d1cba-121">Soluzione</span><span class="sxs-lookup"><span data-stu-id="d1cba-121">Solution</span></span>

<span data-ttu-id="d1cba-122">È white paper in corso una preparazione che dettagli le API e le chiamate di funzione che devono essere effettuate per vari avvio con misurazioni scenari.</span><span class="sxs-lookup"><span data-stu-id="d1cba-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




