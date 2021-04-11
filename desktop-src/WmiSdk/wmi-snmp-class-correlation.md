---
description: La correlazione influiscono sul set di classi restituite da archivio SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Correlazione della classe SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc0ca4740c90563fce05e1b6352ef33b0e3ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226936"
---
# <a name="wmi-snmp-class-correlation"></a><span data-ttu-id="6a515-103">Correlazione della classe SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="6a515-103">WMI SNMP Class Correlation</span></span>

<span data-ttu-id="6a515-104">La correlazione influiscono sul set di classi restituite da archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="6a515-104">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="6a515-105">Le classi correlate sono quelle che un determinato dispositivo SNMP è in grado di supportare nel momento in cui si verifica l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="6a515-105">Correlated classes are those that a given SNMP device is known to support at the time enumeration occurs.</span></span> <span data-ttu-id="6a515-106">L'enumerazione non correlata restituisce tutte le classi presenti all'interno di archivio SMIR, indipendentemente dal fatto che siano supportate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a515-106">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="6a515-107">La correlazione è una funzionalità del provider SNMP WMI e può essere disattivata o attivata (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="6a515-107">Correlation is a feature of the WMI SNMP provider and can be turned off or on (default).</span></span>

> [!Note]  
> <span data-ttu-id="6a515-108">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6a515-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="6a515-109">La correlazione potrebbe impedire la visualizzazione di tutte le classi effettivamente supportate da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a515-109">Correlation might prevent you from seeing all of the classes that are actually supported by a device.</span></span> <span data-ttu-id="6a515-110">Se è noto che una determinata classe è supportata, ma non viene visualizzata in archivio SMIR, questo può essere dovuto a diversi motivi, uno dei quali è la correlazione.</span><span class="sxs-lookup"><span data-stu-id="6a515-110">If you know that a particular class is supported but it does not appear in the SMIR, this could be due to several reasons, one of which is correlation.</span></span> <span data-ttu-id="6a515-111">Prendere in considerazione la disattivazione della correlazione prima di scrivere nel dispositivo in questione.</span><span class="sxs-lookup"><span data-stu-id="6a515-111">Consider turning correlation off before writing to the device in question.</span></span> <span data-ttu-id="6a515-112">Tuttavia, la disattivazione della correlazione comporta la probabilità che molte classi non supportate dal dispositivo vengano visualizzate in archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="6a515-112">However, turning correlation off results in the likelihood that many classes not supported by the device will appear in the SMIR.</span></span> <span data-ttu-id="6a515-113">Inoltre, l'utilizzo della correlazione comporta un costo in termini di prestazioni, in quanto viene eseguita una query sul dispositivo per vedere quali classi sono supportate.</span><span class="sxs-lookup"><span data-stu-id="6a515-113">Also, there is a performance cost in using correlation because the device is queried to see what classes it supports.</span></span> <span data-ttu-id="6a515-114">Quando la correlazione è attivata, il provider SNMP causa un'enumerazione delle classi supportate dal dispositivo in modo analogo al risultato dell'esecuzione di uno strumento di *percorso MIB* .</span><span class="sxs-lookup"><span data-stu-id="6a515-114">When correlation is turned on, the SNMP provider causes an enumeration of device-supported classes similar to the result of running a *mib walk* tool.</span></span>

<span data-ttu-id="6a515-115">Un gestore reti, ad esempio, vuole conoscere diversi elementi chiave di dati relativi a tutti gli hub gestiti in una determinata rete.</span><span class="sxs-lookup"><span data-stu-id="6a515-115">For example, a network manager wants to know several key pieces of data about all the managed hubs in a particular network.</span></span> <span data-ttu-id="6a515-116">Un database dei dispositivi correnti e del relativo MIB supportato esiste già, pertanto non è necessario basarsi sulla funzione di correlazione del dispositivo per fornire gli elementi dati supportati.</span><span class="sxs-lookup"><span data-stu-id="6a515-116">A database of the current devices and their supported MIBs already exists, so there is no need to rely on the correlation function of the device to provide the supported data elements.</span></span> <span data-ttu-id="6a515-117">In questo caso, la correlazione potrebbe essere disattivata.</span><span class="sxs-lookup"><span data-stu-id="6a515-117">In this case, correlation could be turned off.</span></span>

<span data-ttu-id="6a515-118">Nell'esempio seguente viene illustrato come disattivare la correlazione.</span><span class="sxs-lookup"><span data-stu-id="6a515-118">The following example shows how to turn off correlation.</span></span>


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



<span data-ttu-id="6a515-119">D'altra parte, un altro gestore reti potrebbe voler monitorare tutte le unità disco del computer UNIX sulla rete, ma non ha familiarità con i dati MIB in tali computer.</span><span class="sxs-lookup"><span data-stu-id="6a515-119">On the other hand, another network manager may want to monitor all the UNIX machine disk drives on the network but is unfamiliar with the MIB data on those machines.</span></span> <span data-ttu-id="6a515-120">In tal caso, la correlazione verrebbe attivata.</span><span class="sxs-lookup"><span data-stu-id="6a515-120">In that case, correlation would be turned on.</span></span>

 

 



