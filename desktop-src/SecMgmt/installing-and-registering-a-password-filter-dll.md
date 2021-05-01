---
description: La DLL di filtro delle password di Windows, Passfilt.dll, viene eseguita nel contesto di sicurezza dell'account di sistema locale e consente di filtrare le password dell'account di dominio o locale.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installazione e registrazione di una DLL di filtro password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327166"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="9cc87-103">Installazione e registrazione di una DLL di filtro password</span><span class="sxs-lookup"><span data-stu-id="9cc87-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="9cc87-104">È possibile usare il filtro password di Windows per filtrare le password di dominio o dell'account locale.</span><span class="sxs-lookup"><span data-stu-id="9cc87-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="9cc87-105">Per usare il filtro password per gli account di dominio, installare e registrare la DLL in ogni controller di dominio nel dominio.</span><span class="sxs-lookup"><span data-stu-id="9cc87-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="9cc87-106">Per installare il filtro password, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="9cc87-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="9cc87-107">È possibile eseguire questi passaggi manualmente oppure scrivere un programma di installazione per eseguire questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="9cc87-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="9cc87-108">Per eseguire questa procedura, è necessario essere un amministratore o appartenere al gruppo di amministratori.</span><span class="sxs-lookup"><span data-stu-id="9cc87-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="9cc87-109">**Per installare e registrare una DLL di filtro password di Windows**</span><span class="sxs-lookup"><span data-stu-id="9cc87-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="9cc87-110">Copiare la DLL nella directory di installazione di Windows nel controller di dominio o nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="9cc87-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="9cc87-111">Nelle installazioni standard la cartella predefinita è \\ \\ Windows System32.</span><span class="sxs-lookup"><span data-stu-id="9cc87-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="9cc87-112">Assicurarsi di creare una DLL di filtro password a 32 bit per i computer a 32 bit e una DLL di filtro password a 64 bit per i computer a 64 bit e quindi copiarle nel percorso appropriato.</span><span class="sxs-lookup"><span data-stu-id="9cc87-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="9cc87-113">Per registrare il filtro password, aggiornare la chiave del Registro di sistema di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="9cc87-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="9cc87-114">Se il **valore pacchetti di** notifica di tipo *REG_MULTI_SZ* esistente, aggiungere il nome della DLL ai dati di valore esistenti.</span><span class="sxs-lookup"><span data-stu-id="9cc87-114">If the **Notification Packages** value of type *REG_MULTI_SZ* exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="9cc87-115">Non sovrascrivere i valori esistenti e non includere l'estensione dll.</span><span class="sxs-lookup"><span data-stu-id="9cc87-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="9cc87-116">Se il **valore Pacchetti di** notifica non esiste, crearlo, assegnargli il tipo *REG_MULTI_SZ* e quindi specificare il nome della DLL per i dati del valore.</span><span class="sxs-lookup"><span data-stu-id="9cc87-116">If the **Notification Packages** value does not exist, create it, give it the *REG_MULTI_SZ* type and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="9cc87-117">Non includere l'estensione dll.</span><span class="sxs-lookup"><span data-stu-id="9cc87-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="9cc87-118">Il **valore Pacchetti di** notifica può aggiungere più pacchetti.</span><span class="sxs-lookup"><span data-stu-id="9cc87-118">The **Notification Packages** value can add multiple packages.</span></span>

3.  <span data-ttu-id="9cc87-119">Trovare l'impostazione di complessità della password.</span><span class="sxs-lookup"><span data-stu-id="9cc87-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="9cc87-120">In Pannello di controllo fare clic su Prestazioni e manutenzione **,** su Strumenti di amministrazione **,** fare doppio clic su Criteri di sicurezza locali **,** fare doppio clic su Criteri account **,** quindi fare doppio clic su **Criteri password**.</span><span class="sxs-lookup"><span data-stu-id="9cc87-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="9cc87-121">Per applicare sia il filtro password predefinito di Windows che il filtro password personalizzato, assicurarsi che l'impostazione dei criteri Password **deve soddisfare** i requisiti di complessità sia abilitata.</span><span class="sxs-lookup"><span data-stu-id="9cc87-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="9cc87-122">In caso contrario, disabilitare **l'impostazione dei** criteri Password che devono soddisfare i requisiti di complessità.</span><span class="sxs-lookup"><span data-stu-id="9cc87-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cc87-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cc87-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cc87-124">Considerazioni sulla programmazione del filtro password</span><span class="sxs-lookup"><span data-stu-id="9cc87-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="9cc87-125">Imposizione delle password complessa e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="9cc87-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="9cc87-126">Funzioni di filtro password</span><span class="sxs-lookup"><span data-stu-id="9cc87-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



