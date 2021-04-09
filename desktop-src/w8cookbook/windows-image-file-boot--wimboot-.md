---
title: Avvio file immagine Windows (WimBoot)
description: Avvio file immagine Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734642"
---
# <a name="windows-image-file-boot-wimboot"></a><span data-ttu-id="3e948-103">Avvio file immagine Windows (WimBoot)</span><span class="sxs-lookup"><span data-stu-id="3e948-103">Windows Image File Boot (WimBoot)</span></span>

## <a name="platform"></a><span data-ttu-id="3e948-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="3e948-104">Platform</span></span>

<span data-ttu-id="3e948-105">**Client:** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3e948-105">**Clients:** Windows 8.1</span></span>  

## <a name="description"></a><span data-ttu-id="3e948-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e948-106">Description</span></span>

<span data-ttu-id="3e948-107">WimBoot è un metodo alternativo per la distribuzione di Windows da parte degli OEM.</span><span class="sxs-lookup"><span data-stu-id="3e948-107">WimBoot is an alternative way for OEMs to deploy Windows.</span></span> <span data-ttu-id="3e948-108">Una distribuzione di WimBoot avvia ed esegue Windows direttamente da un file di immagine Windows compresso (WIM).</span><span class="sxs-lookup"><span data-stu-id="3e948-108">A WimBoot deployment boots and runs Windows directly out of a compressed Windows Image File (WIM).</span></span> <span data-ttu-id="3e948-109">Questo file WIM non è modificabile e l'accesso a esso è gestito da un nuovo driver di filtro file system (WoF.sys).</span><span class="sxs-lookup"><span data-stu-id="3e948-109">This WIM file is immutable, and access to it is managed by a new file system filter driver (WoF.sys).</span></span>

<span data-ttu-id="3e948-110">Il risultato è una riduzione significativa dello spazio su disco necessario per l'installazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="3e948-110">The result is a significant reduction in the disk space required to install Windows.</span></span>

## <a name="manifestations"></a><span data-ttu-id="3e948-111">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="3e948-111">Manifestations</span></span>

<span data-ttu-id="3e948-112">La maggior parte delle applicazioni deve essere completamente inalterata da WimBoot.</span><span class="sxs-lookup"><span data-stu-id="3e948-112">Most applications should be completely unaffected by WimBoot.</span></span> <span data-ttu-id="3e948-113">Potrebbero essere interessate solo le applicazioni che accedono e sbloccano i file di sistema o i file pre-caricati per l'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="3e948-113">Only applications that access and unlock system files or pre-loaded files for write access may be affected.</span></span> <span data-ttu-id="3e948-114">Poiché il file WIM non è modificabile, gli aggiornamenti (ovvero i file di sistema o pre-caricati) vengono archiviati semplicemente nella partizione C: \\ .</span><span class="sxs-lookup"><span data-stu-id="3e948-114">Since the WIM is immutable, updates to it (that is, system or pre-loaded files) are simply stored on the C:\\ partition.</span></span>

<span data-ttu-id="3e948-115">Se un'applicazione ha sbloccato l'accesso in scrittura per tutti i file di sistema con supporto WIM e i file precaricati, il risparmio fornito da WimBoot verrebbe perso completamente, perché tutti questi file verrebbero decompressi e inseriti nel volume C: \\ .</span><span class="sxs-lookup"><span data-stu-id="3e948-115">If an application unlocked write access for all WIM-backed system and pre-loaded files, the savings that WimBoot delivers would be completely lost, as all of these files would be decompressed and placed on the C:\\ volume.</span></span>

<span data-ttu-id="3e948-116">Inoltre, le applicazioni di backup e ripristino devono essere in grado di riconoscere le distribuzioni di WimBoot, poiché il file WIM è presente in una partizione separata. ovvero, durante il backup, è necessario salvare entrambe le partizioni C: \\ e Wim ed è necessario ripristinare entrambe insieme.</span><span class="sxs-lookup"><span data-stu-id="3e948-116">Furthermore, back-up and restore applications need to be aware of WimBoot deployments, as the WIM is present in a separate partition; that is, on back-up, both the C:\\ and WIM partitions must be saved and both must be restored together.</span></span>

## <a name="solution"></a><span data-ttu-id="3e948-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="3e948-117">Solution</span></span>

<span data-ttu-id="3e948-118">Sono state introdotte nuove API che consentono alle applicazioni di eseguire query direttamente se un volume o un file specifico è supportato da un file WIM.</span><span class="sxs-lookup"><span data-stu-id="3e948-118">New APIs were introduced that allow applications to directly query if a given volume or file is backed by a WIM.</span></span> <span data-ttu-id="3e948-119">Queste informazioni consentono alle applicazioni di prendere decisioni appropriate, ad esempio l'apertura di questi file solo per l'accesso in lettura o l'identificazione di volumi o partizioni di cui è necessario eseguire il backup e il ripristino insieme.</span><span class="sxs-lookup"><span data-stu-id="3e948-119">This information allows applications to make appropriate decisions, such as opening these files only for read access or to identify volumes/partitions that have to be backed up and restored together.</span></span>

## <a name="compatibility-performance-reliability-or-usability-tests"></a><span data-ttu-id="3e948-120">Test di compatibilità, prestazioni, affidabilità o usabilità</span><span class="sxs-lookup"><span data-stu-id="3e948-120">Compatibility, performance, reliability, or usability tests</span></span>

<span data-ttu-id="3e948-121">Gli sviluppatori di applicazioni devono testare il software e gli scenari corrispondenti in un sistema WimBoot, soprattutto se queste applicazioni accedono a file di sistema o precaricati.</span><span class="sxs-lookup"><span data-stu-id="3e948-121">Application developers should test their software and its corresponding scenarios on a WimBoot system, especially if these applications access system or pre-loaded files.</span></span> <span data-ttu-id="3e948-122">È necessario prestare particolare attenzione a una riduzione significativa dello spazio disponibile su disco dopo il completamento di uno scenario.</span><span class="sxs-lookup"><span data-stu-id="3e948-122">Special attention should be paid to a significant reduction in available disk space after a scenario has been completed.</span></span>

 

 




