---
title: Avvio con misurazioni
description: Avvio con misurazioni
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccbba6e5f96fd91c00c295c4b15cab8849f11dc
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730738"
---
# <a name="measured-boot"></a><span data-ttu-id="49466-103">Avvio con misurazioni</span><span class="sxs-lookup"><span data-stu-id="49466-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="49466-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="49466-104">Platforms</span></span>

 <span data-ttu-id="49466-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="49466-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="49466-106">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49466-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="49466-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49466-107">Description</span></span>

<span data-ttu-id="49466-108">Poiché il software antimalware (AM) è diventato migliore e migliore nel rilevamento del malware di runtime, anche gli utenti malintenzionati stanno migliorando la creazione di rootkit che possono nascondere il rilevamento.</span><span class="sxs-lookup"><span data-stu-id="49466-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="49466-109">Il rilevamento di malware che inizia nelle prime fasi del ciclo di avvio è una sfida che la maggior parte dei fornitori di AM deve affrontare diligentemente.</span><span class="sxs-lookup"><span data-stu-id="49466-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="49466-110">In genere, creano hack di sistema non supportati dal sistema operativo host e possono effettivamente comportare il posizionamento del computer in uno stato instabile.</span><span class="sxs-lookup"><span data-stu-id="49466-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="49466-111">Fino a questo punto, Windows non ha fornito un metodo efficace per rilevare e risolvere queste minacce iniziali di avvio.</span><span class="sxs-lookup"><span data-stu-id="49466-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="49466-112">In Windows 8 è stata introdotta una nuova funzionalità denominata avvio misurato, che misura ogni componente, dal firmware fino ai driver di avvio, archivia tali misure nel Trusted Platform Module (TPM) nel computer e quindi rende disponibile un log che può essere testato in remoto per verificare lo stato di avvio del client.</span><span class="sxs-lookup"><span data-stu-id="49466-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="49466-113">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="49466-113">Manifestation</span></span>

<span data-ttu-id="49466-114">La funzionalità di avvio misurato fornisce il software AM con un registro attendibile (resistente a spoofing e manomissioni) di tutti i componenti di avvio avviati prima del software AM.</span><span class="sxs-lookup"><span data-stu-id="49466-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="49466-115">Il software AM può utilizzare il log per determinare se i componenti eseguiti prima di essere attendibili o se sono infetti da malware.</span><span class="sxs-lookup"><span data-stu-id="49466-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="49466-116">Il software AM nel computer locale può inviare il log a un server remoto per la valutazione.</span><span class="sxs-lookup"><span data-stu-id="49466-116">The AM software on the local machine can send the log to a remote sever for evaluation.</span></span> <span data-ttu-id="49466-117">Il server remoto può avviare azioni correttive interagendo con il software sul client o tramite meccanismi fuori banda, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="49466-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="49466-118">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="49466-118">Mitigation</span></span>

<span data-ttu-id="49466-119">Negli scenari aziendali, l'amministratore di sistema ha il controllo del modo in cui vengono usate le informazioni di avvio misurate.</span><span class="sxs-lookup"><span data-stu-id="49466-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="49466-120">Negli scenari dell'utente finale, ad esempio il servizio online banking, il consumer deve acconsentire esplicitamente all'uso dell'avvio misurato per il servizio specifico.</span><span class="sxs-lookup"><span data-stu-id="49466-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="49466-121">Soluzione</span><span class="sxs-lookup"><span data-stu-id="49466-121">Solution</span></span>

<span data-ttu-id="49466-122">Viene preparata una white paper che descrive in dettaglio le API e le chiamate di funzione che devono essere eseguite per diversi scenari di avvio misurato.</span><span class="sxs-lookup"><span data-stu-id="49466-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




