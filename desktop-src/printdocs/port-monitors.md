---
description: Quando un driver di dispositivo ha convertito un intero file journal in comandi di dispositivo non elaborato, il file dei comandi convertiti viene passato nuovamente allo spooler.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitoraggi porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314531"
---
# <a name="port-monitors"></a><span data-ttu-id="317a8-103">Monitoraggi porta</span><span class="sxs-lookup"><span data-stu-id="317a8-103">Port Monitors</span></span>

<span data-ttu-id="317a8-104">Quando un driver di dispositivo ha convertito un intero file journal in comandi di dispositivo non elaborato, il file dei comandi convertiti viene passato nuovamente allo spooler.</span><span class="sxs-lookup"><span data-stu-id="317a8-104">Once a device driver has converted an entire journal file into raw device commands, the file of converted commands is passed back to the spooler.</span></span> <span data-ttu-id="317a8-105">Lo spooler invia questi comandi di basso livello a un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="317a8-105">The spooler sends these low-level commands to a monitor.</span></span> <span data-ttu-id="317a8-106">Un monitoraggio porta è un file con estensione dll che passa i comandi dei dispositivi non elaborati sulla rete, tramite una porta parallela o tramite una porta seriale al dispositivo di stampa.</span><span class="sxs-lookup"><span data-stu-id="317a8-106">A port monitor is a .dll that passes the raw device commands over the network, through a parallel port, or through a serial port to the printer device.</span></span> <span data-ttu-id="317a8-107">È possibile installare monitoraggi porta personalizzati per supportare il passaggio dei dati del dispositivo attraverso altre porte di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="317a8-107">Custom port monitors can be installed to support passing device data through other communication ports.</span></span>

<span data-ttu-id="317a8-108">Usare le funzioni seguenti per lavorare con i monitoraggi delle porte.</span><span class="sxs-lookup"><span data-stu-id="317a8-108">Use the following functions to work with port monitors.</span></span>



| <span data-ttu-id="317a8-109">Funzione</span><span class="sxs-lookup"><span data-stu-id="317a8-109">Function</span></span>                               | <span data-ttu-id="317a8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="317a8-110">Description</span></span>                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="317a8-111">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="317a8-111">**AddMonitor**</span></span>](addmonitor.md)       | <span data-ttu-id="317a8-112">Installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="317a8-112">Installs a local port monitor and links the configuration, data, and monitor files.</span></span> |
| [<span data-ttu-id="317a8-113">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="317a8-113">**DeleteMonitor**</span></span>](deletemonitor.md) | <span data-ttu-id="317a8-114">Rimuove un monitor di porta aggiunto dalla funzione [**AddMonitor**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="317a8-114">Removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>      |
| [<span data-ttu-id="317a8-115">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="317a8-115">**EnumMonitors**</span></span>](enummonitors.md)   | <span data-ttu-id="317a8-116">Enumera i monitoraggi delle porte installati in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="317a8-116">Enumerates the port monitors installed on a specified server.</span></span>                       |



 

 

 



