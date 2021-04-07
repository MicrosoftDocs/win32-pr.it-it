---
description: Descrive le operazioni di reparse point che è possibile eseguire usando DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Operazioni di reparse point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058042"
---
# <a name="reparse-point-operations"></a><span data-ttu-id="18ccb-103">Operazioni di reparse point</span><span class="sxs-lookup"><span data-stu-id="18ccb-103">Reparse Point Operations</span></span>

<span data-ttu-id="18ccb-104">Per determinare se un file system supporta i reparse point, chiamare la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) ed esaminare il file supporta il flag di bit **\_ \_ reparse \_ Point** .</span><span class="sxs-lookup"><span data-stu-id="18ccb-104">To determine whether a file system supports reparse points, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FILE\_SUPPORTS\_REPARSE\_POINTS** bit flag.</span></span>

<span data-ttu-id="18ccb-105">La funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) consente di impostare, modificare, ottenere e rimuovere i reparse point.</span><span class="sxs-lookup"><span data-stu-id="18ccb-105">The [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function enables you to set, modify, obtain, and remove reparse points.</span></span> <span data-ttu-id="18ccb-106">Nella tabella seguente vengono descritte le operazioni di reparse point che è possibile eseguire utilizzando **DeviceIoControl**.</span><span class="sxs-lookup"><span data-stu-id="18ccb-106">The following table describes the reparse point operations that you can perform using **DeviceIoControl**.</span></span>



| <span data-ttu-id="18ccb-107">Operazione</span><span class="sxs-lookup"><span data-stu-id="18ccb-107">Operation</span></span>                                                           | <span data-ttu-id="18ccb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18ccb-108">Description</span></span>                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18ccb-109">**FSCTL \_ set \_ reparse \_ Point**</span><span class="sxs-lookup"><span data-stu-id="18ccb-109">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | <span data-ttu-id="18ccb-110">Consente al programma chiamante di impostare un nuovo punto di analisi o di modificarne uno esistente.</span><span class="sxs-lookup"><span data-stu-id="18ccb-110">Allows the calling program to set a new reparse point, or to modify an existing one.</span></span><br/> |
| [<span data-ttu-id="18ccb-111">**FSCTL \_ ottenere un \_ punto di analisi \_**</span><span class="sxs-lookup"><span data-stu-id="18ccb-111">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | <span data-ttu-id="18ccb-112">Ottiene le informazioni archiviate in un punto di analisi esistente.</span><span class="sxs-lookup"><span data-stu-id="18ccb-112">Obtains the information stored in an existing reparse point.</span></span><br/>                         |
| [<span data-ttu-id="18ccb-113">**FSCTL \_ Elimina \_ punto di analisi \_**</span><span class="sxs-lookup"><span data-stu-id="18ccb-113">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | <span data-ttu-id="18ccb-114">Rimuove un punto di analisi esistente.</span><span class="sxs-lookup"><span data-stu-id="18ccb-114">Removes an existing reparse point.</span></span><br/>                                                   |



 

<span data-ttu-id="18ccb-115">Se si sta modificando, recuperando o eliminando un punto di analisi, è necessario specificare lo stesso tag di reparse nell'operazione contenuta nel file.</span><span class="sxs-lookup"><span data-stu-id="18ccb-115">If you are modifying, getting, or deleting a reparse point, you must specify the same reparse tag in the operation that is contained in the file.</span></span> <span data-ttu-id="18ccb-116">In caso contrario, l'operazione avrà esito negativo e si verificherà un **errore di \_ reparse \_ tag non \_ corrispondente**.</span><span class="sxs-lookup"><span data-stu-id="18ccb-116">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_TAG\_MISMATCH**.</span></span> <span data-ttu-id="18ccb-117">Se si sta modificando o eliminando un punto di analisi, è necessario specificare anche il **GUID** di reparse nell'operazione contenuta nel file.</span><span class="sxs-lookup"><span data-stu-id="18ccb-117">If you are modifying or deleting a reparse point, you must also specify the reparse **GUID** in the operation that is contained in the file.</span></span> <span data-ttu-id="18ccb-118">In caso contrario, l'operazione avrà esito negativo e si verificherà un conflitto di errore di **\_ reparse \_ Attribute \_**.</span><span class="sxs-lookup"><span data-stu-id="18ccb-118">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**.</span></span>

<span data-ttu-id="18ccb-119">Per determinare se un file o una directory contiene un reparse point, utilizzare la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="18ccb-119">To determine whether a file or directory contains a reparse point, use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function.</span></span> <span data-ttu-id="18ccb-120">Se al file o alla directory è associato un reparse point, viene impostato l'attributo **\_ \_ reparse \_ Point dell'attributo file** .</span><span class="sxs-lookup"><span data-stu-id="18ccb-120">If the file or directory has an associated reparse point, the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute is set.</span></span>

<span data-ttu-id="18ccb-121">Per sovrascrivere un reparse point esistente senza avere già un handle per il file o la directory, chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il **flag di file \_ \_ aperto \_ reparse \_ Point**.</span><span class="sxs-lookup"><span data-stu-id="18ccb-121">To overwrite an existing reparse point without already having a handle to the file or directory, call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) with **FILE\_FLAG\_OPEN\_REPARSE\_POINT**.</span></span> <span data-ttu-id="18ccb-122">Questo flag consente di aprire il file indipendentemente dal fatto che il filtro file system corrispondente sia installato e funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="18ccb-122">This flag allows you to open the file whether or not the corresponding file system filter is installed and working correctly.</span></span>

 

