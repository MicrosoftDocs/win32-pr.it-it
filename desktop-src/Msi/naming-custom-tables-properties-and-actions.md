---
description: Gli autori di pacchetti devono assicurarsi che i nomi delle tabelle, delle proprietà o delle azioni personalizzate definite nel pacchetto non siano in conflitto con i nomi delle tabelle, delle proprietà o delle azioni standard native per la Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Denominazione di tabelle, proprietà e azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880726"
---
# <a name="naming-custom-tables-properties-and-actions"></a><span data-ttu-id="7fb0d-103">Denominazione di tabelle, proprietà e azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="7fb0d-103">Naming Custom Tables, Properties, and Actions</span></span>

<span data-ttu-id="7fb0d-104">Gli autori di pacchetti devono assicurarsi che i nomi delle tabelle, delle proprietà o delle azioni personalizzate definite nel pacchetto non siano in conflitto con i nomi delle tabelle, delle proprietà o delle azioni standard native per la Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7fb0d-104">Package authors should ensure that the names of any custom tables, properties, or actions defined in their package will not conflict with the names of standard tables, properties, or actions that are native to the Windows Installer.</span></span>

<span data-ttu-id="7fb0d-105">Gli autori dei pacchetti devono rispettare le linee guida seguenti per i nomi di tabelle, proprietà o azioni personalizzati.</span><span class="sxs-lookup"><span data-stu-id="7fb0d-105">Package authors should adhere to the following guidelines for custom table, property, or action names.</span></span>

-   <span data-ttu-id="7fb0d-106">Creare nomi per le tabelle, le proprietà o le azioni personalizzate con prefisso che identifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fb0d-106">Make names for custom tables, properties, or actions that have a prefix that identifies your application.</span></span>
-   <span data-ttu-id="7fb0d-107">Non usare mai un nome con MSI come prefisso.</span><span class="sxs-lookup"><span data-stu-id="7fb0d-107">Never use a name with Msi as the prefix.</span></span> <span data-ttu-id="7fb0d-108">A partire da Windows Installer 2,0, a tutte le nuove proprietà, azioni e tabelle native Windows Installer sono assegnati nomi con prefisso MSI.</span><span class="sxs-lookup"><span data-stu-id="7fb0d-108">Starting with Windows Installer 2.0, all new native Windows Installer properties, actions, and tables are given names prefixed by Msi.</span></span> <span data-ttu-id="7fb0d-109">Questo prefisso non distingue tra maiuscole e minuscole, ad esempio MsiNewInternalTable.</span><span class="sxs-lookup"><span data-stu-id="7fb0d-109">This prefix is not case sensitive, for example MsiNewInternalTable.</span></span> <span data-ttu-id="7fb0d-110">Poiché il prefisso non distingue tra maiuscole e minuscole, gli autori devono evitare tutti i case del prefisso MSI.</span><span class="sxs-lookup"><span data-stu-id="7fb0d-110">Because the prefix is not case sensitive, authors should avoid all cases of the Msi prefix.</span></span>

<span data-ttu-id="7fb0d-111">Per ulteriori informazioni, vedere [nomi di tabella](table-names.md).</span><span class="sxs-lookup"><span data-stu-id="7fb0d-111">For more information, see [Table Names](table-names.md).</span></span>

 

 



