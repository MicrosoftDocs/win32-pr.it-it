---
description: PRIMARYFOLDER è una proprietà globale che consente all'autore di designare una cartella primaria per l'installazione.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: Proprietà PRIMARYFOLDER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326259"
---
# <a name="primaryfolder-property"></a><span data-ttu-id="f0eec-103">Proprietà PRIMARYFOLDER</span><span class="sxs-lookup"><span data-stu-id="f0eec-103">PRIMARYFOLDER property</span></span>

<span data-ttu-id="f0eec-104">**PRIMARYFOLDER** è una proprietà globale che consente all'autore di designare una cartella primaria per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f0eec-104">The **PRIMARYFOLDER** is a global property that allows the author to designate a primary folder for the installation.</span></span> <span data-ttu-id="f0eec-105">Il valore di questa proprietà deve essere il nome della chiave di una directory presente nella [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0eec-105">The value for this property must be the key name of a directory that exists in the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="f0eec-106">Il programma di installazione usa il percorso risolto della cartella primaria per determinare il volume da usare per l'impostazione dei valori della proprietà [**PrimaryVolumePath**](primaryvolumepath.md) , della proprietà [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , della proprietà [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) e della proprietà [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) .</span><span class="sxs-lookup"><span data-stu-id="f0eec-106">The installer uses the resolved path of the primary folder to determine which volume to use when setting the values of the [**PrimaryVolumePath**](primaryvolumepath.md) property, [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) property, and [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) property.</span></span> <span data-ttu-id="f0eec-107">Il programma di installazione fornisce i valori di queste ultime proprietà agli utenti nell'interfaccia utente per consentire la gestione dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="f0eec-107">The installer provides the values of these latter properties to users in the user interface to help them manage disk space.</span></span> <span data-ttu-id="f0eec-108">Gli autori di pacchetti di solito possono selezionare la cartella più grande come cartella primaria.</span><span class="sxs-lookup"><span data-stu-id="f0eec-108">Commonly package authors can select the largest folder as the primary folder.</span></span>

<span data-ttu-id="f0eec-109">Il valore di questa proprietà deve essere il nome chiave di un record di directory trovato nella [tabella directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0eec-109">The value for this property must be the key name of a directory record found in the [Directory table](directory-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0eec-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0eec-110">Requirements</span></span>



| <span data-ttu-id="f0eec-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0eec-111">Requirement</span></span> | <span data-ttu-id="f0eec-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f0eec-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0eec-113">Versione</span><span class="sxs-lookup"><span data-stu-id="f0eec-113">Version</span></span><br/> | <span data-ttu-id="f0eec-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f0eec-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f0eec-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f0eec-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f0eec-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0eec-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f0eec-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f0eec-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0eec-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0eec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0eec-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0eec-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




