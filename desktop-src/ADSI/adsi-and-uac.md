---
title: ADSI e controllo dell'account utente
description: Windows e Windows Server hanno il controllo dell'account utente, che include le ramificazioni per le applicazioni che utilizzano ADSI (Active Directory Service Interfaces).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047356"
---
# <a name="adsi-and-user-account-control"></a><span data-ttu-id="e272e-103">ADSI e controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="e272e-103">ADSI and User Account Control</span></span>

<span data-ttu-id="e272e-104">Windows e Windows Server hanno il [controllo dell'account utente](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), che include le ramificazioni per le applicazioni che utilizzano ADSI ( [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) ).</span><span class="sxs-lookup"><span data-stu-id="e272e-104">Windows and Windows Server have [User Account Control](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), which has ramifications for applications that use [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="e272e-105">In particolare, queste interfacce sono state progettate per essere eseguite da un account utente con privilegi di amministratore nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e272e-105">Specifically, these interfaces were designed to be run by a user account with administrator privileges on the local computer.</span></span>

<span data-ttu-id="e272e-106">**Problema**</span><span class="sxs-lookup"><span data-stu-id="e272e-106">**Problem**</span></span>

<span data-ttu-id="e272e-107">Ogni volta che un'applicazione si connette alla directory e tenta di creare un oggetto ADSI, viene verificata la presenza di modifiche nello [Schema Active Directory](/windows/desktop/ADSchema/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="e272e-107">Every time an application connects to the directory and attempts to create an ADSI object, the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) is checked for changes.</span></span> <span data-ttu-id="e272e-108">Se è stato modificato dopo l'ultima connessione, lo schema viene scaricato e archiviato in una cache nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e272e-108">If it has changed since the last connection, the schema is downloaded and stored in a cache on the local computer.</span></span> <span data-ttu-id="e272e-109">Nelle versioni di Windows precedenti a Windows Vista, il percorso predefinito per questa cache era</span><span class="sxs-lookup"><span data-stu-id="e272e-109">In versions of Windows prior to Windows Vista, the default location for this cache was</span></span>

`%systemroot%\SchCache\`

<span data-ttu-id="e272e-110">Tuttavia, le applicazioni eseguite da account standard, ovvero non amministratori, non avranno accesso a questa directory e, di conseguenza, le applicazioni che utilizzano le interfacce ADSI eseguite in questa modalità scaricheranno lo schema in ogni connessione, che influirà sulla velocità effettiva e sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e272e-110">However, applications run by standard (that is, non-administrator) accounts will not have access to this directory, and consequently, applications that use ADSI interfaces that are run in this mode will download the schema on every connection, which will impact throughput and performance.</span></span>

<span data-ttu-id="e272e-111">**Soluzioni**</span><span class="sxs-lookup"><span data-stu-id="e272e-111">**Solutions**</span></span>

<span data-ttu-id="e272e-112">*Utente singolo* : per risolvere questo problema, sono disponibili nuove chiavi di controllo del registro di sistema del provider ADSI che determinano i percorsi del registro di sistema e i percorsi dei file per gli oggetti [dello schema di Active Directory](/windows/desktop/ADSchema/active-directory-schema) memorizzati</span><span class="sxs-lookup"><span data-stu-id="e272e-112">*Single user* - To resolve this issue, there are new ADSI Provider registry control keys that determine the registry locations and file locations for cached [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects.</span></span> <span data-ttu-id="e272e-113">Se la chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e272e-113">If the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="e272e-114">è impostato su 0 (zero), ogni utente avrà un percorso di archiviazione diverso per ADSI. le chiavi del registro di sistema verranno archiviate in</span><span class="sxs-lookup"><span data-stu-id="e272e-114">is set to 0 (zero), each user will have a different storage location for ADSI; registry keys will be stored in</span></span>

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

<span data-ttu-id="e272e-115">e i file di cache verranno archiviati in</span><span class="sxs-lookup"><span data-stu-id="e272e-115">and cache files will be stored in</span></span>

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

<span data-ttu-id="e272e-116">Queste impostazioni sono le impostazioni predefinite dei computer che eseguono Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e272e-116">These settings are the default settings on computers running Windows Server 2008 or Windows Vista.</span></span>

<span data-ttu-id="e272e-117">*Multiutente* : se si eseguono applicazioni ADSI in un computer con molti account utente (ad esempio, un server Web), è preferibile non avere molte copie della [Active Directory cache dello schema](/windows/desktop/ADSchema/active-directory-schema) usando grandi quantità di spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="e272e-117">*Multi-user* - If you are running ADSI applications on a computer with many user accounts (for example, a web server), then it's preferable not to have many copies of the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) cache using up large amounts of disk space.</span></span> <span data-ttu-id="e272e-118">Impostazione della chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e272e-118">Setting the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="e272e-119">a 1 (uno) verrà ripristinato il comportamento precedente di ADSI. tutti gli oggetti [dello Schema Active Directory](/windows/desktop/ADSchema/active-directory-schema) verranno archiviati nei percorsi precedenti. la chiave del registro di sistema sarà in</span><span class="sxs-lookup"><span data-stu-id="e272e-119">to 1 (one) will revert ADSI to the previous behavior; all [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects will be stored in their previous locations; the registry key will be in</span></span>

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

<span data-ttu-id="e272e-120">e il file di cache sarà in</span><span class="sxs-lookup"><span data-stu-id="e272e-120">and the cache file will be in</span></span>

`%systemroot%\SchCache`

<span data-ttu-id="e272e-121">In questo caso, gli account amministratore devono eseguire l'applicazione, il che comporterà la memorizzazione nella cache del file di schema nel percorso globale per un uso futuro da parte degli utenti con privilegi minori.</span><span class="sxs-lookup"><span data-stu-id="e272e-121">In this case, administrator accounts should run the application, which will cause the schema file to be cached in the global location for future use by the less privileged users.</span></span>

 

 