---
description: Prima che il motore di configurazione della sicurezza possa chiamare il motore dell'allegato per elaborare le attività specifiche del servizio, è necessario installare il motore di allegati e registrarlo con il motore di configurazione della sicurezza.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrazione di un motore di allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306426"
---
# <a name="registering-an-attachment-engine"></a><span data-ttu-id="bb24a-103">Registrazione di un motore di allegati</span><span class="sxs-lookup"><span data-stu-id="bb24a-103">Registering an Attachment Engine</span></span>

<span data-ttu-id="bb24a-104">Prima che il motore di configurazione della sicurezza possa chiamare il motore dell'allegato per elaborare le attività specifiche del servizio, è necessario installare il motore di allegati e registrarlo con il motore di configurazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bb24a-104">Before the Security Configuration Engine can call your attachment engine to process service-specific tasks, you must install your attachment engine and register it with the Security Configuration Engine.</span></span>

<span data-ttu-id="bb24a-105">**Per installare e registrare la DLL del motore allegati**</span><span class="sxs-lookup"><span data-stu-id="bb24a-105">**To install and register the attachment engine DLL**</span></span>

1.  <span data-ttu-id="bb24a-106">Copiare la DLL del motore degli allegati in una directory del sistema.</span><span class="sxs-lookup"><span data-stu-id="bb24a-106">Copy the attachment engine DLL to a directory on the system.</span></span> <span data-ttu-id="bb24a-107">La directory preferita è% windir% \\ secedit \\ Attachments.</span><span class="sxs-lookup"><span data-stu-id="bb24a-107">The preferred directory is %windir%\\secedit\\attachments.</span></span> <span data-ttu-id="bb24a-108">Se questa directory non esiste, è necessario crearla.</span><span class="sxs-lookup"><span data-stu-id="bb24a-108">If this directory does not exist, you should create it.</span></span>
2.  <span data-ttu-id="bb24a-109">Creare una chiave del registro di sistema nel nodo seguente.</span><span class="sxs-lookup"><span data-stu-id="bb24a-109">Create a registry key under the following node.</span></span> <span data-ttu-id="bb24a-110">Il nome del *servizio* è il nome registrato per l'allegato e deve essere lo stesso nome di servizio utilizzato in Gestione controllo servizi, un modulo che gestisce l'arresto e l'avvio dei servizi.</span><span class="sxs-lookup"><span data-stu-id="bb24a-110">The *service name* is the registered name for the attachment, and must be the same service name used in the Service Control Manager, a module which manages the stopping and starting of services.</span></span> <span data-ttu-id="bb24a-111">Il nome deve essere univoco, pertanto non è in conflitto con i nomi degli altri allegati.</span><span class="sxs-lookup"><span data-stu-id="bb24a-111">The name must also be unique so it does not conflict with the names of other attachments.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  <span data-ttu-id="bb24a-112">Creare il seguente valore stringa nella nuova chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bb24a-112">Create the following string value in the new registry key.</span></span> <span data-ttu-id="bb24a-113">*percorso motore allegato* è il percorso completo del modulo del motore di collegamento.</span><span class="sxs-lookup"><span data-stu-id="bb24a-113">*attachment engine path* is the full path to the attachment engine module.</span></span><dl> <dd><span data-ttu-id="bb24a-114">**ServiceAttachmentPath**  =  *percorso motore allegati*</span><span class="sxs-lookup"><span data-stu-id="bb24a-114">**ServiceAttachmentPath** = *attachment engine path*</span></span><dl> <dt>

<span data-ttu-id="bb24a-115">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bb24a-115">Data type</span></span>
</dt> <dd><span data-ttu-id="bb24a-116">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bb24a-116">REG_SZ</span></span></dd> </dl> </dd> </dl>

 

 



