---
description: La qualità del servizio (QoS) viene implementata in Windows attraverso diversi componenti QoS supportati in Windows Server 2003, Windows XP e Windows 2000.
ms.assetid: e55b085f-6f72-4aa4-a8b0-b7609b9010dc
title: Qualità del servizio in Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87d37f2e30e0a4fb296fc340353e2f4d85b5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310459"
---
# <a name="quality-of-service-in-the-windows-sockets-2-spi"></a><span data-ttu-id="2f66e-103">Qualità del servizio in Windows Sockets 2 SPI</span><span class="sxs-lookup"><span data-stu-id="2f66e-103">Quality of Service in the Windows Sockets 2 SPI</span></span>

<span data-ttu-id="2f66e-104">La qualità del servizio (QoS) viene implementata in Windows attraverso diversi componenti QoS supportati in Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2f66e-104">Quality of Service (QoS) is implemented in Windows through various QoS components supported on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="2f66e-105">Una spiegazione dettagliata di QoS e dei relativi componenti si trova in una sezione dedicata alla qualità del servizio, disponibile in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2f66e-105">A detailed explanation of QoS and its components is located in a section dedicated to Quality of Service, located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2f66e-106">Ogni componente QoS e il ruolo che svolge nell'implementazione QoS sono descritti in questa sezione QoS, con indicazioni aggiuntive fornite per l'implementazione di applicazioni e servizi abilitati per QoS.</span><span class="sxs-lookup"><span data-stu-id="2f66e-106">Each QoS component, and the role it plays in the QoS implementation, is explained in this QoS section, with additional guidance provided for the implementation of QoS-enabled applications and services.</span></span> <span data-ttu-id="2f66e-107">Per informazioni più dettagliate, vedere la sezione relativa alla [qualità del servizio (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2f66e-107">Please see the [Quality of Service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) section of the Windows SDK for more detailed information.</span></span>

<span data-ttu-id="2f66e-108">Questa sezione descrive la qualità delle funzionalità del servizio disponibili per gli sviluppatori Winsock.</span><span class="sxs-lookup"><span data-stu-id="2f66e-108">This section describes Quality of Service capabilities available to Winsock developers.</span></span> <span data-ttu-id="2f66e-109">Nell'elenco seguente vengono descritti gli argomenti di questa sezione:</span><span class="sxs-lookup"><span data-stu-id="2f66e-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="2f66e-110">Modello di utilizzo</span><span class="sxs-lookup"><span data-stu-id="2f66e-110">Usage Model</span></span>](usage-model-2.md)
-   [<span data-ttu-id="2f66e-111">Aggiornamenti QoS</span><span class="sxs-lookup"><span data-stu-id="2f66e-111">QoS Updates</span></span>](qos-updates-2.md)
-   [<span data-ttu-id="2f66e-112">Valori predefiniti in SPI</span><span class="sxs-lookup"><span data-stu-id="2f66e-112">Default Values in the SPI</span></span>](default-values-in-the-spi-2.md)
-   [<span data-ttu-id="2f66e-113">Modelli QoS in SPI</span><span class="sxs-lookup"><span data-stu-id="2f66e-113">QoS Templates in the SPI</span></span>](qos-templates-in-the-spi-2.md)

## <a name="related-topics"></a><span data-ttu-id="2f66e-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f66e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f66e-115">QoS (Quality of Service)</span><span class="sxs-lookup"><span data-stu-id="2f66e-115">Quality of Service (QoS)</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> <dt>

<span data-ttu-id="2f66e-116">[Che cos'è QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2f66e-116">[What Is QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="2f66e-117">Estensione QoS ATM Winsock</span><span class="sxs-lookup"><span data-stu-id="2f66e-117">Winsock ATM QoS Extension</span></span>](winsock-atm-qos-extension.md)
</dt> <dt>

[<span data-ttu-id="2f66e-118">**IOCTL Winsock**</span><span class="sxs-lookup"><span data-stu-id="2f66e-118">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
