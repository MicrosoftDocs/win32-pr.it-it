---
description: Oltre a PrintCapabilities, PrintTicket consente di aggiungere informazioni aggiuntive dai client sotto forma di elementi Property.
ms.assetid: 00f1d2c4-3c71-4b64-b689-83b4399aa61d
title: Informazioni di configurazione non correlate a PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e4ac332d6e9b106ab9d68c29d03366761c01d5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409654"
---
# <a name="configuration-information-not-related-to-printcapabilities"></a><span data-ttu-id="e9dbc-103">Informazioni di configurazione non correlate a PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="e9dbc-103">Configuration Information Not Related to PrintCapabilities</span></span>

<span data-ttu-id="e9dbc-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="e9dbc-104">This topic is not current.</span></span> <span data-ttu-id="e9dbc-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e9dbc-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e9dbc-106">Oltre a fornire selezioni per gli attributi del dispositivo definiti in PrintCapabilities, PrintTicket consente di aggiungere informazioni aggiuntive dai client sotto forma di elementi Property.</span><span class="sxs-lookup"><span data-stu-id="e9dbc-106">In addition to providing selections for the device attributes defined in the PrintCapabilities, the PrintTicket allows additional information to be added by clients in the form of Property elements.</span></span> <span data-ttu-id="e9dbc-107">Lo schema di stampa definisce una serie di istanze property standard e il provider di interfaccia è libero di introdurre anche istanze di proprietà private.</span><span class="sxs-lookup"><span data-stu-id="e9dbc-107">The Print Schema defines a number of standard Property instances, and the interface provider is free to introduce private Property instances as well.</span></span> <span data-ttu-id="e9dbc-108">Ad esempio, se i membri di un'organizzazione inviano la maggior parte dei processi di stampa a una struttura batch centrale, possono specificare per ogni processo un'istanza di Proprietà privata che contiene un indirizzo mittente.</span><span class="sxs-lookup"><span data-stu-id="e9dbc-108">For example, if members of an organization send most of their print jobs to a central batch facility, they can specify for each job a private Property instance that contains a return address.</span></span> <span data-ttu-id="e9dbc-109">Questa proprietà può semplificare il recapito del processo completato all'iniziatore.</span><span class="sxs-lookup"><span data-stu-id="e9dbc-109">This Property can make it easier to deliver the completed job can be delivered to the originator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9dbc-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9dbc-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9dbc-111">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="e9dbc-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



