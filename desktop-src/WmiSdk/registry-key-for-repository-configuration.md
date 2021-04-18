---
description: Strumentazione gestione Windows (WMI) dispone di una nuova chiave del registro di sistema per abilitare o disabilitare la funzionalità di repository di autoripristino.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Chiave del registro di sistema per la configurazione del repository
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309911"
---
# <a name="registry-key-for-repository-configuration"></a><span data-ttu-id="592e6-103">Chiave del registro di sistema per la configurazione del repository</span><span class="sxs-lookup"><span data-stu-id="592e6-103">Registry Key for Repository Configuration</span></span>

<span data-ttu-id="592e6-104">Strumentazione gestione Windows (WMI) include una nuova chiave del registro di sistema per abilitare o disabilitare la funzionalità di repository di ripristino.</span><span class="sxs-lookup"><span data-stu-id="592e6-104">Windows Management Instrumentation (WMI) has a new registry key to enable or disable the AutoRestore repository feature..</span></span> <span data-ttu-id="592e6-105">Per ulteriori informazioni sul ripristino del repository WMI, vedere [backup o ripristino del repository WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="592e6-105">For more information on restoring the WMI repository, see [Backup or Restore WMI Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span></span>

<span data-ttu-id="592e6-106">In Windows 7 il comportamento predefinito prevede il ripristino automatico di un repository da una versione di cui è stato eseguito il backup se viene rilevato un danneggiamento del repository.</span><span class="sxs-lookup"><span data-stu-id="592e6-106">In Windows 7, the default behavior is to auto-restore a repository from a backed-up version if a repository corruption is detected.</span></span> <span data-ttu-id="592e6-107">WMI fornisce il valore del registro di sistema **AutoRestoreEnabled** per disabilitare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="592e6-107">WMI provides the **AutoRestoreEnabled** registry value to disable this feature.</span></span>

<span data-ttu-id="592e6-108">Le chiavi del registro di sistema per WMI si trovano nel registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="592e6-108">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<dl> <dt>

<span data-ttu-id="592e6-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span><span class="sxs-lookup"><span data-stu-id="592e6-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="592e6-110">Consente all'utente di determinare se usare o meno la funzionalità di repository di autoripristino.</span><span class="sxs-lookup"><span data-stu-id="592e6-110">Enables the user to determine whether or not to use the AutoRestore repository feature.</span></span> <span data-ttu-id="592e6-111">Per impostazione predefinita, questa chiave è impostata su 1 e la funzionalità del repository autorestore è abilitata.</span><span class="sxs-lookup"><span data-stu-id="592e6-111">By default this key is set to 1 and the AutoRestore Repository feature is enabled.</span></span>

<span data-ttu-id="592e6-112">Sono possibili le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="592e6-112">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="592e6-113"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="592e6-113"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="592e6-114">Disabled</span><span class="sxs-lookup"><span data-stu-id="592e6-114">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="592e6-115"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="592e6-115"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="592e6-116">Abilitato</span><span class="sxs-lookup"><span data-stu-id="592e6-116">Enabled</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="592e6-117">Il valore del registro di sistema **AutoRestoreEnabled** può essere modificato tramite il console Gestione criteri di gruppo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="592e6-117">The **AutoRestoreEnabled** registry value can be modified by using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="592e6-118">Per ulteriori informazioni, vedere [console Gestione criteri di gruppo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="592e6-118">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="592e6-119">Questa procedura fornisce informazioni dettagliate su come abilitare o disabilitare la funzionalità di repository di autoripristino:</span><span class="sxs-lookup"><span data-stu-id="592e6-119">This procedure provides details about how to enable or disable the AutoRestore repository feature:</span></span>

<span data-ttu-id="592e6-120">**Per modificare il valore predefinito della chiave **AutoRestoreEnabled** usando criteri di gruppo**</span><span class="sxs-lookup"><span data-stu-id="592e6-120">**To change the default value of the **AutoRestoreEnabled** key by using Group Policy**</span></span>

1.  <span data-ttu-id="592e6-121">Aprire Console Gestione Criteri di gruppo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="592e6-121">Open the GPMC.</span></span>
2.  <span data-ttu-id="592e6-122">Creare un oggetto Criteri di gruppo (GPO).</span><span class="sxs-lookup"><span data-stu-id="592e6-122">Create a Group Policy object (GPO).</span></span>
3.  <span data-ttu-id="592e6-123">Modificare l'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="592e6-123">Edit the GPO.</span></span>
4.  <span data-ttu-id="592e6-124">Passare a Preferenze/impostazioni di Windows/Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="592e6-124">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="592e6-125">Fare clic con il pulsante destro del mouse e scegliere **nuovo... Registro di sistema**.</span><span class="sxs-lookup"><span data-stu-id="592e6-125">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="592e6-126">Questa azione presenta un'interfaccia utente in cui è possibile immettere le informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="592e6-126">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="592e6-127">Selezionare il comando **Aggiorna** .</span><span class="sxs-lookup"><span data-stu-id="592e6-127">Select the **Update** command.</span></span>
7.  <span data-ttu-id="592e6-128">Selezionare il percorso della chiave del registro di sistema seguente: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="592e6-128">Select the following registry key path: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM**.</span></span>
8.  <span data-ttu-id="592e6-129">Nel campo **nome** immettere **AutoRestoreEnabled**.</span><span class="sxs-lookup"><span data-stu-id="592e6-129">In the **name** field, enter **AutoRestoreEnabled**.</span></span>
9.  <span data-ttu-id="592e6-130">Nel campo **dati** immettere 0 per disabilitare o 1 per abilitare la funzionalità di repository di ripristino di autoripristino.</span><span class="sxs-lookup"><span data-stu-id="592e6-130">In the **data** field, enter 0 to disable or 1 to enable the AutoRestore repository feature.</span></span>
10. <span data-ttu-id="592e6-131">Fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="592e6-131">Click OK.</span></span>

 

 
