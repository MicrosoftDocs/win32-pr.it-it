---
description: L'elenco spazio su disco consente di calcolare lo spazio su disco necessario per completare le operazioni di installazione.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: Informazioni sull'elenco di Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306520"
---
# <a name="about-the-disk-space-list"></a><span data-ttu-id="33aa6-103">Informazioni sull'elenco di Disk-Space</span><span class="sxs-lookup"><span data-stu-id="33aa6-103">About the Disk-Space List</span></span>

<span data-ttu-id="33aa6-104">L'elenco spazio su disco consente di calcolare lo spazio su disco necessario per completare le operazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="33aa6-104">The disk-space list enables you to calculate the disk space required to complete the installation operations.</span></span> <span data-ttu-id="33aa6-105">Dopo aver creato un elenco di spazio su disco e aggiunto le operazioni su file, è possibile eseguire una query sull'elenco per determinare le unità di destinazione specificate dalle operazioni sui file e lo spazio su disco necessario in ogni unità.</span><span class="sxs-lookup"><span data-stu-id="33aa6-105">After you create a disk-space list and add file operations to it, you can query the list to determine the target drives specified by the file operations, and the disk space required on each drive.</span></span>

<span data-ttu-id="33aa6-106">Confrontando lo spazio necessario per lo spazio disponibile nei dischi di destinazione, è possibile determinare a livello di codice se è disponibile spazio sufficiente per l'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="33aa6-106">By comparing the space required to the space available on the target disks, you can programmatically determine whether sufficient space is available for the current installation.</span></span>

<span data-ttu-id="33aa6-107">È possibile aggiungere o rimuovere operazioni sui file nell'elenco spazio su disco e ricalcolare lo spazio su disco necessario.</span><span class="sxs-lookup"><span data-stu-id="33aa6-107">You can add or remove file operations to the disk-space list and recalculate the disk space required.</span></span> <span data-ttu-id="33aa6-108">Questa funzionalità consente, ad esempio, di scrivere un programma che interagisce con l'utente, consentendo di scegliere i componenti che desiderano installare in base allo spazio su disco necessario.</span><span class="sxs-lookup"><span data-stu-id="33aa6-108">This functionality enables you to, for example, write a program that interacts with the user, allowing him or her to choose what components they want to install based on the disk space required.</span></span>

<span data-ttu-id="33aa6-109">Le funzioni elenco spazio su disco controllano automaticamente le copie dei file preesistenti nel disco di destinazione.</span><span class="sxs-lookup"><span data-stu-id="33aa6-109">The disk-space list functions automatically check for preexisting copies of files on the target disk.</span></span> <span data-ttu-id="33aa6-110">Se viene rilevata una versione precedente del file, le funzioni elenco spazio su disco calcolano lo spazio aggiuntivo necessario per completare le operazioni sui file.</span><span class="sxs-lookup"><span data-stu-id="33aa6-110">If a previous version of the file is found, the disk-space list functions calculate the additional space required to complete the file operations.</span></span>

<span data-ttu-id="33aa6-111">Se, ad esempio, un'operazione di copia specifica che un file a 6000 byte deve essere copiato nell'unità C e la versione 2000 byte di tale file esiste già nell'unità C, le funzioni di spazio su disco restituiranno uno spazio obbligatorio di 4000 byte.</span><span class="sxs-lookup"><span data-stu-id="33aa6-111">For example, if a copy operation specifies that a 6000-byte file be copied to drive C, and a 2000-byte version of that file already exists on the drive C, the disk space functions would return a required space of 4000 bytes.</span></span> <span data-ttu-id="33aa6-112">Lo spazio aggiuntivo viene usato per sostituire la versione precedente del file con la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="33aa6-112">The additional space is used to replace the older version of the file with the newer version.</span></span>

<span data-ttu-id="33aa6-113">L'elenco spazio su disco consente di eseguire il rounding dei file di dimensioni ai limiti del cluster di dischi.</span><span class="sxs-lookup"><span data-stu-id="33aa6-113">The disk-space list functions round file sizes to the disk cluster boundaries.</span></span>

 

 



