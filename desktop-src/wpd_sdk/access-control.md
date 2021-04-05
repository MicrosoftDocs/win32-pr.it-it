---
description: Controllo di accesso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Controllo di accesso (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884917"
---
# <a name="access-control-wpd-api"></a><span data-ttu-id="d957c-103">Controllo di accesso (API WPD)</span><span class="sxs-lookup"><span data-stu-id="d957c-103">Access Control (WPD API)</span></span>

<span data-ttu-id="d957c-104">Il Windows Driver Model (WDM) supporta la restrizione dell'accesso ai dispositivi tramite elenchi di controllo di accesso (ACL) nei nodi del dispositivo Plug and Play (PnP).</span><span class="sxs-lookup"><span data-stu-id="d957c-104">The Windows Driver Model (WDM) supports restricting device access via Access Control Lists (ACLs) on the Plug and Play (PnP) Device Nodes.</span></span> <span data-ttu-id="d957c-105">Ciò significa che i fornitori e gli amministratori di rete possono limitare l'accesso a qualsiasi tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d957c-105">This means that vendors and network administrators can restrict access to any device type.</span></span> <span data-ttu-id="d957c-106">Quando un'applicazione apre un handle per un driver chiamando [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), il gestore di i/O del driver verifica se l'utente specificato ha l'accesso richiesto e, in modo analogo, verifica l'accesso quando IOCTL vengono inviati al driver da tale handle.</span><span class="sxs-lookup"><span data-stu-id="d957c-106">When an application opens a handle to a driver by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), the driver's I/O Manager verifies whether the given user has the required access, and similarly does access checks when IOCTLs are sent to the driver from that handle.</span></span>

<span data-ttu-id="d957c-107">Un amministratore di rete può, ad esempio, limitare l'accesso in sola lettura ai dispositivi portatili da parte degli utenti guest, sebbene possano concedere agli utenti autenticati l'accesso in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d957c-107">For example, a network administrator could restrict Guest users to read-only access for portable devices, while they could grant Authenticated users read/write access.</span></span> <span data-ttu-id="d957c-108">In questo caso, significa che se un Guest ha emesso un comando WPD che richiede l'accesso in lettura/scrittura (ad esempio delete Object); si verificherà un errore di accesso negato, mentre se un utente autenticato ha emesso lo stesso comando, avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d957c-108">In this case, it implies that if a Guest issued a WPD command that required read/write access (such as Delete Object); it would fail with Access Denied, whereas if an Authenticated user issued the same command, it would succeed.</span></span>

<span data-ttu-id="d957c-109">Il Criteri di gruppo voci per il controllo dell'accesso all'archiviazione rimovibile e ai dispositivi portatili non è in realtà un modo semplice per gli amministratori di applicare gli ACL del nodo del dispositivo PnP a un'intera classe di dispositivi alla volta (ad esempio, applicando l'accesso in scrittura per negare i dispositivi portatili) Criteri di gruppo modificare gli ACL di tutti i dispositivi WPD per negare l'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="d957c-109">The Group Policy entries for controlling access to removable storage and portable devices is actually nothing more than an easy way for Administrators to apply PnP device node ACLs to a whole class of devices at a time (for example, applying the "Deny Write Access to Portable Devices" Group Policy would adjust the ACLs of all WPD devices to deny write access).</span></span>

## <a name="io-control-codes-in-wpd"></a><span data-ttu-id="d957c-110">Codici di controllo di I/O in WPD</span><span class="sxs-lookup"><span data-stu-id="d957c-110">I/O Control Codes in WPD</span></span>

<span data-ttu-id="d957c-111">Le applicazioni WPD comunicano con i driver aprendo gli handle del dispositivo e inviando I codici di controllo di I/O (IOCTL).</span><span class="sxs-lookup"><span data-stu-id="d957c-111">WPD applications communicate with drivers by opening device handles and sending I/O Control Codes (IOCTLs).</span></span> <span data-ttu-id="d957c-112">Queste IOCTL sono costituite da quattro sezioni:</span><span class="sxs-lookup"><span data-stu-id="d957c-112">These IOCTLs consist of four sections:</span></span>

1.  <span data-ttu-id="d957c-113">Tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="d957c-113">Device Type</span></span>
2.  <span data-ttu-id="d957c-114">Codice funzione</span><span class="sxs-lookup"><span data-stu-id="d957c-114">Function Code</span></span>
3.  <span data-ttu-id="d957c-115">Buffer (metodo)</span><span class="sxs-lookup"><span data-stu-id="d957c-115">Buffer Method</span></span>
4.  <span data-ttu-id="d957c-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d957c-116">Access Type</span></span>

<span data-ttu-id="d957c-117">La quarta sezione, il tipo di accesso, specifica il requisito di accesso specifico per il comando specificato.</span><span class="sxs-lookup"><span data-stu-id="d957c-117">The fourth section, the Access Type, specifies the specific access requirement for the given command.</span></span> <span data-ttu-id="d957c-118">Il gestore di I/O del driver usa questi dati per eseguire il controllo dell'elenco di controllo di accesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="d957c-118">The driver's I/O manager uses this data to perform the Access Control List (ACL) check.</span></span>

<span data-ttu-id="d957c-119">Quindi, se un IOCTL è stato definito come:</span><span class="sxs-lookup"><span data-stu-id="d957c-119">So if an IOCTL were defined as:</span></span>


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



<span data-ttu-id="d957c-120">Il gestore di I/O del driver controlla che il proprietario dell'handle di dispositivo disponga dell'accesso in lettura al dispositivo quando viene inviato questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d957c-120">The driver's I/O manager would check that the owner of the device handle has read access to the device when this message is sent.</span></span>

<span data-ttu-id="d957c-121">E, se un IOCTL è stato definito come:</span><span class="sxs-lookup"><span data-stu-id="d957c-121">And, if an IOCTL were defined as:</span></span>


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



<span data-ttu-id="d957c-122">Il gestore di I/O del driver controlla che il proprietario dell'handle di dispositivo disponga dell'accesso in lettura/scrittura al dispositivo quando viene inviato questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d957c-122">The driver's I/O manager would check that the owner of the device handle has read/write access to the device when this message is sent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d957c-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d957c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d957c-124">**Panoramica dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="d957c-124">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="d957c-125">**IPortableDevice:: Open**</span><span class="sxs-lookup"><span data-stu-id="d957c-125">**IPortableDevice::Open**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[<span data-ttu-id="d957c-126">**IPortableDevice:: SendCommand**</span><span class="sxs-lookup"><span data-stu-id="d957c-126">**IPortableDevice::SendCommand**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



