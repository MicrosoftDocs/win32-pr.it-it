---
description: Interfacce di connessione MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfacce di connessione MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058187"
---
# <a name="mtpbluetooth-connection-interfaces"></a><span data-ttu-id="d5ac7-103">Interfacce di connessione MTP/Bluetooth</span><span class="sxs-lookup"><span data-stu-id="d5ac7-103">MTP/Bluetooth Connection Interfaces</span></span>

<span data-ttu-id="d5ac7-104">Le interfacce seguenti consentono alle applicazioni di enumerare e connettersi solo ai dispositivi che supportano il protocollo MTP (Media Transfer Protocol) su Bluetooth (MTP/Bluetooth).</span><span class="sxs-lookup"><span data-stu-id="d5ac7-104">The following interfaces allow applications to enumerate and connect only to devices that support the Media Transfer Protocol (MTP) over Bluetooth (MTP/Bluetooth).</span></span> <span data-ttu-id="d5ac7-105">Le interfacce del driver WPD, della raccolta e del client non sono limitate al protocollo MTP/Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d5ac7-105">The WPD driver-, collection-, and client-interfaces are not restricted to the MTP/ Bluetooth protocol.</span></span>



| <span data-ttu-id="d5ac7-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="d5ac7-106">Interface</span></span>                                                              | <span data-ttu-id="d5ac7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5ac7-107">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5ac7-108">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="d5ac7-108">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)       | <span data-ttu-id="d5ac7-109">Definisce un unico metodo di callback utilizzato dalle applicazioni per ricevere la notifica delle richieste completate e annullate.</span><span class="sxs-lookup"><span data-stu-id="d5ac7-109">Defines a single callback method that applications use to receive notification of completed and cancelled requests.</span></span> |
| [<span data-ttu-id="d5ac7-110">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="d5ac7-110">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md) | <span data-ttu-id="d5ac7-111">Enumera le interfacce **IPortableDeviceConnector** .</span><span class="sxs-lookup"><span data-stu-id="d5ac7-111">Enumerates **IPortableDeviceConnector** interfaces.</span></span>                                                                 |
| [<span data-ttu-id="d5ac7-112">**IPortableDeviceConnector**</span><span class="sxs-lookup"><span data-stu-id="d5ac7-112">**IPortableDeviceConnector**</span></span>](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | <span data-ttu-id="d5ac7-113">Supporta i metodi chiamati dalle applicazioni per stabilire connessioni ai dispositivi Bluetooth MTP.</span><span class="sxs-lookup"><span data-stu-id="d5ac7-113">Supports methods that applications call to establish connections to MTP Bluetooth devices.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="d5ac7-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5ac7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5ac7-115">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="d5ac7-115">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



