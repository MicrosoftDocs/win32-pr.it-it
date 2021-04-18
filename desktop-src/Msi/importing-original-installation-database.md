---
description: Iniziare la creazione del pacchetto di aggiornamento copiando il pacchetto di installazione e la struttura di directory di origine del prodotto originale.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importazione del database di installazione originale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314782"
---
# <a name="importing-original-installation-database"></a><span data-ttu-id="c32d5-103">Importazione del database di installazione originale</span><span class="sxs-lookup"><span data-stu-id="c32d5-103">Importing Original Installation Database</span></span>

<span data-ttu-id="c32d5-104">Iniziare la creazione del pacchetto di aggiornamento copiando il pacchetto di installazione e la struttura di directory di origine del prodotto originale.</span><span class="sxs-lookup"><span data-stu-id="c32d5-104">Begin authoring the upgrade package by copying the installation package and source directory tree of the of original product.</span></span> <span data-ttu-id="c32d5-105">Le istruzioni per la creazione del pacchetto di installazione per MNP2000 sono fornite in [un esempio di installazione](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="c32d5-105">Instructions for authoring the installation package for MNP2000 are given in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="c32d5-106">È necessario copiare il contenuto delle cartelle seguenti:</span><span class="sxs-lookup"><span data-stu-id="c32d5-106">You should copy the contents of the following folders:</span></span>

<span data-ttu-id="c32d5-107">C: \\MNP2000.msi di esempio \\</span><span class="sxs-lookup"><span data-stu-id="c32d5-107">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="c32d5-108">C: \\ \\ blocco note di esempio</span><span class="sxs-lookup"><span data-stu-id="c32d5-108">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="c32d5-109">C: \\ \\ file binario di esempio</span><span class="sxs-lookup"><span data-stu-id="c32d5-109">C:\\Sample\\Binary</span></span>\\

<span data-ttu-id="c32d5-110">C: \\ icona di esempio </span><span class="sxs-lookup"><span data-stu-id="c32d5-110">C:\\Sample\\Icon</span></span>\\\\

<span data-ttu-id="c32d5-111">Aggiornare il contenuto della cartella del blocco note in modo che corrisponda all'origine descritta in [pianificazione di un aggiornamento principale](planning-a-major-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="c32d5-111">Update the contents of the Notepad folder so that they match the source described in [Planning a Major Upgrade](planning-a-major-upgrade.md).</span></span> <span data-ttu-id="c32d5-112">Rimuovere tutti i file di origine obsoleti, ad esempio Baseball.txt, e sostituire con i file aggiornati, ad esempio Baseba01.txt.</span><span class="sxs-lookup"><span data-stu-id="c32d5-112">Remove all obsolete source files, such as Baseball.txt, and replace with the updated files, such as Baseba01.txt.</span></span> <span data-ttu-id="c32d5-113">Aggiungere i nuovi file aggiuntivi forniti dall'aggiornamento, ad esempio Opera01.txt.</span><span class="sxs-lookup"><span data-stu-id="c32d5-113">Add the additional new files provided by the upgrade, such as Opera01.txt.</span></span>

<span data-ttu-id="c32d5-114">Rinominare MNP2000.msi in MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="c32d5-114">Rename MNP2000.msi to MNP2001.msi.</span></span> <span data-ttu-id="c32d5-115">Nei passaggi successivi si userà un editor tabelle per modificare il database nel file con estensione msi per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c32d5-115">In subsequent steps you will use a table editor to modify this database into the .msi file for the upgrade.</span></span> <span data-ttu-id="c32d5-116">Le tabelle di database non modificate in modo esplicito nelle sezioni successive sono identiche alle tabelle nel database del prodotto originale, MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="c32d5-116">Database tables that are not explicitly modified in the subsequent sections are identical to the tables in the original product's database, MNP2000.msi.</span></span>

[<span data-ttu-id="c32d5-117">Continua</span><span class="sxs-lookup"><span data-stu-id="c32d5-117">Continue</span></span>](updating-directory-structure-for-an-upgrade.md)

 

 



