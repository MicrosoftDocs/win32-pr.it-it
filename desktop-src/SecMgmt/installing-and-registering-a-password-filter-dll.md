---
description: La DLL del filtro password di Windows, Passfilt.dll, viene eseguita nel contesto di sicurezza dell'account di sistema locale e consente di filtrare le password dell'account di dominio o locale.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installazione e registrazione di una DLL di filtro password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882089"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="e9bca-103">Installazione e registrazione di una DLL di filtro password</span><span class="sxs-lookup"><span data-stu-id="e9bca-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="e9bca-104">È possibile utilizzare il filtro password di Windows per filtrare le password dell'account di dominio o locale.</span><span class="sxs-lookup"><span data-stu-id="e9bca-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="e9bca-105">Per utilizzare il filtro password per gli account di dominio, installare e registrare la DLL in ogni controller di dominio nel dominio.</span><span class="sxs-lookup"><span data-stu-id="e9bca-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="e9bca-106">Per installare il filtro delle password, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="e9bca-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="e9bca-107">È possibile eseguire questi passaggi manualmente oppure è possibile scrivere un programma di installazione per eseguire questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="e9bca-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="e9bca-108">Per eseguire questa procedura, è necessario essere un amministratore o appartenere al gruppo di amministratori.</span><span class="sxs-lookup"><span data-stu-id="e9bca-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="e9bca-109">**Per installare e registrare una DLL di filtro password Windows**</span><span class="sxs-lookup"><span data-stu-id="e9bca-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="e9bca-110">Copiare la DLL nella directory di installazione di Windows nel controller di dominio o nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e9bca-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="e9bca-111">Nelle installazioni standard, la cartella predefinita è \\ Windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="e9bca-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="e9bca-112">Assicurarsi di creare una DLL di filtro password a 32 bit per computer a 32 bit e una DLL di filtro password a 64 bit per computer a 64 bit, quindi copiarli nel percorso appropriato.</span><span class="sxs-lookup"><span data-stu-id="e9bca-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="e9bca-113">Per registrare il filtro password, aggiornare la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="e9bca-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="e9bca-114">Se la sottochiave **pacchetti di notifica** esiste, aggiungere il nome della dll ai dati del valore esistente.</span><span class="sxs-lookup"><span data-stu-id="e9bca-114">If the **Notification Packages** subkey exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="e9bca-115">Non sovrascrivere i valori esistenti e non includere l'estensione. dll.</span><span class="sxs-lookup"><span data-stu-id="e9bca-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="e9bca-116">Se la sottochiave **pacchetti di notifica** non esiste, aggiungerla e quindi specificare il nome della dll per i dati del valore.</span><span class="sxs-lookup"><span data-stu-id="e9bca-116">If the **Notification Packages** subkey does not exist, add it, and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="e9bca-117">Non includere l'estensione. dll.</span><span class="sxs-lookup"><span data-stu-id="e9bca-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="e9bca-118">La sottochiave **pacchetti di notifica** può aggiungere più pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e9bca-118">The **Notification Packages** subkey can add multiple packages.</span></span>

3.  <span data-ttu-id="e9bca-119">Individuare l'impostazione relativa alla complessità delle password.</span><span class="sxs-lookup"><span data-stu-id="e9bca-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="e9bca-120">Nel pannello di controllo fare clic su **prestazioni e manutenzione**, fare clic su **strumenti di amministrazione**, fare doppio clic su **criteri di sicurezza locali**, fare doppio clic su criteri **account**, quindi fare doppio clic su **criteri password**.</span><span class="sxs-lookup"><span data-stu-id="e9bca-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="e9bca-121">Per applicare sia il filtro password di Windows predefinito che il filtro password personalizzato, assicurarsi che l'impostazione dei criteri **password deve soddisfare i requisiti di complessità** sia abilitata.</span><span class="sxs-lookup"><span data-stu-id="e9bca-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="e9bca-122">In caso contrario, disabilitare le **password devono soddisfare i requisiti di complessità** impostazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="e9bca-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9bca-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9bca-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9bca-124">Considerazioni sulla programmazione del filtro password</span><span class="sxs-lookup"><span data-stu-id="e9bca-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="e9bca-125">Imposizione avanzata delle password e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="e9bca-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="e9bca-126">Funzioni di filtro password</span><span class="sxs-lookup"><span data-stu-id="e9bca-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



