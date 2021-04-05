---
description: Al termine della copia shadow, il meccanismo più importante per ottenere l'accesso ai dati del file che contiene consiste nell'usare l'oggetto dispositivo della copia shadow.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Accesso del richiedente ai dati copiati in Shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131266"
---
# <a name="requester-access-to-shadow-copied-data"></a><span data-ttu-id="98eae-103">Accesso del richiedente ai dati copiati in Shadow</span><span class="sxs-lookup"><span data-stu-id="98eae-103">Requester Access to Shadow Copied Data</span></span>

<span data-ttu-id="98eae-104">Al termine della copia shadow, il meccanismo più importante per ottenere l'accesso ai dati del file che contiene consiste nell'usare l' [*oggetto dispositivo*](vssgloss-d.md)della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="98eae-104">Once the shadow copy has completed, the most important mechanism for getting access to the file data it contains is through the use of the shadow copy's [*device object*](vssgloss-d.md).</span></span>

<span data-ttu-id="98eae-105">Il **membro \_ pwszSnapshotDeviceObject m** di una [**struttura \_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) è una stringa che contiene un oggetto dispositivo del volume copiato dall'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="98eae-105">The **m\_pwszSnapshotDeviceObject** member of a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure is a string containing a shadow-copied volume's device object.</span></span> <span data-ttu-id="98eae-106">Un richiedente può ottenere un oggetto **\_ \_ prop dello snapshot VSS** del volume copiato shadow se conosce l' **\_ ID VSS** del volume (GUID di identificazione) e lo passa a [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="98eae-106">A requester can obtain a shadow-copied volume's **VSS\_SNAPSHOT\_PROP** object if it knows the volume's **VSS\_ID** (identifying GUID) and passes it to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="98eae-107">Un richiedente può anche ottenere informazioni sulle proprietà della copia shadow usando il membro **obj. snap** della [**struttura \_ \_ prop dell'oggetto VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (ovvero una struttura di [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) ottenuta usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) per eseguire l'iterazione dell'elenco di oggetti restituiti da una chiamata a [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="98eae-107">A requester can also obtain shadow copy property information by using the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) structure (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

<span data-ttu-id="98eae-108">L'oggetto dispositivo deve essere interpretato come la radice di un volume copiato Shadow.</span><span class="sxs-lookup"><span data-stu-id="98eae-108">The device object should be interpreted as the root of a shadow-copied volume.</span></span> <span data-ttu-id="98eae-109">Per questo motivo, l'oggetto dispositivo non contiene la barra rovesciata (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="98eae-109">For this reason, the device object contains no backslash ("\\").</span></span>

<span data-ttu-id="98eae-110">I percorsi nel volume copiato shadow vengono ottenuti sostituendo la radice del percorso originale con l'oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98eae-110">Paths on the shadow copied volume are obtained by replacing the root of the original path with the device object.</span></span> <span data-ttu-id="98eae-111">Se, ad esempio, si specifica un percorso nel volume originale di "C: \\ database \\ \* . mdb" e un'istanza della [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) di snapProp, è possibile ottenere il percorso nel volume copiato Shadow concatenando snapPropm \_ pwszShadow copyDeviceObject, " \\ " e " \\ database \\ \* . mdb".</span><span class="sxs-lookup"><span data-stu-id="98eae-111">For example, given a path on the original volume of "C:\\DATABASE\\\*.mdb" and a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) instance of snapProp, you would obtain the path on the shadow copied volume by concatenating snapPropm\_pwszShadow copyDeviceObject, "\\", and "\\DATABASE\\\*.mdb".</span></span>

<span data-ttu-id="98eae-112">I set di file VSS potrebbero contenere caratteri jolly nei relativi descrittori di file. Pertanto, il recupero di un elenco completo dei file in una copia shadow gestita da un componente potrebbe richiedere l'uso di metodi come **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.</span><span class="sxs-lookup"><span data-stu-id="98eae-112">The VSS file sets might have wildcard characters in their file descriptors, so obtaining a full list of the files on a shadow copy managed by a component might require the use of methods such as **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>

 

 



