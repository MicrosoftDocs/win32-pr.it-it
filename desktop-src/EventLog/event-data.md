---
description: A ogni evento possono essere associati dati specifici degli eventi.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Dati eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308373"
---
# <a name="event-data"></a><span data-ttu-id="50270-103">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="50270-103">Event Data</span></span>

<span data-ttu-id="50270-104">A ogni evento possono essere associati dati specifici degli eventi.</span><span class="sxs-lookup"><span data-stu-id="50270-104">Each event can have event-specific data associated with it.</span></span> <span data-ttu-id="50270-105">Il Visualizzatore eventi non interpreta questi dati. vengono visualizzati dati aggiuntivi solo in un formato esadecimale e di testo combinato.</span><span class="sxs-lookup"><span data-stu-id="50270-105">The Event Viewer does not interpret this data; it displays extra data only in a combined hexadecimal and text format.</span></span> <span data-ttu-id="50270-106">Il limite massimo per la dimensione di un evento nel log even è 0x3FFFF bytes.</span><span class="sxs-lookup"><span data-stu-id="50270-106">The maximum limit on the size of an event in the even log is 0x3FFFF bytes.</span></span> <span data-ttu-id="50270-107">Pertanto, utilizzare dati specifici degli eventi sporadicamente, inclusi solo se si è certi che saranno utili a un utente che esegue il debug di un problema.</span><span class="sxs-lookup"><span data-stu-id="50270-107">Therefore, use event-specific data sparingly, including it only if you are sure it will be useful to someone debugging a problem.</span></span> <span data-ttu-id="50270-108">Molti eventi correlati alla rete, ad esempio, includono i blocchi di controllo di rete (BCN) come dati specifici degli eventi.</span><span class="sxs-lookup"><span data-stu-id="50270-108">For example, many network-related events include network control blocks (NCB) as event-specific data.</span></span>

<span data-ttu-id="50270-109">Quando si usano dati specifici degli eventi, l'ultima parte della relativa stringa di descrizione deve fornire una nota sulle informazioni fornite come dati specifici dell'evento.</span><span class="sxs-lookup"><span data-stu-id="50270-109">When you use event-specific data, the last part of its description string should provide a note about the information provided as event-specific data.</span></span> <span data-ttu-id="50270-110">Il software di rete, ad esempio, potrebbe fornire una nota come: "(la BCN è costituita dai dati dell'evento)". Come convenzione, usare le parentesi per racchiudere tali osservazioni, come indicato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="50270-110">For example, the network software could provide a note such as: "(The NCB is the event data.)" As a convention, use parentheses around such remarks, as indicated in this example.</span></span>

<span data-ttu-id="50270-111">È anche possibile usare dati specifici dell'evento per archiviare le informazioni che l'applicazione può elaborare in modo indipendente dal Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="50270-111">You can also use event-specific data to store information the application can process independently of the Event Viewer.</span></span> <span data-ttu-id="50270-112">Ad esempio, è possibile scrivere un visualizzatore specifico per gli eventi oppure scrivere un programma che analizza il log e crea un report che include le informazioni dei dati specifici dell'evento.</span><span class="sxs-lookup"><span data-stu-id="50270-112">For example, you could write a viewer specifically for your events, or write a program that scans the log and creates a report that includes information from the event-specific data.</span></span>

 

 



