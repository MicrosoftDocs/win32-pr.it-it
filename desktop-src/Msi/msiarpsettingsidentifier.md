---
description: La proprietà MSIARPSETTINGSIDENTIFIER contiene un elenco delimitato da punti e virgola dei percorsi del registro di sistema in cui l'applicazione archivia le impostazioni e le preferenze di un utente.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Proprietà MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331311"
---
# <a name="msiarpsettingsidentifier-property"></a><span data-ttu-id="5ef44-103">Proprietà MSIARPSETTINGSIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="5ef44-103">MSIARPSETTINGSIDENTIFIER property</span></span>

<span data-ttu-id="5ef44-104">La proprietà **MSIARPSETTINGSIDENTIFIER** contiene un elenco delimitato da punti e virgola dei percorsi del registro di sistema in cui l'applicazione archivia le impostazioni e le preferenze di un utente.</span><span class="sxs-lookup"><span data-stu-id="5ef44-104">The **MSIARPSETTINGSIDENTIFIER** property contains a semi-colon delimited list of the registry locations where the application stores a user's settings and preferences.</span></span> <span data-ttu-id="5ef44-105">Durante un aggiornamento del sistema operativo, il programma di installazione può utilizzare queste informazioni per migliorare l'esperienza degli utenti che eseguono la migrazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5ef44-105">During an operating system upgrade, setup can use this information to improve the experience of users who are migrating applications.</span></span>

<span data-ttu-id="5ef44-106">Il valore della proprietà **MSIARPSETTINGSIDENTIFIER** è un testo letterale che contiene l'elenco dei percorsi del registro di sistema in cui vengono archiviate le impostazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ef44-106">The value of the **MSIARPSETTINGSIDENTIFIER** property is literal text that contains the list of registry locations where the application stores its settings.</span></span> <span data-ttu-id="5ef44-107">Il valore può specificare più percorsi del registro di sistema possibili.</span><span class="sxs-lookup"><span data-stu-id="5ef44-107">The value can specify multiple possible registry locations.</span></span> <span data-ttu-id="5ef44-108">Separare più percorsi del registro di sistema usando un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="5ef44-108">Separate multiple registry locations by using semi-colons.</span></span> <span data-ttu-id="5ef44-109">Le impostazioni dell'applicazione vengono in genere archiviate negli hive del registro di sistema **HKCU** o **HKLM** nel formato: *\\ \\ versione dell'applicazione aziendale*.</span><span class="sxs-lookup"><span data-stu-id="5ef44-109">Application settings are typically stored in the **HKCU** or **HKLM** registry hives in the form: *Company\\Application\\Version*.</span></span> <span data-ttu-id="5ef44-110">L'esempio seguente è un possibile valore per la proprietà **MSIARPSETTINGSIDENTIFIER** .</span><span class="sxs-lookup"><span data-stu-id="5ef44-110">The following example is a possible value for the **MSIARPSETTINGSIDENTIFIER** property.</span></span>

<span data-ttu-id="5ef44-111">*MyCompany \\ AppSuite \\ 1,0; MyCompany \\ App1 \\ 1,0; MyCompany \\ App2 \\ 1,0*</span><span class="sxs-lookup"><span data-stu-id="5ef44-111">*MyCompany\\AppSuite\\1.0;MyCompany\\App1\\1.0;MyCompany\\App2\\1.0*</span></span>

<span data-ttu-id="5ef44-112">Questa proprietà è facoltativa e può essere impostata nella tabella delle [Proprietà](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5ef44-112">This property is optional and can be set in the [Property](property-table.md) table.</span></span> <span data-ttu-id="5ef44-113">Se questa proprietà viene visualizzata nella tabella delle proprietà, il valore non deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="5ef44-113">If this property appears in the Property table, the value must not be set to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef44-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ef44-114">Requirements</span></span>



| <span data-ttu-id="5ef44-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ef44-115">Requirement</span></span> | <span data-ttu-id="5ef44-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5ef44-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef44-117">Versione</span><span class="sxs-lookup"><span data-stu-id="5ef44-117">Version</span></span><br/> | <span data-ttu-id="5ef44-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5ef44-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5ef44-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5ef44-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5ef44-120">Windows Installer 4,5 in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5ef44-120">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5ef44-121">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5ef44-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ef44-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ef44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef44-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ef44-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5ef44-124">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="5ef44-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




