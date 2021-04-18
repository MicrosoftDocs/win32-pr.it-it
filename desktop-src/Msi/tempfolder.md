---
description: Il programma di installazione imposta la proprietà TempFolder sul percorso completo della cartella Temp. Gli autori non devono necessariamente impostare la proprietà TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Proprietà TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324917"
---
# <a name="tempfolder-property"></a><span data-ttu-id="def43-103">Proprietà TempFolder</span><span class="sxs-lookup"><span data-stu-id="def43-103">TempFolder property</span></span>

<span data-ttu-id="def43-104">Il programma di installazione imposta la proprietà **TempFolder** sul percorso completo della cartella Temp.</span><span class="sxs-lookup"><span data-stu-id="def43-104">The installer sets the **TempFolder** property to the full path to the Temp folder.</span></span>

<span data-ttu-id="def43-105">Gli autori non devono necessariamente impostare la proprietà **TempFolder** .</span><span class="sxs-lookup"><span data-stu-id="def43-105">Authors should not need to set the **TempFolder** property.</span></span> <span data-ttu-id="def43-106">Windows Installer usa la funzione [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) per recuperare il percorso della directory designata per i file temporanei e per impostare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="def43-106">Windows Installer uses the [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files and to set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="def43-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="def43-107">Remarks</span></span>

<span data-ttu-id="def43-108">Un valore comune per questa proprietà è C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="def43-108">A common value for this property is C:\\Temp.</span></span>

## <a name="requirements"></a><span data-ttu-id="def43-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="def43-109">Requirements</span></span>



| <span data-ttu-id="def43-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="def43-110">Requirement</span></span> | <span data-ttu-id="def43-111">Valore</span><span class="sxs-lookup"><span data-stu-id="def43-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def43-112">Versione</span><span class="sxs-lookup"><span data-stu-id="def43-112">Version</span></span><br/> | <span data-ttu-id="def43-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="def43-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="def43-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="def43-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="def43-115">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="def43-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="def43-116">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="def43-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="def43-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="def43-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def43-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="def43-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 
