---
title: Fornire le autorizzazioni utente per i dispositivi con masterizzazione multimediale
description: Per impostazione predefinita, Windows Vista e Windows Server 2008 concedono l'accesso in lettura/scrittura agli amministratori e agli utenti connessi direttamente al computer (utenti intermedi).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104234423"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a><span data-ttu-id="5b942-103">Fornire le autorizzazioni utente per i dispositivi con masterizzazione multimediale</span><span class="sxs-lookup"><span data-stu-id="5b942-103">Providing User Permissions for Media Burning Devices</span></span>

<span data-ttu-id="5b942-104">Per impostazione predefinita, Windows Vista e Windows Server 2008 concedono l'accesso in lettura/scrittura agli amministratori e agli utenti connessi direttamente al computer (utenti intermedi).</span><span class="sxs-lookup"><span data-stu-id="5b942-104">By default, both Windows Vista and Windows Server 2008 grant read/write access to administrators and users logged directly into the machine (intermediate users).</span></span> <span data-ttu-id="5b942-105">Tuttavia, in Windows XP e Windows Server 2003 un amministratore deve concedere questi privilegi di lettura/scrittura al dispositivo ad altri gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="5b942-105">However, in Windows XP and Windows Server 2003 an administrator must grant these device read/write privileges to other user groups.</span></span>

<span data-ttu-id="5b942-106">Un amministratore può modificare le autorizzazioni specifiche relative ai dispositivi per utenti esperti e utenti interattivi.</span><span class="sxs-lookup"><span data-stu-id="5b942-106">An administrator may adjust specific device-related permissions for power users and interactive users.</span></span>

<span data-ttu-id="5b942-107">Per accedere al pannello autorizzazioni gruppo appropriato in Windows XP, fare clic sul pulsante **Start**, scegliere **Esegui**, digitare **gpedit. msc**, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b942-107">To reach the appropriate group permissions panel in Windows XP, click **Start**, click **Run**, type **gpedit.msc**, and then click **OK**.</span></span> <span data-ttu-id="5b942-108">Nell'interfaccia Criteri di gruppo espandere **Configurazione computer**, **impostazioni di Windows**, **Impostazioni protezione**, **criteri locali**, quindi fare doppio clic su **Opzioni di sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="5b942-108">In the Group Policy interface, expand **Computer Configuration**, expand **Windows Settings**, expand **Security Settings**, expand **Local Policies**, and double-click **Security Options**.</span></span>

![Screenshot che mostra la finestra "Criteri di gruppo" con i criteri selezionati nel riquadro "criteri".](images/gpolpanel.jpg)

<span data-ttu-id="5b942-110">In questo pannello, un amministratore deve specificare le impostazioni di due opzioni del dispositivo per fornire le autorizzazioni necessarie per il gruppo:</span><span class="sxs-lookup"><span data-stu-id="5b942-110">At this panel, an administrator must specify the settings of two device options to provide the required group permissions:</span></span>

-   <span data-ttu-id="5b942-111">Imposta "dispositivi: limita l'accesso CD-ROM al solo utente connesso localmente" per **abilitare**</span><span class="sxs-lookup"><span data-stu-id="5b942-111">Set "Devices: Restrict CD-ROM access to locally logged-on user only" to **Enabled**</span></span>
-   <span data-ttu-id="5b942-112">Impostare "dispositivi: consentito formattare ed estrarre supporti rimovibili" per **gli amministratori e gli utenti avanzati**.</span><span class="sxs-lookup"><span data-stu-id="5b942-112">Set "Devices: Allowed to format and eject removable media" to **Administrators and Power Users**.</span></span> <span data-ttu-id="5b942-113">È inoltre possibile emulare le autorizzazioni di Windows Vista impostando questa opzione su **amministratori e utenti interattivi**.</span><span class="sxs-lookup"><span data-stu-id="5b942-113">It is also possible to emulate Windows Vista permissions by setting this option to **Administrators and Interactive Users**.</span></span>

<span data-ttu-id="5b942-114">Sebbene non esista un'interfaccia utente specifica in Windows XP o Windows Server 2003 per l'uso di [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) o [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), è possibile usare queste API per concedere a gruppi di utenti personalizzati le autorizzazioni per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="5b942-114">While a specific UI does not exist in Windows XP or Windows Server 2003 for the use of [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) or [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), it is possible to use these APIs to grant custom user groups device permissions.</span></span> <span data-ttu-id="5b942-115">Una chiamata a **SetSecurityInfo** , ad esempio, consentirà di concedere le autorizzazioni ai gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="5b942-115">For example, a call to **SetSecurityInfo** will grant permissions to user groups.</span></span> <span data-ttu-id="5b942-116">Le modifiche alle autorizzazioni con questa API sono temporanee e non verranno mantenute durante il riavvio.</span><span class="sxs-lookup"><span data-stu-id="5b942-116">Permission changes with this API are temporary and will not persist across a reboot.</span></span> <span data-ttu-id="5b942-117">Tuttavia, la chiamata di [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) implementerà le modifiche delle autorizzazioni nel registro di sistema, che rimarranno in modo permanente in un riavvio.</span><span class="sxs-lookup"><span data-stu-id="5b942-117">However, calling [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) will implement the permission changes in the registry, which will persist across a reboot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b942-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b942-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b942-119">Uso di IMAPi</span><span class="sxs-lookup"><span data-stu-id="5b942-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="5b942-120">**SetSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="5b942-120">**SetSecurityInfo**</span></span>](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[<span data-ttu-id="5b942-121">SetupDiSetDeviceRegistryProperty</span><span class="sxs-lookup"><span data-stu-id="5b942-121">SetupDiSetDeviceRegistryProperty</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 