---
title: Funzioni file system distribuito
description: Di seguito sono riportate le funzioni file system distribuito (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483765"
---
# <a name="distributed-file-system-functions"></a><span data-ttu-id="ba717-103">Funzioni file system distribuito</span><span class="sxs-lookup"><span data-stu-id="ba717-103">Distributed File System Functions</span></span>

<span data-ttu-id="ba717-104">Di seguito sono riportate le funzioni file system distribuito (DFS).</span><span class="sxs-lookup"><span data-stu-id="ba717-104">The following are the Distributed File System (DFS) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ba717-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ba717-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ba717-106">NetDfsAdd</span><span class="sxs-lookup"><span data-stu-id="ba717-106">NetDfsAdd</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
<span data-ttu-id="ba717-107">Crea un nuovo collegamento file system distribuito (DFS) o aggiunge destinazioni a un collegamento esistente in uno spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-107">Creates a new Distributed File System (DFS) link or adds targets to an existing link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-108">NetDfsAddFtRoot</span><span class="sxs-lookup"><span data-stu-id="ba717-108">NetDfsAddFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
<span data-ttu-id="ba717-109">Crea un nuovo spazio dei nomi di file system distribuito basato su dominio (DFS).</span><span class="sxs-lookup"><span data-stu-id="ba717-109">Creates a new domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="ba717-110">Se lo spazio dei nomi esiste già, la funzione aggiunge la destinazione radice specificata.</span><span class="sxs-lookup"><span data-stu-id="ba717-110">If the namespace already exists, the function adds the specified root target to it.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-111">NetDfsAddRootTarget</span><span class="sxs-lookup"><span data-stu-id="ba717-111">NetDfsAddRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
<span data-ttu-id="ba717-112">Consente di creare uno spazio dei nomi DFS basato su dominio o autonomo o di aggiungere una nuova destinazione radice a uno spazio dei nomi basato su dominio esistente.</span><span class="sxs-lookup"><span data-stu-id="ba717-112">Creates a domain-based or stand-alone DFS namespace or adds a new root target to an existing domain-based namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-113">NetDfsAddStdRoot</span><span class="sxs-lookup"><span data-stu-id="ba717-113">NetDfsAddStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
<span data-ttu-id="ba717-114">Crea un nuovo spazio dei nomi di file system distribuito autonomo (DFS).</span><span class="sxs-lookup"><span data-stu-id="ba717-114">Creates a new stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-115">NetDfsEnum</span><span class="sxs-lookup"><span data-stu-id="ba717-115">NetDfsEnum</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
<span data-ttu-id="ba717-116">Enumera gli spazi dei nomi file system distribuito (DFS) ospitati in un server o in un collegamento DFS di uno spazio dei nomi ospitato da un server.</span><span class="sxs-lookup"><span data-stu-id="ba717-116">Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-117">NetDfsGetClientInfo</span><span class="sxs-lookup"><span data-stu-id="ba717-117">NetDfsGetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
<span data-ttu-id="ba717-118">Recupera le informazioni su una radice file system distribuito (DFS) o un collegamento dalla cache gestita dal client DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-118">Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-119">NetDfsGetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="ba717-119">NetDfsGetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="ba717-120">Recupera il descrittore di sicurezza dell'oggetto contenitore per gli spazi dei nomi DFS basati su dominio nel dominio di Active Directory specificato.</span><span class="sxs-lookup"><span data-stu-id="ba717-120">Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-121">NetDfsGetInfo</span><span class="sxs-lookup"><span data-stu-id="ba717-121">NetDfsGetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
<span data-ttu-id="ba717-122">Recupera le informazioni relative a una radice file system distribuito (DFS) specificata o a un collegamento in uno spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-122">Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-123">NetDfsGetSecurity</span><span class="sxs-lookup"><span data-stu-id="ba717-123">NetDfsGetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
<span data-ttu-id="ba717-124">Recupera il descrittore di sicurezza per l'oggetto radice dello spazio dei nomi DFS specificato.</span><span class="sxs-lookup"><span data-stu-id="ba717-124">Retrieves the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-125">NetDfsGetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="ba717-125">NetDfsGetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="ba717-126">Recupera il descrittore di sicurezza per l'oggetto contenitore dello spazio dei nomi DFS autonomo specificato.</span><span class="sxs-lookup"><span data-stu-id="ba717-126">Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-127">NetDfsGetSupportedNamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="ba717-127">NetDfsGetSupportedNamespaceVersion</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
<span data-ttu-id="ba717-128">Determina il numero di versione dei metadati supportata.</span><span class="sxs-lookup"><span data-stu-id="ba717-128">Determines the supported metadata version number.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-129">NetDfsMove</span><span class="sxs-lookup"><span data-stu-id="ba717-129">NetDfsMove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
<span data-ttu-id="ba717-130">Rinomina o sposta un collegamento DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-130">Renames or moves a DFS link.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-131">NetDfsRemove</span><span class="sxs-lookup"><span data-stu-id="ba717-131">NetDfsRemove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
<span data-ttu-id="ba717-132">Rimuove un collegamento di file system distribuito (DFS) o una destinazione di collegamento specifica di un collegamento DFS in uno spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-132">Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS namespace.</span></span> <span data-ttu-id="ba717-133">Quando si rimuove una destinazione di collegamento specifica, il collegamento viene rimosso se viene rimossa l'ultima destinazione del collegamento del collegamento.</span><span class="sxs-lookup"><span data-stu-id="ba717-133">When removing a specific link target, the link itself is removed if the last link target of the link is removed.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-134">NetDfsRemoveFtRoot</span><span class="sxs-lookup"><span data-stu-id="ba717-134">NetDfsRemoveFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
<span data-ttu-id="ba717-135">Rimuove la destinazione radice specificata da uno spazio dei nomi di file system distribuito basato su dominio (DFS).</span><span class="sxs-lookup"><span data-stu-id="ba717-135">Removes the specified root target from a domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="ba717-136">Se è in corso la rimozione dell'ultima destinazione radice dello spazio dei nomi DFS, la funzione eliminerà anche lo spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-136">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="ba717-137">È possibile eliminare uno spazio dei nomi DFS senza prima eliminare tutti i relativi collegamenti.</span><span class="sxs-lookup"><span data-stu-id="ba717-137">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-138">NetDfsRemoveFtRootForced</span><span class="sxs-lookup"><span data-stu-id="ba717-138">NetDfsRemoveFtRootForced</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
<span data-ttu-id="ba717-139">Rimuove la destinazione radice specificata da uno spazio dei nomi file system distribuito (DFS) basato su dominio, anche se il server di destinazione radice è offline.</span><span class="sxs-lookup"><span data-stu-id="ba717-139">Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.</span></span> <span data-ttu-id="ba717-140">Se è in corso la rimozione dell'ultima destinazione radice dello spazio dei nomi DFS, la funzione eliminerà anche lo spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-140">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="ba717-141">È possibile eliminare uno spazio dei nomi DFS senza prima eliminare tutti i relativi collegamenti.</span><span class="sxs-lookup"><span data-stu-id="ba717-141">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

> [!Note]
> <span data-ttu-id="ba717-142">La funzione [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) non aggiorna il registro di sistema nel server di destinazione radice DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-142">The [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) function does not update the registry on the DFS root target server.</span></span> <span data-ttu-id="ba717-143">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ba717-143">For more information, see the Remarks section.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-144">NetDfsRemoveRootTarget</span><span class="sxs-lookup"><span data-stu-id="ba717-144">NetDfsRemoveRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
<span data-ttu-id="ba717-145">Rimuove una destinazione radice DFS da uno spazio dei nomi DFS basato su dominio.</span><span class="sxs-lookup"><span data-stu-id="ba717-145">Removes a DFS root target from a domain-based DFS namespace.</span></span> <span data-ttu-id="ba717-146">Se la destinazione radice è l'ultima destinazione radice nello spazio dei nomi DFS, questa funzione rimuove lo spazio dei nomi DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-146">If the root target is the last root target in the DFS namespace, this function removes the DFS namespace.</span></span> <span data-ttu-id="ba717-147">Questa funzione può essere utilizzata anche per rimuovere uno spazio dei nomi DFS autonomo.</span><span class="sxs-lookup"><span data-stu-id="ba717-147">This function can also be used to remove a stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-148">NetDfsRemoveStdRoot</span><span class="sxs-lookup"><span data-stu-id="ba717-148">NetDfsRemoveStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
<span data-ttu-id="ba717-149">Elimina uno spazio dei nomi di file system distribuito autonomo (DFS).</span><span class="sxs-lookup"><span data-stu-id="ba717-149">Deletes a stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-150">NetDfsSetClientInfo</span><span class="sxs-lookup"><span data-stu-id="ba717-150">NetDfsSetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
<span data-ttu-id="ba717-151">Modifica le informazioni relative a una radice file system distribuito (DFS) o a un collegamento nella cache gestita dal client DFS.</span><span class="sxs-lookup"><span data-stu-id="ba717-151">Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-152">NetDfsSetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="ba717-152">NetDfsSetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="ba717-153">Imposta il descrittore di sicurezza dell'oggetto contenitore per gli spazi dei nomi DFS basati su dominio nel dominio di Active Directory specificato.</span><span class="sxs-lookup"><span data-stu-id="ba717-153">Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-154">NetDfsSetInfo</span><span class="sxs-lookup"><span data-stu-id="ba717-154">NetDfsSetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
<span data-ttu-id="ba717-155">Imposta o modifica le informazioni relative a una radice file system distribuito (DFS), una destinazione radice, un collegamento o una destinazione di collegamento specifici.</span><span class="sxs-lookup"><span data-stu-id="ba717-155">Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-156">NetDfsSetSecurity</span><span class="sxs-lookup"><span data-stu-id="ba717-156">NetDfsSetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
<span data-ttu-id="ba717-157">Imposta il descrittore di sicurezza per l'oggetto radice dello spazio dei nomi DFS specificato.</span><span class="sxs-lookup"><span data-stu-id="ba717-157">Sets the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="ba717-158">NetDfsSetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="ba717-158">NetDfsSetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="ba717-159">Imposta il descrittore di sicurezza per l'oggetto contenitore dello spazio dei nomi DFS autonomo specificato.</span><span class="sxs-lookup"><span data-stu-id="ba717-159">Sets the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> </dl>

<span data-ttu-id="ba717-160">Si noti che un'applicazione che richiama una delle funzioni può causare indirettamente al server dello spazio dei nomi DFS locale di gestire la chiamata di funzione per eseguire una sincronizzazione completa dei metadati dello spazio dei nomi correlati dal master emulatore PDC per quel dominio.</span><span class="sxs-lookup"><span data-stu-id="ba717-160">Note that an application invoking any of the functions may indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of the related namespace metadata from the PDC emulator master for that domain.</span></span> <span data-ttu-id="ba717-161">Questa sincronizzazione completa potrebbe verificarsi anche quando è configurata la modalità di scalabilità radice per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ba717-161">This full synchronization could happen even when root scalability mode is configured for that namespace.</span></span>
