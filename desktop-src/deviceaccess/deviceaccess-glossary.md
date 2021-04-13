---
title: Glossario di accesso ai dispositivi
description: Di seguito sono riportati i termini usati in tutta la documentazione per l'API di accesso ai dispositivi.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398524"
---
# <a name="device-access-glossary"></a><span data-ttu-id="11355-103">Glossario di accesso ai dispositivi</span><span class="sxs-lookup"><span data-stu-id="11355-103">Device Access Glossary</span></span>

<span data-ttu-id="11355-104">Di seguito sono riportati i termini usati in tutta la documentazione per l'API di accesso ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="11355-104">The following are terms used throughout the documentation for the Device Access API.</span></span>

<dl> <dt>

<span data-ttu-id="11355-105">**AppContainer**</span><span class="sxs-lookup"><span data-stu-id="11355-105">**AppContainer**</span></span>
</dt> <dd>

<span data-ttu-id="11355-106">Ambiente di esecuzione altamente limitato in cui un processo viene eseguito con un subset ridotto dei privilegi dell'utente.</span><span class="sxs-lookup"><span data-stu-id="11355-106">A highly restricted execution environment in which a process runs with a reduced subset of the user's privileges.</span></span> <span data-ttu-id="11355-107">Un processo in esecuzione all'interno di un AppContainer viene chiamato processo AppContainer.</span><span class="sxs-lookup"><span data-stu-id="11355-107">A process that's running within an AppContainer is called an AppContainer process.</span></span> <span data-ttu-id="11355-108">Un processo AppContainer è isolato dagli altri processi AppContainer e dal profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="11355-108">An AppContainer process is isolated from other AppContainer processes and from the user's profile.</span></span> <span data-ttu-id="11355-109">Ha accesso limitato a un piccolo subset di risorse di sistema, ad esempio file, dispositivi, chiavi del registro di sistema, IPC (Interprocess Communication) endpoint di chiamata di procedura/remote (RPC) e risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="11355-109">It has limited access to a very small subset of system resources like files, devices, registry keys, interprocess communication (IPC)/remote procedure call (RPC) endpoints, and network resources.</span></span>

</dd> <dt>

<span data-ttu-id="11355-110">**Associazione**</span><span class="sxs-lookup"><span data-stu-id="11355-110">**Binding**</span></span>
</dt> <dd>

<span data-ttu-id="11355-111">Associazione di un oggetto di accesso al dispositivo a una particolare interfaccia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11355-111">Associating a device access object with a particular device interface.</span></span> <span data-ttu-id="11355-112">Se l'associazione ha esito positivo, le app di Windows Store possono usare l'oggetto accesso al dispositivo come broker per comunicare con il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11355-112">If binding is successful, Windows Store apps can use the device access object as a broker to communicate with the device driver.</span></span>

</dd> <dt>

<span data-ttu-id="11355-113">**Gestore**</span><span class="sxs-lookup"><span data-stu-id="11355-113">**Broker**</span></span>
</dt> <dd>

<span data-ttu-id="11355-114">Componente che fornisce l'accesso a una risorsa che non viene concessa per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="11355-114">A component that provides access to a resource that isn't granted by default.</span></span>

</dd> <dt>

<span data-ttu-id="11355-115">**App con privilegi**</span><span class="sxs-lookup"><span data-stu-id="11355-115">**Privileged App**</span></span>
</dt> <dd>

<span data-ttu-id="11355-116">App identificata nei metadati di un determinato dispositivo come associato a tale dispositivo, in modo che possa comunicare con l'interfaccia limitata del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11355-116">An app that's identified in a particular device's metadata as associated with that device, so that it can communicate with the device driver's restricted interface.</span></span> <span data-ttu-id="11355-117">Un esempio di un'app di questo tipo potrebbe essere un'app per la riproduzione di musica proprietaria che dispone di autorizzazioni esclusive per la sincronizzazione con un lettore musicale portatile, quando le app dei concorrenti non possono.</span><span class="sxs-lookup"><span data-stu-id="11355-117">An example of such an app might be a proprietary music playback app that has exclusive permission to sync with a portable music player, when apps from competitors can't.</span></span> <span data-ttu-id="11355-118">Per altre informazioni su come impostare i metadati di un dispositivo o su come limitare un driver alle app con privilegi, vedere [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span><span class="sxs-lookup"><span data-stu-id="11355-118">For more information about how to set a device's metadata or how to restrict a driver to privileged apps, see [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span></span>

</dd> </dl>
