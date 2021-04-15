---
description: Rappresentazione del dispositivo
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Rappresentazione del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484740"
---
# <a name="device-representation"></a><span data-ttu-id="aaf40-103">Rappresentazione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="aaf40-103">Device Representation</span></span>

<span data-ttu-id="aaf40-104">I dispositivi hanno due comportamenti principali che vengono risolti dall'architettura dei dispositivi portatili Windows (WPD):</span><span class="sxs-lookup"><span data-stu-id="aaf40-104">Devices have two main behaviors that are addressed by the Windows Portable Devices (WPD) architecture:</span></span>

-   <span data-ttu-id="aaf40-105">Accesso e archiviazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="aaf40-105">Accessing and storing content.</span></span> <span data-ttu-id="aaf40-106">Ad esempio, le applicazioni devono essere in grado di aggiungere file musicali a un lettore musicale portatile.</span><span class="sxs-lookup"><span data-stu-id="aaf40-106">For example, applications must be able to add music files to a portable music player.</span></span>
-   <span data-ttu-id="aaf40-107">Programmazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaf40-107">Programming the device.</span></span> <span data-ttu-id="aaf40-108">Sono incluse operazioni semplici come la modifica delle impostazioni e la preparazione del dispositivo per l'acquisizione dei dati o operazioni più complesse, ad esempio il caricamento del firmware.</span><span class="sxs-lookup"><span data-stu-id="aaf40-108">This includes simple operations such as changing settings and preparing the device for data capture, or more complex operations such as uploading firmware.</span></span> <span data-ttu-id="aaf40-109">Gli esempi includono l'esecuzione di un comando "Take picture" in una fotocamera digitale ancora.</span><span class="sxs-lookup"><span data-stu-id="aaf40-109">Examples include issuing a "Take Picture" command to a digital still camera.</span></span>

<span data-ttu-id="aaf40-110">In WPD questi comportamenti vengono descritti rappresentando il dispositivo come una gerarchia di oggetti.</span><span class="sxs-lookup"><span data-stu-id="aaf40-110">In WPD, these behaviors are described by representing the device as a hierarchy of objects.</span></span> <span data-ttu-id="aaf40-111">La figura seguente mostra una rappresentazione dell'oggetto WPD per un dispositivo multifunzione, che in questo caso è un telefono cellulare.</span><span class="sxs-lookup"><span data-stu-id="aaf40-111">The following illustration shows a WPD object representation for a multi-function device, which in this case is a mobile phone.</span></span>

![illustrazione che mostra la gerarchia di oggetti per un telefono cellulare](images/wpd-overview-figure3.gif)

<span data-ttu-id="aaf40-113">Questa gerarchia illustra le funzionalità e i contenuti seguenti.</span><span class="sxs-lookup"><span data-stu-id="aaf40-113">This hierarchy illustrates the following functionality and contents.</span></span>

<span data-ttu-id="aaf40-114">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="aaf40-114">Functionality:</span></span>

-   <span data-ttu-id="aaf40-115">Oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aaf40-115">Storage object.</span></span> <span data-ttu-id="aaf40-116">Questo dispositivo dispone di archiviazione dati.</span><span class="sxs-lookup"><span data-stu-id="aaf40-116">This device has data storage.</span></span>
-   <span data-ttu-id="aaf40-117">Servizio contatti.</span><span class="sxs-lookup"><span data-stu-id="aaf40-117">Contacts Service.</span></span> <span data-ttu-id="aaf40-118">Questo servizio è un oggetto funzionale che può essere utilizzato per sincronizzare e archiviare contatti sul telefono.</span><span class="sxs-lookup"><span data-stu-id="aaf40-118">This service is a functional object that can be used to synchronize and store contacts on the phone.</span></span>
-   <span data-ttu-id="aaf40-119">Servizio SMS.</span><span class="sxs-lookup"><span data-stu-id="aaf40-119">SMS Service.</span></span> <span data-ttu-id="aaf40-120">Questo servizio è un oggetto funzionale che può essere utilizzato per l'invio, la ricezione e l'archiviazione di messaggi SMS.</span><span class="sxs-lookup"><span data-stu-id="aaf40-120">This service is a functional object that can be used to send, receive, and store SMS messages.</span></span>

<span data-ttu-id="aaf40-121">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="aaf40-121">Contents:</span></span>

-   <span data-ttu-id="aaf40-122">Oggetti multimediali.</span><span class="sxs-lookup"><span data-stu-id="aaf40-122">Media objects.</span></span> <span data-ttu-id="aaf40-123">Questo dispositivo archivia immagini, musica e file video in cartelle nell'oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aaf40-123">This device stores images, music, and video files in folders on the Storage object.</span></span> <span data-ttu-id="aaf40-124">Mentre i file mostrati nell'illustrazione sono archiviati in una cartella, un dispositivo può suddividere il contenuto in cartelle organizzate in base al tipo di supporto archiviato; ad esempio, cartelle immagini, cartelle musica e cartelle video.</span><span class="sxs-lookup"><span data-stu-id="aaf40-124">While the files shown in the illustration are stored under one folder, a device can subdivide content into folders organized by the type of media stored; for example, image folders, music folders, and video folders.</span></span>
-   <span data-ttu-id="aaf40-125">Contattare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="aaf40-125">Contact objects.</span></span> <span data-ttu-id="aaf40-126">Questo dispositivo archivia le informazioni di contatto, ad esempio nome, numero di telefono e indirizzo, come elementi figlio del servizio contatti</span><span class="sxs-lookup"><span data-stu-id="aaf40-126">This device stores contact information (such as name, phone number, and address) as children of the Contacts Service</span></span>
-   <span data-ttu-id="aaf40-127">Oggetti Message.</span><span class="sxs-lookup"><span data-stu-id="aaf40-127">Message objects.</span></span> <span data-ttu-id="aaf40-128">Questo dispositivo archivia i messaggi SMS come elementi figlio del servizio SMS.</span><span class="sxs-lookup"><span data-stu-id="aaf40-128">This device stores SMS messages as children of the SMS Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaf40-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aaf40-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaf40-130">**Panoramica dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="aaf40-130">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



