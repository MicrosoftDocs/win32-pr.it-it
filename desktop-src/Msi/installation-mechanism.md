---
description: "Ci sono due fasi per un processo di installazione completato: acquisizione ed esecuzione. Se l'installazione ha esito negativo, è possibile che si verifichi una fase di rollback."
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Meccanismo di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308902"
---
# <a name="installation-mechanism"></a><span data-ttu-id="c18dc-104">Meccanismo di installazione</span><span class="sxs-lookup"><span data-stu-id="c18dc-104">Installation Mechanism</span></span>

<span data-ttu-id="c18dc-105">Ci sono due fasi per un processo di installazione completato: acquisizione ed esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c18dc-105">There are two phases to a successful installation process: acquisition and execution.</span></span> <span data-ttu-id="c18dc-106">Se l'installazione ha esito negativo, è possibile che si verifichi una fase di rollback.</span><span class="sxs-lookup"><span data-stu-id="c18dc-106">If the installation is unsuccessful, a rollback phase may occur.</span></span>

## <a name="acquisition"></a><span data-ttu-id="c18dc-107">Acquisizione</span><span class="sxs-lookup"><span data-stu-id="c18dc-107">Acquisition</span></span>

<span data-ttu-id="c18dc-108">All'inizio della fase di acquisizione, un'applicazione o un utente indica al programma di installazione di installare una funzionalità o un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c18dc-108">At the beginning of the acquisition phase, an application or a user instructs the installer to install a feature or an application.</span></span> <span data-ttu-id="c18dc-109">Il programma di installazione procede quindi attraverso le azioni specificate nelle tabelle di sequenza del database di installazione.</span><span class="sxs-lookup"><span data-stu-id="c18dc-109">The installer then progresses through the actions specified in the sequence tables of the installation database.</span></span> <span data-ttu-id="c18dc-110">Queste azioni eseguono una query sul database di installazione e generano uno script che fornisce una procedura dettagliata per l'esecuzione dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="c18dc-110">These actions query the installation database and generate a script that gives a step-by-step procedure for performing the installation.</span></span>

## <a name="execution"></a><span data-ttu-id="c18dc-111">Esecuzione</span><span class="sxs-lookup"><span data-stu-id="c18dc-111">Execution</span></span>

<span data-ttu-id="c18dc-112">Durante la fase di esecuzione, il programma di installazione passa le informazioni a un processo con privilegi elevati ed esegue lo script.</span><span class="sxs-lookup"><span data-stu-id="c18dc-112">During the execution phase, the installer passes the information to a process with elevated privileges and runs the script.</span></span>

## <a name="rollback"></a><span data-ttu-id="c18dc-113">Rollback</span><span class="sxs-lookup"><span data-stu-id="c18dc-113">Rollback</span></span>

<span data-ttu-id="c18dc-114">Se un'installazione ha esito negativo, il programma di installazione ripristina lo stato originale del computer.</span><span class="sxs-lookup"><span data-stu-id="c18dc-114">If an installation is unsuccessful, the installer restores the original state of the computer.</span></span> <span data-ttu-id="c18dc-115">Quando il programma di installazione elabora lo script di installazione, genera contemporaneamente uno script di rollback.</span><span class="sxs-lookup"><span data-stu-id="c18dc-115">When the installer processes the installation script it simultaneously generates a rollback script.</span></span> <span data-ttu-id="c18dc-116">Oltre allo script di rollback, il programma di installazione salva una copia di tutti i file eliminati durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c18dc-116">In addition to the rollback script, the installer saves a copy of every file it deletes during the installation.</span></span> <span data-ttu-id="c18dc-117">Questi file vengono conservati in una directory di sistema nascosta.</span><span class="sxs-lookup"><span data-stu-id="c18dc-117">These files are kept in a hidden, system directory.</span></span> <span data-ttu-id="c18dc-118">Al termine dell'installazione, vengono eliminati lo script di rollback e i file salvati.</span><span class="sxs-lookup"><span data-stu-id="c18dc-118">Once the installation is complete, the rollback script and the saved files are deleted.</span></span> <span data-ttu-id="c18dc-119">Per ulteriori informazioni, vedere [rollback Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="c18dc-119">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



