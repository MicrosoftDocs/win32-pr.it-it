---
description: È possibile specificare un descrittore di sicurezza per una pipe anonima quando si chiama la funzione non. Il descrittore di sicurezza controlla l'accesso alle estremità di lettura e scrittura della pipe.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Diritti di accesso e sicurezza per le pipe anonime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318075"
---
# <a name="anonymous-pipe-security-and-access-rights"></a><span data-ttu-id="0f10a-104">Diritti di accesso e sicurezza per le pipe anonime</span><span class="sxs-lookup"><span data-stu-id="0f10a-104">Anonymous Pipe Security and Access Rights</span></span>

<span data-ttu-id="0f10a-105">La sicurezza di Windows consente di controllare l'accesso alle pipe anonime.</span><span class="sxs-lookup"><span data-stu-id="0f10a-105">Windows security enables you to control access to anonymous pipes.</span></span> <span data-ttu-id="0f10a-106">Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="0f10a-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="0f10a-107">È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per una pipe quando si chiama la funzione [**non**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) .</span><span class="sxs-lookup"><span data-stu-id="0f10a-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a pipe when you call the [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function.</span></span> <span data-ttu-id="0f10a-108">Il descrittore di sicurezza controlla l'accesso alle estremità di lettura e scrittura della pipe.</span><span class="sxs-lookup"><span data-stu-id="0f10a-108">The security descriptor controls access to both the read and write ends of the pipe.</span></span> <span data-ttu-id="0f10a-109">Se si specifica **null**, la pipe ottiene un descrittore di sicurezza predefinito.</span><span class="sxs-lookup"><span data-stu-id="0f10a-109">If you specify **NULL**, the pipe gets a default security descriptor.</span></span> <span data-ttu-id="0f10a-110">Gli ACL nel descrittore di sicurezza predefinito per una pipe provengono dal token primario o di rappresentazione del creatore.</span><span class="sxs-lookup"><span data-stu-id="0f10a-110">The ACLs in the default security descriptor for a pipe come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="0f10a-111">Per recuperare il descrittore di sicurezza di una pipe, chiamare la funzione [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="0f10a-111">To retrieve a pipe's security descriptor, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span> <span data-ttu-id="0f10a-112">Per modificare il descrittore di sicurezza di una pipe, chiamare la funzione [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="0f10a-112">To change a pipe's security descriptor, call the [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) function.</span></span>

<span data-ttu-id="0f10a-113">La funzione [**non**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) restituisce due handle alla pipe anonima: un handle di lettura con \_ accesso generico Read e Synchronize e un handle di scrittura con \_ accesso generico di scrittura e sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0f10a-113">The [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function returns two handles to the anonymous pipe: a read handle with GENERIC\_READ and SYNCHRONIZE access; and a write handle with GENERIC\_WRITE and SYNCHRONIZE access.</span></span> <span data-ttu-id="0f10a-114">\_ \_ L'accesso di lettura e scrittura generico usa lo stesso mapping dei diritti di accesso per le named pipe.</span><span class="sxs-lookup"><span data-stu-id="0f10a-114">GENERIC\_READ and GENERIC\_WRITE access use the same access rights mapping as for named pipes.</span></span>

<span data-ttu-id="0f10a-115">L' \_ accesso in lettura generico per una pipe anonima combina i diritti per la lettura dei dati dalla pipe, la lettura degli attributi della pipe, la lettura degli attributi estesi e la lettura dell'elenco DACL della pipe.</span><span class="sxs-lookup"><span data-stu-id="0f10a-115">GENERIC\_READ access for an anonymous pipe combines the rights to read data from the pipe, read pipe attributes, read extended attributes, and read the pipe's DACL.</span></span>

<span data-ttu-id="0f10a-116">L' \_ accesso in scrittura generico per una pipe anonima combina i diritti per la scrittura dei dati nella pipe, l'aggiunta di dati, la scrittura di attributi pipe, la scrittura di attributi estesi e la lettura dell'elenco DACL della pipe.</span><span class="sxs-lookup"><span data-stu-id="0f10a-116">GENERIC\_WRITE access for an anonymous pipe combines the rights to write data to the pipe, append data to it, write pipe attributes, write extended attributes, and read the pipe's DACL.</span></span>

 

 
