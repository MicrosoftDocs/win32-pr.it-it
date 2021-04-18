---
description: In alcuni casi potrebbe essere necessario installare una versione più recente di un provider in un sistema in esecuzione.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Aggiornamento di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315191"
---
# <a name="updating-a-provider"></a><span data-ttu-id="03b9a-103">Aggiornamento di un provider</span><span class="sxs-lookup"><span data-stu-id="03b9a-103">Updating a Provider</span></span>

<span data-ttu-id="03b9a-104">In alcuni casi potrebbe essere necessario installare una versione più recente di un provider in un sistema in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="03b9a-104">Sometimes you may need to install a newer version of a provider onto a running system.</span></span> <span data-ttu-id="03b9a-105">Se il provider è installato come DLL, è possibile installare un nuovo provider senza dover riavviare il servizio, riavviare il computer o influire in altro modo sulle applicazioni che utilizzano WMI in quel momento.</span><span class="sxs-lookup"><span data-stu-id="03b9a-105">If your provider is installed as a DLL, you can install a new provider without having to restart the service, reboot the computer, or otherwise affect any applications using WMI at that time.</span></span>

<span data-ttu-id="03b9a-106">Nella procedura riportata di seguito viene descritto come aggiornare un provider.</span><span class="sxs-lookup"><span data-stu-id="03b9a-106">The following procedure describes how to update a provider.</span></span>

<span data-ttu-id="03b9a-107">**Per aggiornare un provider**</span><span class="sxs-lookup"><span data-stu-id="03b9a-107">**To update a provider**</span></span>

1.  <span data-ttu-id="03b9a-108">Compilare il nuovo provider.</span><span class="sxs-lookup"><span data-stu-id="03b9a-108">Build the new provider.</span></span>

    1.  <span data-ttu-id="03b9a-109">Compilare il nuovo provider con un nome di DLL diverso e un **CLSID** diverso.</span><span class="sxs-lookup"><span data-stu-id="03b9a-109">Compile the new provider with a different DLL name and a different **CLSID**.</span></span>

        <span data-ttu-id="03b9a-110">Modificare, ad esempio, Myprov.dll in Myprov1.dll e **CLSID \_ MyProProv** in **CLSID \_ diprov** 1.</span><span class="sxs-lookup"><span data-stu-id="03b9a-110">For example, change Myprov.dll to Myprov1.dll, and **CLSID\_MyProProv** to **CLSID\_MyProv** 1.</span></span>

    2.  <span data-ttu-id="03b9a-111">Modificare il file MOF di registrazione del provider in modo da utilizzare il nuovo CLSID (CLSID \_ MyProv1), ma lo stesso nome del provider ("prov").</span><span class="sxs-lookup"><span data-stu-id="03b9a-111">Modify the provider registration MOF file to use the new CLSID (CLSID\_MyProv1), but the same provider name ("MyProv").</span></span>

2.  <span data-ttu-id="03b9a-112">Installare il nuovo provider.</span><span class="sxs-lookup"><span data-stu-id="03b9a-112">Install the new provider.</span></span>

    1.  <span data-ttu-id="03b9a-113">Copiare la nuova DLL del provider con il nuovo nome insieme a quello precedente.</span><span class="sxs-lookup"><span data-stu-id="03b9a-113">Copy the new provider DLL with the new name alongside the old one.</span></span>
    2.  <span data-ttu-id="03b9a-114">Registrare autonomamente il nuovo provider.</span><span class="sxs-lookup"><span data-stu-id="03b9a-114">Self-register the new provider.</span></span>

        <span data-ttu-id="03b9a-115">Ad esempio, usare il comando **regsvr32** **myprov1.dll** per registrare il nuovo provider.</span><span class="sxs-lookup"><span data-stu-id="03b9a-115">For example, use the **regsvr32** **myprov1.dll** command to register the new provider.</span></span>

    3.  <span data-ttu-id="03b9a-116">Compilare il nuovo MOF di registrazione del provider, sovrascrivendo quindi la registrazione del provider precedente.</span><span class="sxs-lookup"><span data-stu-id="03b9a-116">Compile the new provider registration MOF, thus overwriting the old provider registration.</span></span> <span data-ttu-id="03b9a-117">Fino a questo punto, il vecchio provider era completamente funzionante; il nuovo provider è ora completamente operativo.</span><span class="sxs-lookup"><span data-stu-id="03b9a-117">Until this point, the old provider was fully functional; now the new provider is fully operational.</span></span>

3.  <span data-ttu-id="03b9a-118">Rimuovere la versione precedente del provider, se necessario.</span><span class="sxs-lookup"><span data-stu-id="03b9a-118">Remove the old version of the provider, if necessary.</span></span>

    1.  <span data-ttu-id="03b9a-119">Annulla la registrazione della DLL precedente.</span><span class="sxs-lookup"><span data-stu-id="03b9a-119">Unregister the old DLL.</span></span>

        <span data-ttu-id="03b9a-120">Usare, ad esempio, il comando **regsvr32** **/umyprov.dll** per annullare la registrazione della dll precedente.</span><span class="sxs-lookup"><span data-stu-id="03b9a-120">For example, use the **regsvr32** **/umyprov.dll** command to unregister the old DLL.</span></span>

    2.  <span data-ttu-id="03b9a-121">Contrassegnare la vecchia DLL da eliminare al riavvio chiamando [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span><span class="sxs-lookup"><span data-stu-id="03b9a-121">Mark the old DLL to be deleted on reboot by calling [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span></span>

<span data-ttu-id="03b9a-122">Per aggiornare un provider implementato da server locale, è possibile eseguire una procedura simile.</span><span class="sxs-lookup"><span data-stu-id="03b9a-122">You can take similar steps to upgrade a local server-implemented provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03b9a-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03b9a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03b9a-124">Sviluppo di un provider WMI</span><span class="sxs-lookup"><span data-stu-id="03b9a-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="03b9a-125">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03b9a-125">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="03b9a-126">Sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="03b9a-126">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
